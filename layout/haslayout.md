# haslayout(ie 渲染引擎)
---
## 什么是haslayout
haslayout是Windows Internet Explorer渲染引擎的一个内部组成部分。在Internet Explorer中，使用布局概念来控制元素的尺寸和定位。在理想情况下，所有元素都控制自己的尺寸和定位。但是，这在IE中会导致很大的性能问题。因此，IE开发团队决定只将布局应用于实际需要它的那些元素，这样就可以充分地减少性能开销。

拥有布局(have layout)的元素负责本身及其子元素的尺寸和定位。如果一个元素没有布局，那么它的尺寸和位置由最近的拥有布局的祖先元素控制。IE显示引擎利用布局概念减少它的处理开销。一个元素要么自己对自身的内容进行计算大小和组织，要么依赖于父元素来计算尺寸和组织内容。

为了调节这两个不同的概念，渲染引擎采用了hasLayout的属性，属性值可以为true或false。当一个元素的 hasLayout属性值为true时，我们说这个元素有一个布局（layout），当一个元素有一个布局时，它负责对自己和可能的子孙元素进行尺寸计算和定位。简单来说，这意味着这个元素需要花更多的代价来维护自身和里面的内容，而不是依赖于祖先元素来完成这些工作。因此，一些元素默认会有一个布局。当我们说一个元素“拥有layout”或“得到layout”，或者说一个元素“has layout”的时候，我们的意思是指它的微软专有属性 hasLayout 被设为了true 。一个“layout元素”可以是一个默认就拥有layout的元素或者是一个通过设置某些CSS属性得到layout 的元素。如果某个HTML元素拥有haslayout属性，那么这个元素的 haslayout的值一定只有true，haslayout为只读属性一旦被触发，就不可逆转。通过IE Developer Toolbar可以查看IE下HTML元素是否拥有haslayout，在IE Developer Toolbar下，拥有haslayout的元素，通常显示为“haslayout = -1”。

## 默认拥有haslayout属性
```html
<html>, <body>
<table>, <tr>, <th>, <td>
<img>
<hr>
<input>, <button>, <select>, <textarea>, <fieldset>, <legend>
<iframe>, <embed>, <object>, <applet>
<marquee>
```

## 触发haslayout属性

很多情况下，我们把 hasLayout的状态改成true 就可以解决很大部分ie下显示的bug。
hasLayout属性不能直接设定，你只能通过设定一些特定的css属性来触发并改变 hasLayout 状态。下面列出可以触发hasLayout的一些CSS属性值。

#### display
启动haslayout的值:inline-block
取消hasLayout的值:其他值

#### width/height
启动hasLayout的值：除了auto以外的值
取消hasLayout的值：auto
 ( 对 IE6 及更早版本来说很常用，该方法被称为霍莉破解(Holly hack)，即设定这个元素的高度为 1% (height:1%;)。但是要注意，当这个元素的 overflow 属性被设置为 visible 时，这个方法就失效了。)

#### position
启动hasLayout的值：absolute
取消hasLayout的值：static

#### float
启动hasLayout的值：left或right
取消hasLayout的值：none

#### zoom
启动hasLayout的值：有值
取消hasLayout的值：narmal或者空值
(又一个ie私有属性，不兼容标准。)

ie7还有一些额外的属性可以触发该属性（不完全列表）：
min-height: (任何值)
max-height: (任何值除了none)
min-width: (任何值)
max-width: (任何值除了none)
overflow: (任何值除了visible)
overflow-x: (任何值除了visible)
overflow-y: (任何值除了visible)
position: fixed

## 发现及使用

因元素hasLayout而导致的问题其实一般都很容易发现：往往是内容出现错位甚至完全不可见，比如含浮动或者绝对定位子元素的容器高度会塌陷，在ie6/ie7下我们为其添加zoom：1属性就触发了haslayout，从而修复高度塌陷的问题;再比如，我们经常会碰到ie6和ie7同时出现的bug，这个时候可以考虑是否源于 haslayout，可以添加一些可以触发haslayout的属性来解决。
