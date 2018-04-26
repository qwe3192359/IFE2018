### 过渡

#### transition（缩写方式）
##### 语法
* transition：[ none | <single-transition-property> ] || <time> || <single-transition-timing-function> || <time>
##### 取值
* transition-property：检索或设置对象中的参与过渡的属性
* transition-duration：检索或设置对象过渡的持续时间
* transition-timing-function：检索或设置对象中过渡的动画类型
* transition-delay：检索或设置对象延迟过渡的时间
##### 说明
* 注意：如果只提供一个<time>参数，则为 <' transition-duration '> 的值定义；如果提供二个<time>参数，
    则第一个为 <' transition-duration '> 的值定义，第二个为 <' transition-delay '> 的值定义
* 同一元素设置多个属性过渡效果用逗号隔开
```
transition:
		border-color .5s ease-in .1s,
		background-color .5s ease-in .1s,
		color .5s ease-in .1s;
```

#### transition-property
##### 语法
* transition-property：none | all | <IDENT>
##### 默认值
* all
##### 取值
* none：不指定过渡的css属性
* all：所有可以进行过渡的css属性
* <IDENT>：指定要进行过渡的css属性
##### 说明
* 默认值为：all。默认为所有可以进行过渡的css属性。
* 如果提供多个属性值，以逗号进行分隔。

#### transition-duration
##### 语法
* transition-duration：<time>
##### 默认值
* 0
##### 取值
* ms
* s
##### 说明
* 取值为时间单位
* 如果提供多个属性值，以逗号进行分隔

#### transition-timing-function
##### 语法
* transition-duration：<IDENT>
##### 默认值
* ease
##### 取值
* linear：线性过渡。等同于贝塞尔曲线(0.0, 0.0, 1.0, 1.0)
* ease：平滑过渡。等同于贝塞尔曲线(0.25, 0.1, 0.25, 1.0)
* ease-in：由慢到快。等同于贝塞尔曲线(0.42, 0, 1.0, 1.0)
* ease-out：由快到慢。等同于贝塞尔曲线(0, 0, 0.58, 1.0)
* ease-in-out：由慢到快再到慢。等同于贝塞尔曲线(0.42, 0, 0.58, 1.0)
* step-start：等同于 steps(1, start)
* step-end：等同于 steps(1, end)
* steps(<integer>[, [ start | end ] ]?)：接受两个参数的步进函数。第一个参数必须为正整数，
    指定函数的步数。第二个参数取值可以是start或end，指定每一步的值发生变化的时间点。第二个参数是
    可选的，默认值为end。类似于动画的帧
* cubic-bezier(x1, y1, x2, y2)：特定的贝塞尔曲线类型，4个数值需在[0, 1]区间内
##### 说明
* 如果提供多个属性值，以逗号进行分隔

#### transition-delay
* 同transition-duration