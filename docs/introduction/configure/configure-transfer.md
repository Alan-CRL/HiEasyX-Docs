---
comments: true
---

# 迁移项目并配置 HiEasyX 库

本文档适用于 **项目从 EasyX 迁移至 HiEasyX 库** 的迁移方案，如果想在新项目中直接使用 HiEasyX，请单击[此处](configure-new.md)

## Step 1: 配置 HiEasyX

1、 下载仓库到本地

2、 请将项目字符集设置为 `unicode` 因为 HiEasyX 暂时不支持 多字符字符集（MBCS）。

!!! info ""
    将项目字符集设置成 `unicode` 可能会引发报错，请阅读[此篇文章](https://codebus.cn/yangw/about-unicode)自行修改。
    
    如果您的项目本来就是 `unicode` 字符集，那真是太好了！您可以进行下一步了。
    
3、 复制仓库项目中的 `./HiEasyX/HiEasyX.h` 文件 和 `./HiEasyX/HiEasyX/` 整个文件夹到您的项目目录下

4、 将刚才复制的文件和文件夹加入到您的 Visual Studio 项目中（拖入 Visual Studio 的项目资源管理器即可，或可以手动添加）

???+ info "温馨提示"

    由于 HiEasyX 源码文件较多，故建议在 Visual Studio 项目资源管理器中创建 HiEasyX   筛选器，将上述文件和文件夹都拖入此筛选器中，这样可以使项目结构更整洁。第一次编译需要编译全部文件，所以耗时较长，后面就不会了。

## Step 2: 改头文件

首先确保您已在项目中配置 HiEasyX。

然后，只需要将

```cpp
#include <easyx.h>
```

或

```cpp
#include <graphics.h>
```

改为

```cpp
#include "HiEasyX.h"
```

## Step 3: 标识窗口任务

如果原项目中使用了双缓冲，则一定会调用 `FlushBatchDraw` 函数，这样就能更方便地找出每个绘图代码块了，否则就需要将每个绘图代码块手动找出来。

只要在绘图代码块的前后分别加上：

```cpp
BEGIN_TASK();
```

和

```cpp
END_TASK();
```

即可。窗口任务相关内容已在前文交代清楚，故不再重复。注意不要将不必要的代码也放入窗口任务中。

### 迁移示例

下面将展示把原代码和迁移后的代码

=== "示例一"

    ```cpp title="使用 EasyX 时的代码"
    #include <easyx.h>
    
    int main()
    {
        initgraph();
        
        while(1)
        {
            BeginBatchDraw();
            
            circle(320, 240, 100);
            
            EndBatchDraw();
        }
        
        return 0;
    }
    ```
    
    ```cpp title="迁移成 HiEasyX 后的代码"
    #include "HiEasyX.h"
    
    int main()
    {
        initgraph();
        
        while(1)
        {
            BEGIN_TASK();
            
            circle(320, 240, 100);
            
            END_TASK();
            FLUSH_DRAW();
        }
        
        return 0;
    }
    ```

=== "示例二"

    ```cpp title="使用 EasyX 时的代码"
    #include <easyx.h>
    
    int main()
    {
        initgraph();
        
        BeginBatchDraw();
        for(int i = 1; i <= 100; i++)
        {
            circle(i, 240, 100);
            FlushBatchDraw();
        }
        EndBatchDraw();
        
        return 0;
    }
    ```
    
    ```cpp title="迁移成 HiEasyX 后的代码"
    #include "HiEasyX.h"
    
    int main()
    {
        initgraph();
        
        for(int i = 1; i <= 100; i++)
        {
            circle(i, 240, 100);
            FLUSH_DRAW();
        }
        
        return 0;
    }
    ```