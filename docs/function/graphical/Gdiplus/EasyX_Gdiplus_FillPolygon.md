---
comments: true
---

# EasyX_Gdiplus_FillPolygon
函数 · 位于 HiGdiplus.cpp 中第 317 行

### 函数模型

```cpp
void HiEasyX::EasyX_Gdiplus_FillPolygon(int      points_num,
		                                POINT*   points,
		                                COLORREF linecolor,
		                                COLORREF fillcolor,
		                                float  	 linewidth,
		                                bool  	 enable_alpha,
		                                bool  	 enable_aa,
		                                IMAGE*   pImg);
```

### 作用
画有边框填充多边形

### 说明
#### 参数
- `points_num`：多边形定点数

- `*points`：[PointF 类](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)，PointF 类封装二维坐标系中的点

- `linecolor`：划线颜色

- `fillcolor`：填充颜色

- `linewidth`：划线宽度

- `enable_alpha`：是否启用透明度

- `enable_aa`：是否启用抗锯齿

- `pImg`：绘图设备指针

#### 返回值
无

#### 示例
无