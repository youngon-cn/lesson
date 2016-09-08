# Css Transition

>CSS的transition允许CSS的属性值在一定的时间区间内平滑地过渡。这种效果可以在鼠标单击、获得焦点、被点击或对元素任何改变中触发，并圆滑地以动画效果改变CSS的属性值。

---
## transition主要包含四个属性值:

- `transition-property`: 执行变换的属性 .
- `transition- duration` : 变换延续的时间 .
- `transition-timing-function` : 在延续时间段，变换的速率变化 .
- `transition- delay` : 变换延迟时间 .

---
### transition-property  : `none` ｜ `all` ｜  `[indent]`
>用来指定当元素其中一个属性改变时执行`transition`效果,其主要有以下几个值:`none(没有属性改变)`;`all（所有属性改变）`这个也是其默认值;`indent(元素属性名)`;当其值为`none`时,`transition`马上停止执行,当指定为`all`时,则元素产生任何属性值变化时都将执行`transition`效果,`ident`是可以指定元素的某一个属性值.

#### `ident` 其对应的类型如下:

 - `color :` 通过红,绿,蓝和透明度组件变换(每个数值单独处理),如:`background-color`, `border-color`, `color`, `outline-color`等CSS属性;
 - `length :` 真实的数字-精准的数字, 如: `word-spacing`, `width`, `vertical- align`, `top`, `right`, `bottom`, `left`, `padding`, `outline-width`, `margin`, `min-width`, `min-height`, `max-width`, `max-height`, `line-height`, `height`, `border-width`, `border-spacing`, `background-position等属性`;
 - `percentage :` 真实的数字-百分比数字, 如：`word-spacing`, `width`, `vertical-align`, `top`, `right`, `bottom`, `left`, `min-width`, `min-height`, `max-width`, `max-height`, `line-height`, `height`, `background-position`等属性;
 - `integer :`离散步骤(整个数字), 在真实的数字空间, 以及使用floor()转换为整数时发生, 如: `outline-offset`, `z-index`等属性;
 - `number`真实的(浮点型)数值, 如: `zoom`, `opacity`, `font-weight`等属性;
 - `transform list :` 详情请参阅:[《CSS3 Transform》](./Transform.md);
 - `rectangle :`通过`x`, `y`, `width`和`height`(转为数值)变换, 如:`crop`;
 - `visibility :` 离散步骤, 在`0`到`1`数字范围之内, `0`表示`隐藏`，`1`表示完全`显示`, 如: `visibility`;
 - `shadow :` 作用于`color`, `x`, `y`和`blur`(模糊)属性, 如:`text-shadow`;
 - `gradient :` 通过每次停止时的位置和颜色进行变化。它们必须有相同的类型(放射状的或是线性的)和相同的停止数值以便执行动画, 如: `background-image`;
 - `paint server (SVG) :` 只支持下面的情况: 从`gradient`到`gradient`以及`color`到`color`, 然后工作与上面类似;
 - `space-separated list of above :` 如果列表有相同的项目数值, 则列表每一项按照上面的规则进行变化, 否则无变化;
 - `a shorthand property :` 如果缩写的所有部分都可以实现动画，则会像所有单个属性变化一样变化。
 > *注:* 具体什么CSS属性可以实现transition效果，在W3C官网中列出了所有可以实现transition效果的CSS属性值以及值的类型，大家可以点这里了解详情。这里需要提醒一点是，并不是什么属性改变都为触发transition动作效果，比如页面的自适应宽度，当浏览器改变宽度时，并不会触发transition的效果。但上述表格所示的属性类型改变都会触发一个transition动作效果。

### transition-duration :  `time`
>`transition-duration`是用来指定元素转换过程的持续时间,取值:`<time>`为数值，单位为`s(秒)`,可以作用于所有元素,包括`:before`和`:after`伪元素。其默认值是`0`, 也就是变换时是即时的。

### transition-timing-function : `bezier` ｜ `ease`
>`transition-timing-function`的值允许你根据时间的推进去改变属性值的变换速率, `transition-timing-function`有`6`个可能值:

- `ease :`（逐渐变慢）默认值，`ease`函数等同于贝塞尔曲线`(0.25, 0.1, 0.25, 1.0)`;
- `linear :`（匀速），`linear` 函数等同于贝塞尔曲线`(0.0, 0.0, 1.0, 1.0)`;
- `ease-in :` (加速)，`ease-in` 函数等同于贝塞尔曲线`(0.42, 0, 1.0, 1.0);`
- `ease-out :`（减速），`ease-out` 函数等同于贝塞尔曲线`(0, 0, 0.58, 1.0)`
- `ease-in-out :`（加速然后减速），`ease-in-out` 函数等同于贝塞尔曲线`(0.42, 0, 0.58, 1.0)`;
- `cubic-bezier :`（该值允许你去自定义一个时间曲线）， 特定的`cubic-bezier`曲线。 `(x1, y1, x2, y2)`四个值特定于曲线上点P1和点P2。所有值需在`[0, 1]`区域内，否则无效。

>其是`cubic-bezier`为通过贝赛尔曲线来计算`转换`过程中的属性值，如下曲线所示，通过改变`P1(x1, y1)`和`P2(x2, y2)`的坐标可以改变整个过程的`Output Percentage`。初始默认值为`default`。
