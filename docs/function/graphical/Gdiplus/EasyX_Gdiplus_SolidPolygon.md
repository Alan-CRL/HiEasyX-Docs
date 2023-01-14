---
comments: true
---

# EasyX_Gdiplus_SolidPolygon
函数 · 位于 HiGdiplus.cpp 中第 289 行

### 函数模型

```cpp
void HiEasyX::EasyX_Gdiplus_SolidPolygon(int 	  points_num,
										 POINT*   points,
										 COLORREF fillcolor,
										 bool  	  enable_alpha,
										 bool  	  enable_aa,
										 IMAGE*   pImg);
```

### 作用
画无边框填充多边形

### 说明
#### 参数
- `points_num`：多边形定点数

- `*points`：[PointF 类](https://learn.microsoft.com/zh-cn/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)，PointF 类封装二维坐标系中的点

- `fillcolor`：填充颜色

- `enable_alpha`：是否启用透明度

- `enable_aa`：是否启用抗锯齿

- `pImg`：绘图设备指针

#### 返回值
无

#### 示例
无