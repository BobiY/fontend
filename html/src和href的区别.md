# SRC 和 HREF 的区别

### src 

- src 指向外部资源，会将请求的资源嵌入到网页请求的位置。（比如图片，js 文件等）
- 在请求，解析这些外部资源时会停止其他资源的下载和解析，直到对应的资源下载，解析完毕


### href

- href指向网络资源的所在位置，用来建立和当前元素或文档之间的链接
- 当浏览器识别到对应的链接时会并行的下载对应资源，不会阻塞网页的解析


### 应用

- js 搭配的是 src，会阻塞页面解析，所以要放到页面底部加载
- link 标签搭配的 href，所以 css 要放在头部加载，它不会阻塞页面的解析过程。而且加载完毕就会和文档合成渲染树。

