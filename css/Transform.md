# Css Transform

>`transform` 属性向元素应用 `2D` 或 `3D` 转换。该属性允许我们对元素进行旋转、缩放、移动或倾斜。

### `transform`: `none` | `transform-functions`;
`functions-name` : `rotate` | `scale` | `skew` | `translate` | `matrix`
>`none`:表示不进么变换；``<transform-function>``表示一个或多个变换函数，以空格分开；换句话说就是我们同时对一个元素进行transform的多种属性操作，例如`rotate`、`scale`、`translate`三种，但这里需要提醒大家的，以往我们叠加效果都是用逗号（“`,`”）隔开,但transform中使用多个属性时却需要有空格隔开。大家记住了是空格隔开。
