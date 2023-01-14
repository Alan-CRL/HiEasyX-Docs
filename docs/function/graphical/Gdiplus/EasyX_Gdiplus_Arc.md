---
comments: true
---

# EasyX_Gdiplus_Arc
函数 · 位于 HiGdiplus.cpp 中第 509 行

### 函数模型

```cpp
void HiEasyX::EasyX_Gdiplus_Arc(float  	 x,
		                        float  	 y,
		                        float  	 w,
		                        float  	 h,
		                        float  	 stangle,
		                        float  	 endangle,
		                        COLORREF linecolor,
		                        float  	 linewidth,
		                        bool  	 enable_alpha,
		                        bool  	 enable_aa,
		                        IMAGE*   pImg);
```

### 作用
画圆弧（传入逆时针角度）

### 说明
#### 参数
- `x`：圆弧的外切矩形的左上角横坐标

- `y`：圆弧的外切矩形的左上角纵坐标

- `w`：圆弧的外切矩形的宽度

- `h`：圆弧的外切矩形的高度

- `stangle`：指定 x 轴与定义饼状图的弧线起点之间的角度（以度为单位）的实数。正值指定逆时针旋转

- `endangle`：指定定义饼状图的弧的起始点和终点之间的角度（以度为单位）的实数。正值指定逆时针旋转

- `linecolor`：划线颜色

- `linewidth`：划线宽度

- `enable_alpha`：是否启用透明度

- `enable_aa`：是否启用抗锯齿

- `pImg`：绘图设备指针

#### 返回值
无

#### 示例
无