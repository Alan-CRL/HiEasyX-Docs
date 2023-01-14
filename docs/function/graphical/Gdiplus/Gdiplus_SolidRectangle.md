---
comments: true
---

# Gdiplus_SolidRectangle
函数 · 位于 HiGdiplus.cpp 中第 115 行

### 函数模型

```cpp
void Gdiplus_SolidRectangle(HDC					   hdc,
							float				   x,
							float				   y,
							float				   w,
							float				   h,
							Gdiplus::Color		   fillcolor,
							Gdiplus::SmoothingMode smoothing_mode);
```

### 作用
画无边框填充矩形

### 说明
#### 参数
- `hdc`：绘图设备 HDC

- `x`：矩形左上角横坐标

- `y`：矩形左上角纵坐标

- `w`：矩形宽度

- `h`：矩形高度

- `fillcolor`：填充颜色

- `smoothing_mode`：[Gdiplus::SmoothingMode](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplusenums/ne-gdiplusenums-smoothingmode) 类

#### 返回值
无

#### 示例
无