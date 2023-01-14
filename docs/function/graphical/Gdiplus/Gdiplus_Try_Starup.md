---
comments: true
---

# Gdiplus_Try_Starup
函数 · 位于 HiGdiplus.cpp 中第 12 行

### 函数模型

```cpp
void HiEasyX::Gdiplus_Try_Starup();
```

### 作用
启动 Gdiplus(GDI+)，如果已经启动则直接返回

!!! warning "注意"
    注意，必须先启动 Gdiplus(GDI+)，才能使用其他的 Gdiplus(GDI+) 的绘图函数

### 说明
创建第一个绘图窗口时，Gdiplus(GDI+) 会自动开启。

关闭最后一个绘图窗口时，Gdiplus(GDI+) 会自动关闭。