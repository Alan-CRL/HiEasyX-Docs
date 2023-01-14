---
comments: true
---

# EasyX_Gdiplus_Line
函数 · 位于 HiGdiplus.cpp 中第 238 行

### 函数模型

```cpp
void HiEasyX::EasyX_Gdiplus_Line(float 	  x1,
								 float 	  y1,
								 float 	  x2,
								 float 	  y2,
								 COLORREF linecolor,
								 float 	  linewidth,
								 bool 	  enable_alpha,
								 bool 	  enable_aa,
         						 IMAGE*   pImg);
```

### 作用
画直线

### 说明
#### 参数
- `x1`：绘图起点横坐标

- `y1`：绘图起点纵坐标

- `x2`：绘图终点横坐标

- `y2`：绘图终点纵坐标

- `linecolor`：划线颜色

- `linewidth`：划线宽度

- `enable_alpha`：是否启用透明度

- `enable_aa`：是否启用抗锯齿

- `pImg`：绘图设备指针

#### 返回值
无

#### 示例
无