---
comments: true
---

# Gdiplus_Line
函数 · 位于 HiGdiplus.cpp 中第 40 行

### 函数模型

```cpp
void HiEasyX::Gdiplus_Line(HDC                    hdc,
		                   float                  x1,
		                   float                  y1,
		                   float                  x2,
		                   float                  y2,
		                   Gdiplus::Color         linecolor,
		                   float                  linewidth,
		                   Gdiplus::SmoothingMode smoothing_mode);
```

### 作用
画直线

### 说明
#### 参数
- `hdc`：绘图设备 HDC

- `x1`：绘图起点横坐标

- `y1`：绘图起点纵坐标

- `x2`：绘图终点横坐标

- `y2`：绘图终点纵坐标

- `linecolor`：划线颜色

- `linewidth`：划线宽度

- `smoothing_mode`：[Gdiplus::SmoothingMode](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplusenums/ne-gdiplusenums-smoothingmode) 类

#### 返回值
无

#### 示例
无