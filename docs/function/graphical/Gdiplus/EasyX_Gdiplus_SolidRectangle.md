---
comments: true
---

# EasyX_Gdiplus_SolidRectangle
函数 · 位于 HiGdiplus.cpp 中第 353 行

### 函数模型

```cpp
void HiEasyX::EasyX_Gdiplus_SolidRectangle(float  	x,
										   float  	y,
										   float  	w,
										   float  	h,
										   COLORREF fillcolor,
										   bool  	enable_alpha,
										   bool  	enable_aa,
										   IMAGE*   pImg);
```

### 作用
画无边框填充矩形

### 说明
#### 参数
- `x`：矩形左上角横坐标

- `y`：矩形左上角纵坐标

- `w`：矩形宽度

- `h`：矩形高度

- `fillcolor`：填充颜色

- `enable_alpha`：是否启用透明度

- `enable_aa`：是否启用抗锯齿

- `pImg`：绘图设备指针

#### 返回值
无

#### 示例
无