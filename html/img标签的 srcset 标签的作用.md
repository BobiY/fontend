# img 标签的 srcset 标签的作用

在使用 img 标签时，不同尺寸屏幕下的相同图片会表现的不同。为了解决这个问题，可以使用 scrset 来指定不同屏幕尺寸下的图片的选取。

## srcset

这个属性可以执行不同宽度下应该选取什么图片。属性的定义格式如下，多个属性用 , 隔开
```
// 属性定义规则为：图片地址 屏幕宽度 像素密度(DPI)  一般指定一个后面的条件即可，不然取并集
<img 
  srcset="a.png 300w, b.png 2x"
/>
```
上面的代码表示，宽度为 300px 时使用 a.png 。当 像素密度为 2 时使用 b.png

## sizes

sizes 属性是搭配 srcset 一起使用的。size 指定媒体查询的尺寸，表明哪些尺寸下应该使用哪些图片。
```
<img 
  srcset="a.png 300w, b.png 2x"
  sizes="(min-width: 320px) 300w, 1200w"
/>
```

上面的代码表示，当屏幕的宽度比 320px 大时适应 a.png。1200px 时使用 b.png

## css image-set()

css image-set() 属性和 img 的 srcset 属性作用一样，只是在 css 对相关的属性进行定义
```
body {
  background-image: image-set( 
          url(../images/pic-1.jpg) 1x, 
          url(../images/pic-2.jpg) 2x, 
          url(../images/pic-3.jpg) 600dpi
        );
}
```
规则的指定和srcset 一样。上述代码，在普通屏幕上用 pic-1。高分屏用 pic-2。对于更高的分辨率的屏幕使用 pic-3