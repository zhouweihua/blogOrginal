---
title: '[earn money by js] 靠着JavaScript赚钱系列9-相关事件阻止函数'
date: 2117-11-26 23:59:51
tags: ['earn-money', 'JavaScript']
---
stopImmediatePropagation & stopPropagation & preventDefault & return false & cancelBubble

<font size="4" color="#000">preventDefault</font>
阻止了默认事件

<font size="4" color="#000">stopPropagation</font>
阻止了冒泡事件

<font size="4" color="#000">stopImmediatePropagation</font>
阻止了冒泡 同时平级事件也被阻止了 默认事件没有被阻止

<font size="4" color="#000">return false</font>
没有传说中的全部阻止的效果 这一点或许要大家自己测了才知道

<font size="4" color="#ccc">cancelBubble</font>
事实上stoppropagation和cancelBubble的作用是一样的，都是用来阻止浏览器默认的事件冒泡行为。
一般很少人用

demo地址
https://zhouweihua.github.io/example/event.html

参考资料
http://www.cnblogs.com/dannyxie/p/5642727.html

----------------

事件冒泡和事件捕获
如果你想要做的是和冒泡正好相反的操作 请记住 还有<font color="red">事件捕获</font>操作

demo地址
https://zhouweihua.github.io/example/eventPopGet.html

----------------
不得用于商业用途 转载需注明出处
