## meta 标签的作用

meta 标签由 name 和 content 两部分组成，用来描述HTML网页的属性。

用来定义网页的元数据，可以规定网页以那种方式渲染，搜索引擎优化，或者其他 web 服务

## 主要属性介绍

官方规定的属性有三个 

- name
- http-equiv
- scheme 

scheme 是控制如何解析 content 的内容。

其中，name 和 http-equiv 必须和 content 搭配使用。

name 最常用的是 keywords 值，content 指定 keywords 的值
`<meta name='keywords' content='JS'>`

可以将 上述标签理解为 `{keywords: 'JS'}`。

http-equiv 用来指定当服务器发送给浏览器html 资源时添加额外的自定义头信息

常用的如下：

`<meta http-equiv="charset" content="iso-8859-1">`
`<meta http-equiv="expires" content="31 Dec 2008">`

```
content-type: text/html
charset:iso-8859-1
expires:31 Dec 2008
```
这里可以根据需要任意指定想要的请求头信息。但是尽量是有用的

可以在 meta 标签上任意指定属性和值。如果机器能读懂，就会读取。

`<meta charset='utf-'8 />` 表示使用哪种编码格式解析文档。这个标签只能有一个属性，不然会乱码

## 常用的 meta 标签

### SEO 优化

```

<!-- 页面关键词 keywords -->
<meta name="keywords" content="your keywords">
<!-- 页面描述内容 description -->
<meta name="description" content="your description">
<!-- 定义网页作者 author -->
<meta name="author" content="author,email address">
<!-- 定义网页搜索引擎索引方式，robotterms 是一组使用英文逗号「,」分割的值，通常有如下几种取值：none，noindex，nofollow，all，index和follow。 -->
<meta name="robots" content="index,follow">
```

### viewport

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

参数的定义如下：

- width viewport 宽度(数值/device-width)
- height viewport 高度(数值/device-height)
- initial-scale 初始缩放比例
- maximum-scale 最大缩放比例
- minimum-scale 最小缩放比例
- user-scalable 是否允许用户缩放(yes/no)


### 更多

更多的常用标签参考[这里](https://blog.csdn.net/weixin_37657720/article/details/80548223)