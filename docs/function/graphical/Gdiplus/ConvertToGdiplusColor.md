---
comments: true
---

# ConvertToGdiplusColor
函数 · 位于 HiGdiplus.cpp 中第 30 行

### 函数模型

```cpp
Gdiplus::Color HiEasyX::ConvertToGdiplusColor(COLORREF color,
		                                      bool reserve_alpha = false);
```

### 作用
转换 COLORREF 到 Gdiplus::Color

### 说明
#### 参数
- `color`：原颜色

- `reserve_alpha`：是否保留 COLORREF 中的 alpha 值

#### 返回值
无

#### 示例
无