# HTML XHTML 和 XML 的区别

- HTML(超文本标记语言)：用于书写页面结构，但是在 HTML4.0 之前都是现有实现再有规范，导致整个HTML非常松散和不规范
- XML(可扩展标记语言)：主要用于数据传入，作用和 `JSON` 类似，但是没有 `JSON` 轻量和高效。所以现在使用不如 `JSON` 广泛。
- XHTML(可扩展超文本标记语言)：基于上面的两种语言而来，主要是**为了解决 HTML 的混乱状态而设计的**。HTML5 就是基于此产生，在文档开头加了 `<!DOCTYPE html>` 就会以标准方式渲染，否则以混乱模式渲染


# HTML5 和 HTML4 的区别

- HTML5 的稳定类型只有一种 `<!DOCTYPE html>`
- HTML5 不在基于SGML而是基于 XHTML
- 新的元素：section, video, progress, nav, meter, time, aside, canvas, command, datalist, details, embed,
figcaption, figure, footer, header, hgroup, keygen, mark, output, rp, rt, ruby, source, summary, wbr。
- input元素的新类型：date, email, url等等。
- 新的属性：ping（⽤于a与area）, charset（⽤于meta）, async（⽤于script）。
- 全域属性：id, tabindex, repeat。
- 新的全域属性：contenteditable, contextmenu, draggable, dropzone, hidden, spellcheck。
- 移除元素：acronym, applet, basefont, big, center, dir, font, frame, frameset, isindex, noframes, strike, tt


# 对 HTML5 标签语义化的理解

> 语义化值的是使用合适的 HTML 去组织页面，让页面具有良好的结构和含义。比如 `<p>`代表段落，`<article>` 代表正文等。

## 语义化带来的好处有以下几点

- 对开发者而言：使用语义类标签增强了可读性，开发者能够清晰的看出页面结构，便于团队维护和开发
- 对机器而言：带有语义化的标签表现丰富，便于爬虫和搜索引擎获取有效信息。语义化还支持读屏软件根据文章内容列出大纲等。

- 这对于简书、知乎这种富⽂本类的应⽤很重要，语义化对于其⽹站的内容传播有很⼤的帮助，
- 但是对于功能性的web软件重要性⼤打折扣，⽐如⼀个按钮、Skeleton这种组件根本没有对应的语义（不能突出重点），也不需要什么SEO。