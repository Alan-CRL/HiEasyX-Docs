# initgraph_win32
函数 · 位于 HiWindow.cpp 第 1487 行

### 函数模型

```cpp
HWND HiEasyX::initgraph_win32(int     w = 640,
		                      int     h = 480,
		                      int     flag = EW_NORMAL,
		                      LPCTSTR lpszWndTitle = L"",
		                      WNDPROC WindowProcess = nullptr,
		                      HWND    hParent = nullptr 
		                     ) 	
```

### 作用

创建 Win32 绘图窗口 

### 说明

#### 参数
```wiki
[in] w	           窗口宽
[in] h	           窗口高
[in] flag	       窗口样式（EW_ 系列宏，默认为 EW_NORMAL）
[in] lpszWndTitle  窗口标题
[in] WindowProcess 窗口过程函数
[in] hParent	   父窗口句柄 
```

#### 返回值
创建的窗口句柄

#### 告示
!!! note "笔记"
    调用此函数将跳过 EasyX 原生窗口创建的步骤 窗口默认支持双击消息
    
!!! bug "漏洞"
    不建议大批量创建绘图窗口，如果必要，请适当添加延时，否则可能导致未知问题。

#### 窗口过程函数规范
函数签名：
    `LRESULT CALLBACK WndProc(HWND hWnd, UINT msg, WPARAM wParam, LPARAM lParam);`

注意事项：
    若要以默认方式处理消息，则返回 `HIWINDOW_DEFAULT_PROC` 即可（不要使用 `DefWindowProc` 函数）

示例函数：
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

<script src="https://giscus.app/client.js"
    data-repo="Alan-CRL/HiEasyX-Docs"
    data-repo-id="R_kgDOH6UtUA"
    data-category="General"
    data-category-id="DIC_kwDOH6UtUM4CRJQ5"
    data-mapping="url"
    data-strict="0"
    data-reactions-enabled="1"
    data-emit-metadata="0"
    data-input-position="top"
    data-theme="light"
    data-lang="zh-CN"
    crossorigin="anonymous"
    async>
</script>