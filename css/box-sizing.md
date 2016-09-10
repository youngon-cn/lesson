# Box-sizing

>The box-sizing property is used to alter the default CSS box model used to calculate width and height of the elements. It is possible to use this property to emulate the behavior of browsers that do not correctly support the CSS box model specification.

为了兼容而使用

box-sizing 属性允许您以特定的方式定义匹配某个区域的特定元素。
box-sizing 属性可以为三个值之一：content-box(default)|border-box|padding-box。

content-box：border和padding不计算入width之内

padding-box：padding计算入width内

border-box：border和padding计算入width之内，其实就是怪异模式了~

ie8+浏览器支持content-box和border-box；

ff则支持全部三个值。
