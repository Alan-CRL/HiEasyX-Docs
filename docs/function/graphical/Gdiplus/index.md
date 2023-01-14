---
comments: true
---

# 函数说明

此文档及下属文档包含 HiEasyX 所封装的 Gdiplus(GDI+) 系列函数

!!! warning "注意"
    务必先使用 `Gdiplus_Try_Starup` 启用 Gdiplus(GDI+) 后，才能使用下列所有函数

## 目录

| 函数 | 说明 |
| :- | :- |
| [`Gdiplus_Try_Starup`](Gdiplus_Try_Starup.md) | 启动 Gdiplus(GDI+) |
| [`Gdiplus_Shutdown`](Gdiplus_Shutdown.md) | 关闭 Gdiplus(GDI+) |
| [`ConvertToGdiplusColor`](ConvertToGdiplusColor.md) | 转换 COLORREF 到 Gdiplus::Color |
| [`EasyX_Gdiplus_Line`](EasyX_Gdiplus_Line.md) | 画直线 |
| [`EasyX_Gdiplus_Polygon`](EasyX_Gdiplus_Polygon.md) | 画多边形 |
| [`EasyX_Gdiplus_SolidPolygon`](EasyX_Gdiplus_SolidPolygon.md) | 画无边框填充多边形 |
| [`EasyX_Gdiplus_FillPolygon`](EasyX_Gdiplus_FillPolygon.md) | 画有边框填充多边形 |
| [`EasyX_Gdiplus_Rectangle`](EasyX_Gdiplus_Rectangle.md) | 画矩形 |
| [`EasyX_Gdiplus_SolidRectangle`](EasyX_Gdiplus_SolidRectangle.md) | 画无边框填充矩形 |
| [`EasyX_Gdiplus_FillRectangle`](EasyX_Gdiplus_FillRectangle.md) | 画有边框填充矩形 |
| [`EasyX_Gdiplus_Ellipse`](EasyX_Gdiplus_Ellipse.md) | 画椭圆 |
| [`EasyX_Gdiplus_SolidEllipse`](EasyX_Gdiplus_SolidEllipse.md) | 画无边框填充椭圆 |
| [`EasyX_Gdiplus_FillEllipse`](EasyX_Gdiplus_FillEllipse.md) | 画有边框填充椭圆 |
| [`EasyX_Gdiplus_Pie`](EasyX_Gdiplus_Pie.md) | 画饼状图（传入逆时针角度） |
| [`EasyX_Gdiplus_SolidPie`](EasyX_Gdiplus_SolidPie.md) | 画无边框填充饼状图（传入逆时针角度） |
| [`EasyX_Gdiplus_FillPie`](EasyX_Gdiplus_FillPie.md) | 画有边框填充饼状图（传入逆时针角度） |
| [`EasyX_Gdiplus_Arc`](EasyX_Gdiplus_Arc.md) | 画圆弧（传入逆时针角度） |
| [`Gdiplus_Line`](Gdiplus_Line.md) | 画直线 |
| [`Gdiplus_Polygon`](Gdiplus_Polygon.md) | 画多边形 |
| [`Gdiplus_SolidPolygon`](Gdiplus_SolidPolygon.md) | 画无边框填充多边形 |
| [`Gdiplus_Rectangle`](Gdiplus_Rectangle.md) | 画矩形 |
| [`Gdiplus_SolidRectangle`](Gdiplus_SolidRectangle.md) | 画无边框填充矩形 |
| [`Gdiplus_Ellipse`](Gdiplus_Ellipse.md) | 画椭圆 |
| [`Gdiplus_SolidEllipse`](Gdiplus_SolidEllipse.md) | 画无边框填充椭圆 |
| ~~[`Gdiplus_Pie`](Gdiplus_Pie.md)~~ | 画饼状图（传入顺时针角度） |
| ~~[`Gdiplus_SolidPie`](Gdiplus_SolidPie.md)~~ | 画无边框填充饼状图（传入顺时针角度） |
| ~~[`Gdiplus_Arc`](Gdiplus_Arc.md)~~ | 画圆弧（传入顺时针角度） |