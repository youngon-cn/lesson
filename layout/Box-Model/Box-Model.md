# Box Model 

![Box Model](./Box Model.gif)

- Margin(外边距) - 清除边框外的区域，外边距是透明的。
- Border(边框) - 围绕在内边距和内容外的边框。
- Padding(内边距) - 清除内容周围的区域，内边距是透明的。
- Content(内容) - 盒子的内容，显示文本和图像。

>最终元素的总宽度计算公式是这样的：
总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距

>元素的总高度最终计算公式是这样的：
总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

## CSS Border(边框)
>CSS边框属性允许你指定一个元素边框的样式和颜色。

##### border: (width) (style) (color);

##### border-width : (length);

##### border-style : (style);
- none: 默认无边框
- dotted: dotted:定义一个点线框
- dashed: 定义一个虚线框
- solid: 定义实线边界
- double: 定义两个边界。 两个边界的宽度和border-width的值相同
- groove: 定义3D沟槽边界。效果取决于边界的颜色值
- ridge: 定义3D脊边界。效果取决于边界的颜色值
- inset:定义一个3D的嵌入边框。效果取决于边界的颜色值
- outset: 定义一个3D突出边框。 效果取决于边界的颜色值

##### border-color : (color)
- name - 指定颜色的名称，如 "red"
- RGB - 指定 RGB 值, 如 "rgb(255,0,0)"
- Hex - 指定16进制值, 如 "#ff0000"
