---
comments: true
---

# Gdiplus_Polygon
函数 · 位于 HiGdiplus.cpp 中第 60 行

### 函数模型

```cpp
void HiEasyX::Gdiplus_Polygon(HDC					 hdc,
							  int					 points_num,
							  Gdiplus::PointF		 *points,
							  Gdiplus::Color		 linecolor,
							  float					 linewidth,
							  Gdiplus::SmoothingMode smoothing_mode);
```

### 作用
画多边形

### 说明
#### 参数
- `hdc`：绘图设备 HDC

- `points_num`：多边形定点数

- `*points`：[PointF 类](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)，PointF 类封装二维坐标系中的点

- `linecolor`：划线颜色

- `linewidth`：划线宽度

- `smoothing_mode`：[Gdiplus::SmoothingMode](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplusenums/ne-gdiplusenums-smoothingmode) 类

#### 返回值
无

#### 示例
无