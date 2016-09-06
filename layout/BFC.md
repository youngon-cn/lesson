# BFC（Block Formatting Context）``块级格式化范围``

>A block formatting context is a part of a visual CSS rendering of a Web page. It is the region in which the layout of block boxes occurs and in which floats interact with each other.

BFC 是CSS渲染网页的一部分浮动元素会形成BFC，浮动元素内部子元素的主要受该浮动元素影响，两个浮动元素之间是互不影响的。

>A block formatting context is created by one of the following:
- the root element or something that contains it
- floats (elements where float is not none)
- absolutely positioned elements (elements where position is  absolute or fixed)
- inline-blocks (elements with display: inline-block)
- table cells (elements with display: table-cell, which is the default for HTML table cells)
- table captions (elements with display: table-caption, which is the default for HTML table captions)
- elements where overflow has a value other than visible
- flex boxes (elements with display: flex or inline-flex)

BFC ``块级格式化范围`` 由一下条件时创建的:

- 根元素或其他包含它的元素 (如HTML标签)
- 浮动 (元素的float不为none
- 绝对定位 (元素的position为absolute或fixed
- 行内块inline-blocks (元素的display为inline-block)
- 表格单元格 (元素的 display: table-cell，HTML表格单元格默认属性)
- 表格标题 (元素的 display: table-caption, HTML表格标题默认属性)
- 元素overflow的值不为 visible的元素
- 弹性盒 flex boxes (元素的 display: flex或 inline-flex)

>将元素设置的overflow设置为hidden，此区域将成为BFC区域，BFC内子元素不能影响到外界元素，会达到清除浮动的效果。如果你将元素的display设置为inline-block，也会有相同效果。
