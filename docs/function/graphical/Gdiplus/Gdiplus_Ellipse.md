---
comments: true
---

# Gdiplus_Rectangle
函数 · 位于 HiGdiplus.cpp 中第 134 行

### 函数模型

```cpp
void HiEasyX::Gdiplus_Ellipse(HDC					 hdc,
							  float					 x,
							  float					 y,
							  float					 w,
							  float					 h,
							  Gdiplus::Color		 linecolor,
							  float					 linewidth,
							  Gdiplus::SmoothingMode smoothing_mode);
```

### 作用
画椭圆

### 说明
#### 参数
- `hdc`：绘图设备 HDC

- `x`：椭圆的外切矩形的左上角横坐标

- `y`：椭圆的外切矩形的左上角纵坐标

- `w`：椭圆的外切矩形的宽度

- `h`：椭圆的外切矩形的高度

- `linecolor`：划线颜色

- `linewidth`：划线宽度

- `smoothing_mode`：[Gdiplus::SmoothingMode](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplusenums/ne-gdiplusenums-smoothingmode) 类

#### 返回值
无

#### 示例
无