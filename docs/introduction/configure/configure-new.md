---
comments: true
search:
  exclude: true
---

# 新项目配置 HiEasyX 库

本文档适用于 **新建项目或非 EasyX 项目** 配置 HiEasyX 库，如果想迁移 EasyX 项目至 HiEasyX，请单击[此处](configure-transfer.md)

1. 下载仓库到本地
2. 创建一个 Visual Studio C++ 项目，并将项目字符集设置为 `unicode`
3. 复制仓库项目中的 `./HiEasyX/HiEasyX.h` 文件 和 `./HiEasyX/HiEasyX/` 整个文件夹到您的项目目录下
4. 将刚才复制的文件和文件夹加入到您的 Visual Studio 项目中（拖入 Visual Studio 的项目资源管理器即可，或可以手动添加）
5. 编写代码，编译运行

???+ info "温馨提示"

    由于 HiEasyX 源码文件较多，故建议在 Visual Studio 项目资源管理器中创建 HiEasyX   筛选器，将上述文件和文件夹都拖入此筛选器中，这样可以使项目结构更整洁。第一次编译需要编译全部文件，所以耗时较长，后面就不会了。