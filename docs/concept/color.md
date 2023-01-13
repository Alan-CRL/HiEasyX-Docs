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