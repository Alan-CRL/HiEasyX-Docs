---
comments: true
---

# Gdiplus_SolidPie
函数 · 位于 HiGdiplus.cpp 中第 195 行

!!! bug "维护"
    此函数出现漏洞，停用维护中，^^==请不要使用！==^^

### 函数模型

```cpp
void HiEasyX::Gdiplus_SolidPie(HDC 					  hdc,
					           float 				  x,
					           float 				  y,
					           float 				  w,
					           float 				  h,
					           float 				  stangle,
					           float 				  endangle,
					           Gdiplus::Color 		  fillcolor,
					           Gdiplus::SmoothingMode smoothing_mode);
```

### 作用
画无边框填充饼状图（传入顺时针角度）

### 说明
#### 参数
- `hdc`：绘图设备 HDC

- `x`：饼状图所在椭圆的外切矩形的左上角横坐标

- `y`：饼状图所在椭圆的外切矩形的左上角纵坐标

- `w`：饼状图所在椭圆的外切矩形的宽度

- `h`：饼状图所在椭圆的外切矩形的高度

- `stangle`：指定 x 轴与定义饼状图的弧线起点之间的角度（以度为单位）的实数。正值指定顺时针旋转

- `endangle`：指定定义饼状图的弧的起始点和终点之间的角度（以度为单位）的实数。正值指定顺时针旋转

- `fillcolor`：填充颜色

- `smoothing_mode`：[Gdiplus::SmoothingMode](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplusenums/ne-gdiplusenums-smoothingmode) 类

#### 返回值
无

#### 示例
无