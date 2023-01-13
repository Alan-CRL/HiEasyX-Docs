---
comments: true
---

# setcliprgn
函数 · 位于 EasyX 库中

### 函数模型

```cpp
void setcliprgn(HRGN hrgn);
```

### 作用
这个函数用于设置当前绘图设备的裁剪区。

### 说明
#### 参数
- `hrgn`：区域的句柄。创建区域所使用的坐标为[物理坐标](../../concept/coordinate.md#_2)。如果该值为 `NULL`，表示取消之前设置的裁剪区。

#### 返回值
无

#### 备注
`HRGN` 是 Windows 定义的表示区域的句柄。将该区域设置为裁剪区后，任何区域外的绘图都将无效（但仍然可以通过操作显示缓冲区在裁剪区外绘图）。

可以使用 Windows GDI 函数创建一个区域。例如，创建矩形区域可以使用函数：
```cpp
HRGN CreateRectRgn(int left, int top, int right, int bottom);
```

此外，还可以使用函数 `CreateEllipticRgn` 创建椭圆形的区域，使用 `CreatePolygonRgn` 创建多边形的区域等等。还可以使用 `CombineRgn` 组合区域。更多关于区域的 GDI 函数，请参考 MSDN 中的 [Region Functions](https://docs.microsoft.com/windows/win32/gdi/region-functions)。

注意：创建区域后，如果不再使用，请执行 `DeleteObject(HRGN hrgn)` 以释放该区域对应的系统资源。

#### 示例
以下代码用于创建一个矩形裁剪区，并在该裁剪区内画圆，请观察裁剪效果：

```cpp
#include <graphics.h>
#include <conio.h>

int main()
{
	// 初始化绘图窗口
	initgraph(640, 480);

	// 创建一个矩形区域
	HRGN rgn = CreateRectRgn(100, 100, 200, 200);
	// 将该矩形区域设置为裁剪区
	setcliprgn(rgn);
	// 不再使用 rgn，清理 rgn 占用的系统资源
	DeleteObject(rgn);

	// 画圆，受裁剪区影响，只显示出四段圆弧
	circle(150, 150, 55);

	// 取消之前设置的裁剪区
	setcliprgn(NULL);

	// 画圆，不再受裁剪区影响，显示出一个完整的圆
	circle(150, 150, 60);

	// 按任意键退出
	_getch();
	closegraph();
}
```