# Window::Create
函数 · 位于 HiWindow.cpp 第 1553 行

### 函数模型

```cpp
HWND HiEasyX::Window::Create(int     w = 640,
		                     int  	 h = 480,
		                     int  	 flag = EW_NORMAL,
		                     LPCTSTR lpszWndTitle = L"",
		                     WNDPROC WindowProcess = nullptr,
		                     HWND  	 hParent = nullptr 
		                    ) 	
```

### 作用

等价于 InitWindow

### 说明

=== "示例一"
    创建一个 640,480的窗口
    ```cpp
    hiex::Window wnd;
    wnd.Create(640, 480);
    ```
    
=== "示例二"
    创建一个 640,480的窗口
    ```cpp
    hiex::Window wnd(640, 480);
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