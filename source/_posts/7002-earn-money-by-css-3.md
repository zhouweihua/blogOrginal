---
title: '[earn money by css] 靠着css赚钱系列3'
date: 2116-11-26 23:59:57
tags: ['earn-money', 'css']
---
<font size="4" color="#000">ios中fixed和键盘兼容的问题</font> 
这是一个很常见的问题
![ios fixed问题调研](/7002-earn-money-by-css-3/iosfixed.jpg)

解决思路有两种

1.
将fixed的的元素转化成固定在底部的元素
这种直接干掉fixed做法 属于暴力的做法 一般不要使用

2.
第二种思路就是 键盘事件的触发一般都是input框导致的
在input框中监听focus blur事件
focus触发时 将fixed元素隐藏
blur触发时 将fixed元素显示
目前最好的解决思路就是这个方法


----------------
不得用于商业用途 转载需注明出处