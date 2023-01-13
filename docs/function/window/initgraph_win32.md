---
comments: true
---

# initgraph_win32
函数 · 位于 HiWindow.cpp 中第 1630 行

### 函数模型

```cpp
HWND HiEasyX::initgraph_win32(int	  w = 640,
							  int	  h = 480,
							  int	  flag = EW_NORMAL,
							  LPCTSTR lpszWndTitle = L"",
							  WNDPROC WindowProcess = nullptr,
							  HWND	  hParent = nullptr);
```

### 作用
创建一个 Win32 绘图窗口（异于原生 EasyX 窗口）

### 说明
#### 参数
- `w`：绘图窗口的宽度。

- `h`：绘图窗口的高度。

- `flag`：窗口样式（EW_ 系列宏，默认为 EW_NORMAL）。可为以下值：

| 值             | 含义                      | 
| :------------- | :----------------------- |
| `EX_DBLCLKS`     | 在绘图窗口中支持鼠标双击事件。 |
| `EX_NOMINIMIZE`  | 禁用绘图窗口的最小化按钮。    |
| `EX_SHOWCONSOLE` | 显示控制台窗口。            |

- `lpszWndTitle`：窗口标题

- `WindowProcess`：窗口过程函数

- `hParent`：父窗口句柄 

#### 返回值
返回新建绘图窗口的句柄。

!!! bug "BUG"
    不建议大批量创建绘图窗口，如果必要，请适当添加延时，否则可能导致未知问题。

#### 说明
!!! note "`initgraph` 函数 与 `initgraph_win32` 函数的区别"

    `initgraph`：当所有程序窗口被关闭后，程序会自动退出（结束进程）

	`initgraph_win32`：当所有程序窗口被关闭后，程序 **不会** 退出（结束进程）

#### 窗口过程函数规范

##### 函数签名
```cpp
LRESULT CALLBACK WndProc(HWND hWnd, UINT msg, WPARAM wParam, LPARAM lParam);
```

##### 注意事项
若要以默认方式处理消息，则返回 `HIWINDOW_DEFAULT_PROC` 即可（不要使用 `DefWindowProc` 函数）

##### 示例函数
```cpp
LRESULT CALLBACK WndProc(HWND hWnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch (msg)
    {
    case WM_PAINT:
        BEGIN_TASK_WND(hWnd);
        circle(100, 100, 70);
        END_TASK();
        break;
 
    case WM_CLOSE:
        DestroyWindow(hWnd);
        break;
 
    case WM_DESTROY:
        // TODO: 在此处释放申请的内存
        PostQuitMessage(0);
        break;
 
    default:
        return HIWINDOW_DEFAULT_PROC;   // 标识使用默认消息处理函数继续处理
 
        // 若要以默认方式处理，请勿使用此语句
        //return DefWindowProc(hWnd, msg, wParam, lParam);
        break;
    }
 
    return 0;
}
```