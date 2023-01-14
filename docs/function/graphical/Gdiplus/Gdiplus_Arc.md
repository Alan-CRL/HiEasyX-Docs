---
comments: true
---

# Gdiplus_Arc
函数 · 位于 HiGdiplus.cpp 中第 216 行

!!! bug "维护"
    此函数出现漏洞，停用维护中，^^==请不要使用！==^^

### 函数模型

```cpp
void HiEasyX::Gdiplus_Arc(HDC 					 hdc,
         		 		  float 				 x,
         		 		  float 				 y,
         		 		  float 				 w,
         		 		  float 				 h,
         		 		  float 				 stangle,
         				  float 				 endangle,
         		 		  Gdiplus::Color 		 linecolor,
         		          float 				 linewidth,
         		          Gdiplus::SmoothingMode smoothing_mode);
```

### 作用
画圆弧（传入顺时针角度）

### 说明
#### 参数
- `hdc`：绘图设备 HDC

- `x`：圆弧的外切矩形的左上角横坐标

- `y`：圆弧的外切矩形的左上角纵坐标

- `w`：圆弧的外切矩形的宽度

- `h`：圆弧的外切矩形的高度

- `stangle`：指定 x 轴与定义饼状图的弧线起点之间的角度（以度为单位）的实数。正值指定顺时针旋转

- `endangle`：指定定义饼状图的弧的起始点和终点之间的角度（以度为单位）的实数。正值指定顺时针旋转

- `linecolor`：划线颜色

- `linewidth`：划线宽度

- `smoothing_mode`：[Gdiplus::SmoothingMode](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplusenums/ne-gdiplusenums-smoothingmode) 类

#### 返回值
无

#### 示例
无