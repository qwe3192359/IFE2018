### 过渡+定位+宽度控制过渡切换效果
定位元素{left:0;}，元素在左侧
定位元素{right:0;}，元素在右侧
定位元素{left:0;right:0;margin:auto;}，元素在中间
通过hover切换left,right,margin可控制元素进出方向，也可以给hover加其他参数控制进出的不同效果
[查看demo](http://qwe3192359.github.io/IFE2018/demo/)
![](http://qwe3192359.github.io/IFE2018/demo/Animation.gif)

```
 <style type="text/css">
        body{
            text-align: center;
        }
        .box{
            width: 100px;
            height: 100px;
            position: relative;
            text-align: center;
            line-height: 100px;
            border: 1px solid #eee;
            display: inline-block;
        }
        .box::after{
            display: inline-block;
            content: '';
            height: 3px;
            background: #e4393c;
            transition: 1s;
            position: absolute;
            bottom: 0;
            width: 0;
        }
        .box:hover::after{
            width: 100%;
        }
        .box1::after{
            left: 0;
        }
        .box2::after{
            right: 0;
        }
        .box2:hover::after{
            left: 0;
        }
        .box3::after{
            right: 0;
            width: 0;
        }
        .box4::after{
            right: 0;
            left: 0;
        }
        .box4:hover::after{
            left: auto;
            right: 0;
        }
        .box5::after{
            left: 0;
            margin: auto;
        }
        .box5:hover::after{
            right: 0;
        }
        .box6::after{
            right: 0;
            margin: auto;
        }
        .box6:hover::after{
            left: 0;
        }
        .box7::after{
            right: 0;
            width: 0;
            margin: auto;
            left: 0;
        }
    </style>

<div class="box box1">左进左出</div>
<div class="box box2">左进右出</div>
<div class="box box3">右进右出</div>
<div class="box box4">右进左出</div>
<div class="box box5">中间进入左出</div>
<div class="box box6">中间进右出</div>
<div class="box box7">中间进中间出</div>

```
