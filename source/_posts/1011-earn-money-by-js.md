---
title: '[earn money by js] 靠着JavaScript赚钱系列11-理解动画一般流程'
date: 2117-11-26 23:59:49
tags: ['earn-money', 'JavaScript']
---
iscroll 拖拽动画的原理

很多人一看到动画就会害怕 特别是一些复杂的动画
其实我也挺怕的
只从深入研究一下 很多动画就显得不是那么可怕了

动画效果 关键的数是3个 transition transform translate

transition设置: 动画的对象; 动画的过程参数; 在一定的时间区间内平滑的过渡；
----transition:property duration timing-function delay;
--------property:CSS的属性，例如：width height 为none时停止所有的运动，可以为transform
--------duration:持续时间
--------timing-function:ease等
--------delay:延迟
--------注意：当property为all的时候所有动画

transform设置: 最终完成的效果
----CSS3中主要包括 旋转：rotate() 顺时针旋转给定的角度，允许负值 rotate(30deg)
--------扭曲：skew() 元素翻转给定的角度,根据给定的水平线（X 轴）和垂直线（Y 轴）参数：skew(30deg,20deg)
--------缩放：scale() 放大或缩小，根据给定的宽度（X 轴）和高度（Y 轴）参数： scale(2,4)
--------移动：translate() 平移，传进 x,y值，代表沿x轴和y轴平移的距离
--------所有的2D转换方法组合在一起： matrix()  旋转、缩放、移动以及倾斜元素
 
translate:移动，<font color="red">transform的一个方法</font>
----注意：它是transform的一个方法 这个就足够了
----用法：el.style.webkitTransform = 'translate3d(0,0,0)';


<font size="4" color="#000">一般代码编写流程就是</font>
在css中设置transition

然后在js中调整transform

我们一般变化就是x y坐标的位置 这个时候用到的就是translate

----------------
不得用于商业用途 转载需注明出处

