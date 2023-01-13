---
comments: true
search:
  exclude: true
---

# HiEasyX 绘图函数库简介

HiEasyX 是 Windows 平台下的简易绘图库，是面向 C++ 语言的绘图库。

HiEasyX 绘图库基于 EasyX、GDI+ 等项目，是由 Visual Studio 构建的开源绘图库。

---

通俗来讲，HiEasyX 更像是 EasyX 的升级，让 EasyX 有更多更完美的功能。

HiEasyX 非常适用于新手，无需强大的学习力，即可轻松驾驭。

---

HiEasyX 只有一个目的： **让 EasyX 更易用**

## 适用环境

HiEasyX 需要支持 MSVC 为编译环境的 IDE，需要 C++11 及其以上版本。

HiEasyX 要求设置项目字符集为 Unicode。

## 概念

HiEasyX 是基于 EasyX 的扩展库，支持创建多窗口、透明抗锯齿绘图、系统 UI 组件等等。

HiEasyX 和 EasyX 的契合度很高，所以，在掌握 EasyX 的基础上使用 HiEasyX 是很容易的。

## 命名空间

HiEasyX 在代码中使用 `HiEasyX` 命名空间，缩写 `hiex`，兼容旧版命名空间 `EasyWin32`。

## 库全局设置

在 HiDef.h 中有控制库全局设置的宏定义，可以自行参阅并设置，此处不展开。