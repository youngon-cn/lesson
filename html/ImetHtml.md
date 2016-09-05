# 初始Html

## HTML是什么
 - HTML 指的是超文本标记语言: HyperText Markup Language
 - HTML 不是一种编程语言，而是一种标记语言
 - 标记语言是一套标记标签 (markup tag)
 - HTML 指的是超文本标记语言: HyperText Markup Language
 - HTML 使用标记标签来描述网页
 - HTML 文档包含了HTML 标签及文本内容
 - HTML文档也叫做 web 页面

## HTML 标签 (HTML tag)
 - HTML 标签是由尖括号包围的关键词，比如 <html>
 - HTML 标签通常是成对出现的，比如 <b> 和 </b>
 - 标签对中的第一个标签是开始标签，第二个标签是结束标签
 - 开始和结束标签也被称为开放标签和闭合标签

## HTML 结构

- <\html> 与 <\/html> 之间的文本描述网页
- <\body> 与 <\/body> 之间的文本是可见的页面内容
- <\h1> 与 <\/h1> 之间的文本被显示为标题
- <\p> 与 <\/p> 之间的文本被显示为段落

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>页面标题</title>
  </head>
  <body>
    <h1>我的第一个标题</h1>
    <p>我的第一个段落。</p>
  </body>
</html>
```
####  DOCTYPE
><!DOCTYPE> 声明位于文档中的最前面的位置，处于 <html> 标签之前。
<!DOCTYPE> 声明不是一个 HTML 标签；它是用来告知 Web 浏览器页面使用了哪种 HTML 版本。
在 HTML 4.01 中，<!DOCTYPE> 声明需引用 DTD （文档类型声明），因为 HTML 4.01 是基于 SGML （Standard Generalized Markup Language 标准通用标记语言）。DTD 指定了标记语言的规则，确保了浏览器能够正确的渲染内容。
HTML5 不是基于 SGML，因此不要求引用 DTD。
提示：总是给您的 HTML 文档添加 <!DOCTYPE> 声明，确保浏览器能够预先知道文档类型。

简单说就是 选择使用的Html版本
- <!DOCTYPE html> (HTML5)
- <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">(HTML 4.01)


#### head
>元素是所有头部元素的容器

- <\title> 在头部中，这个元素是必需的
- <\style> 标签用于为 HTML 文档定义样式信息-css。
- <\base> 标签为页面上的所有链接规定默认地址或默认目标。
- <\link> 标签定义文档与外部资源的关系。
- <\meta> 提供了 HTML 文档的元数据
- <\script> script 元素既可以包含脚本语句，也可以通过 src 属性指向外部脚本文件。
- <\noscript> 元素用来定义在脚本未被执行时的替代内容（文本）。

#### body
>元素定义了 HTML 文档的主体, 也是浏览器显示的元素
