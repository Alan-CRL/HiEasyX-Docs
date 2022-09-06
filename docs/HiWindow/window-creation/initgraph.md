# initgraph
宏定义 · 位于 HiWindow.h 第 729 行

### 宏定义内容

```cpp
HiEasyX::initgraph_win32(__VA_ARGS__);HiEasyX::AutoExit()
```

### 作用

创建 Win32 绘图窗口

### 说明

此函数使用 [initgraph_win32](initgraph_win32.md) 创建了一个指定大小的窗口

并设置了 [AutoExit]()，即关闭所有窗口后自动推出程序。

??? bug "正在调查的漏洞"
    在程序中使用 多线程 后，在 `AutoExit()` 中可能出现 `exit` 失败的问题，导致程序无法退出。
    
    如果您出现了此问题，请将 `AutoExit()` 中的 `exit(0);` 替换成 `abort();`（强制退出程序）即可。
    
    推断：此问题可能发生在 Windows 11 或特定的编译环境下。

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