---
comments: true
---

# initgraph
函数 · 位于 HiWindow.h 中第 857 行

### 函数模型

#### 定义
已被 `#define` 宏定义成

```cpp
HiEasyX::initgraph_win32(__VA_ARGS__);HiEasyX::AutoExit()
```

#### 用法

```cpp
HWND initgraph(int width,
	           int height,
	           int flag = NULL);
```

### 作用
创建一个 Win32 绘图窗口（异于原生 EasyX 窗口）

### 说明
#### 参数
- `width` 绘图窗口的宽度。

- `height` 绘图窗口的高度。

- `flag` 窗口样式（EW_ 系列宏，默认为 EW_NORMAL）。可为以下值：

| 值             | 含义                      | 
| :------------- | :----------------------- |
| `EX_DBLCLKS`     | 在绘图窗口中支持鼠标双击事件。 |
| `EX_NOMINIMIZE`  | 禁用绘图窗口的最小化按钮。    |
| `EX_SHOWCONSOLE` | 显示控制台窗口。            |


#### 返回值
返回新建绘图窗口的句柄。

#### 说明
!!! note "`initgraph` 函数 与 `initgraph_win32` 函数的区别"

    `initgraph`：当所有程序窗口被关闭后，程序会自动退出（结束进程）

	`initgraph_win32`：当所有程序窗口被关闭后，程序 **不会** 退出（结束进程）

#### 示例
以下代码片段创建一个尺寸为 640x480 的绘图窗口：
```cpp
initgraph(640, 480);
```

以下代码片段创建一个尺寸为 640x480 的绘图窗口，同时显示控制台窗口：
```cpp
initgraph(640, 480, EX_SHOWCONSOLE);
```

以下代码片段创建一个尺寸为 640x480 的绘图窗口，同时显示控制台窗口，并禁用关闭按钮：
```cpp
initgraph(640, 480, EX_SHOWCONSOLE | EX_NOCLOSE);
```