---
comments: true
search:
  exclude: true
---

# 颜色
HiEasyX 使用 24bit 真彩色，不支持调色板模式。

## 表示颜色的方法

### 用预定义常量表示颜色

| 常量            | 值          | 颜色 |
| :-              | :-         | :-  |
| `BLACK`         | `0`        | 黑  |
| `BLUE`          | `0xAA0000` | 蓝  |
| `GREEN`         | `0x00AA00` | 绿  |
| `CYAN`          | `0xAAAA00` | 青  |
| `RED`           | `0x0000AA` | 红  |
| `MAGENTA`       | `0xAA00AA` | 紫  |
| `BROWN`         | `0x0055AA` | 棕  |
| `LIGHTGRAY`     | `0xAAAAAA` | 浅灰 |
| `DARKGRAY`      | `0x555555` | 深灰 |
| `LIGHTBLUE`     | `0xFF5555` | 亮蓝 |
| `LIGHTGREEN`    | `0x55FF55` | 亮绿 |
| `LIGHTCYAN`     | `0xFFFF55` | 亮青 |
| `LIGHTRED`      | `0x5555FF` | 亮红 |
| `LIGHTMAGENTA`  | `0xFF55FF` | 亮紫 |
| `YELLOW`        | `0x55FFFF` | 黄  |
| `WHITE`         | `0xFFFFFF` | 白  |
| **以下为 HiEasyX 拓展** |
| `DARKBLUE`      | `RGB(0x00, 0x00, 0x8B)` |  |
| `DARKCYAN`      | `RGB(0x00, 0x8B, 0x8B)` |  |
| `DARKGOLDENROD` | `RGB(0xB8, 0x86, 0x0B)` |  |
| `DARKGREEN`     | `RGB(0x00, 0x64, 0x00)` |  |
| `DARKRED`       | `RGB(0x8B, 0x00, 0x00)` |  |
| `DEEPPINK`      | `RGB(0xFF, 0x14, 0x93)` |  |
| `DEEPSKYBLUE`   | `RGB(0x00, 0xBF, 0xFF)` |  |
| `FORESTGREEN`   | `RGB(0x22, 0x8B, 0x22)` |  |
| `GOLD`          | `RGB(0xFF, 0xD7, 0x00)` |  |
| `GRAY`          | `RGB(0x80, 0x80, 0x80)` |  |
| `GREENYELLOW`   | `RGB(0xAD, 0xFF, 0x2F)` |  |
| `LIGHTPINK`     | `RGB(0xFF, 0xB6, 0xC1)` |  |
| `LIGHTSKYBLUE`  | `RGB(0x87, 0xCE, 0xFA)` |  |
| `LIGHTYELLOW`   | `RGB(0xFF, 0xFF, 0xE0)` |  |
| `DARKYELLOW`    | `RGB(255, 201, 14)`     |  |
| `ORANGE`        | `RGB(0xFF, 0xA5, 0x00)` |  |
| `ORANGERED`     | `RGB(0xFF, 0x45, 0x00)` |  |
| `PINK`          | `RGB(0xFF, 0xC0, 0xCB)` |  |
| `PINKWHITE`     | `RGB(255, 230, 250)`    |  |
| `PURPLE`        | `RGB(0x80, 0x00, 0x80)` |  |
| `SKYBLUE`       | `RGB(0x87, 0xCE, 0xEB)` |  |
| `SNOW`          | `RGB(0xFF, 0xFA, 0xFA)` |  |
| `SPRINGGREEN`   | `RGB(0x00, 0xFF, 0x7F)` |  |
| `STEELBLUE`     | `RGB(0x46, 0x82, 0xB4)` |  |
| `TOMATO`        | `RGB(0xFF, 0x63, 0x47)` |  |
| `WHITESMOKE`                 | `RGB(0xF5, 0xF5, 0xF5)` |  |
| `YELLOWGREEN`                | `RGB(0x9A, 0xCD, 0x32)` |  |
| `CLASSICGRAY`                | `RGB(0xF0, 0xF0, 0xF0)` | Windows 经典灰 |
| `MODERN_BORDER_GRAY`         | `0xADADAD` | 现代边框灰 |
| `MODERN_FILL_GRAY`           | `0xE1E1E1` | 现代填充灰 |
| `MODERN_BORDER_BLUE`         | `0xD77800` | 现代边框蓝 |
| `MODERN_FILL_BLUE`           | `0xFBF1E5` | 现代填充蓝 |
| `MODERN_BORDER_PRESSED_BLUE` | `0x995400` | 现代边框蓝（按下） |
| `MODERN_FILL_PRESSED_BLUE`   | `0xF7E4CC` | 现代填充蓝（按下） |

### 用 16 进制数字表示颜色
16 进制的颜色表示规则为：0xbbggrr (bb=蓝，gg=绿，rr=红)

### 用 RGB 宏合成颜色
详见 RGB。

### 用 HSLtoRGB、HSVtoRGB 转换其他色彩模型到 RGB 颜色
详见 HSLtoRGB、HSVtoRGB。

## 示例
以下是几种设置画线颜色的方法：

``` cpp
setlinecolor(0xff0000);
setlinecolor(BLUE);
setlinecolor(RGB(0, 0, 255));
setlinecolor(HSLtoRGB(240, 1, 0.5));
```