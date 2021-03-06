# 初识CSS

## CSS是什么
- CSS 指层叠样式表 (Cascading Style Sheets)
- 样式定义如何显示 HTML 元素
- 样式通常存储在样式表中
- 把样式添加到 HTML 4.0 中，是为了解决内容与表现分离的问题
- 外部样式表可以极大提高工作效率
- 外部样式表通常存储在 CSS 文件中
- 多个样式定义可层叠为一

### 样式解决了一个很大的问题

>HTML 标签原本被设计为用于定义文档内容，如下实例：
``<h1>``这是一个标题``</h1>``
``<p>``这是一个段落.``</p>``
样式表定义如何显示 HTML 元素，就像 HTML 3.2 的字体标签和颜色属性所起的作用那样。样式通常保存在外部的 .css 文件中。通过仅仅编辑一个简单的 CSS 文档，外部样式表使你有能力同时改变站点中所有页面的布局和外观。
为了解决这个问题，万维网联盟（W3C），这个非营利的标准化联盟，肩负起了 HTML 标准化的使命，并在 HTML 4.0 之外创造出样式（Style）。
当代浏览器都支持 CSS .

## CSS 实例

>CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:
![CSS 规则](../img/cssrules.gif)
选择器通常是您需要改变样式的 HTML 元素。
每条声明由一个属性和一个值组成。
属性（property）是您希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开。
CSS声明总是以分号(;)结束，声明组以大括号({})括起来:

## CSS 注释
>注释是用来解释你的代码，并且可以随意编辑它，浏览器会忽略它。
CSS注释以 ``"/*"`` 开始, 以 ``"*/"`` 结束, 实例如下:
