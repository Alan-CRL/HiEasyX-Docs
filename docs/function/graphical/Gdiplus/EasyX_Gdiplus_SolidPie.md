---
comments: true
---

# EasyX_Gdiplus_SolidPie
函数 · 位于 HiGdiplus.cpp 中第 469 行

### 函数模型

```cpp
void HiEasyX::EasyX_Gdiplus_SolidPie(float    x,
		                             float    y,
		                             float    w,
		                             float    h,
		                             float    stangle,
		                             float    endangle,
		                             COLORREF fillcolor,
		                             bool  	  enable_alpha,
		                             bool  	  enable_aa,
		                             IMAGE*   pImg);
```

### 作用
画无边框填充饼状图（传入逆时针角度）

### 说明
#### 参数
- `hdc`：绘图设备 HDC

- `x`：饼状图所在椭圆的外切矩形的左上角横坐标

- `y`：饼状图所在椭圆的外切矩形的左上角纵坐标

- `w`：饼状图所在椭圆的外切矩形的宽度

- `h`：饼状图所在椭圆的外切矩形的高度

- `stangle`：指定 x 轴与定义饼状图的弧线起点之间的角度（以度为单位）的实数。正值指定逆时针旋转

- `endangle`：指定定义饼状图的弧的起始点和终点之间的角度（以度为单位）的实数。正值指定逆时针旋转

- `fillcolor`：填充颜色

- `enable_alpha`：是否启用透明度

- `enable_aa`：是否启用抗锯齿

- `pImg`：绘图设备指针

#### 返回值
无

#### 示例
无