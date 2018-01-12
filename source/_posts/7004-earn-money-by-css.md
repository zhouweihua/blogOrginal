---
title: '[earn money by css] 靠着css赚钱系列4-盒子模型'
date: 2116-11-26 23:59:56
tags: ['earn-money', 'css']
---
<font size="4" color="#000">盒子模型</font> 
常常遇到的就是box-sizing属性的设置

(1) content-box：
默认值，可以使设置的宽度和高度值应用到元素的内容框。盒子的width只包含内容。
即总宽度=margin+border+padding+width

(2) border-box：
设置的width值其实是除margin外的border+padding+element的总宽度。盒子的width包含border+padding+内容
即总宽度=margin+width

<font size="4" color="#000">系统默认的是content-box 但是border-box更符合我们人的理解思维</font> 

在写代码的时候：
很多时候是利用百分比去写相关元素
一个很简单的例子就是我们想要一个按钮左右留30px的边距； 然后撑满剩余的部分；

content-box：就需要我们自己去计算相关的值；很不利于写代码
border-box：就可以直接在外层元素上设置padding；那么内层元素width：100%就会自动填充剩余的空间

参考资料：
http://www.cnblogs.com/cchyao/archive/2010/07/12/1775846.html


----------------
不得用于商业用途 转载需注明出处