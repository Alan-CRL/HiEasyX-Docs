---
comments: true
---

# EasyX_Gdiplus_Ellipse
函数 · 位于 HiGdiplus.cpp 中第 389 行

### 函数模型

```cpp
void HiEasyX::EasyX_Gdiplus_Ellipse(float    x,
									float    y,
									float  	 w,
									float  	 h,
									COLORREF linecolor,
									float  	 linewidth,
									bool  	 enable_alpha,
									bool  	 enable_aa,
									IMAGE*   pImg);
```

### 作用
画椭圆

### 说明
#### 参数
- `x`：椭圆的外切矩形的左上角横坐标

- `y`：椭圆的外切矩形的左上角纵坐标

- `w`：椭圆的外切矩形的宽度

- `h`：椭圆的外切矩形的高度

- `linecolor`：划线颜色

- `linewidth`：划线宽度

- `enable_alpha`：是否启用透明度

- `enable_aa`：是否启用抗锯齿

- `pImg`：绘图设备指针

#### 返回值
无

#### 示例
无