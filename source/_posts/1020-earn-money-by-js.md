---
title: '[earn money by js] 靠着JavaScript赚钱系列20'
date: 2117-11-26 23:59:40
tags: ['earn-money', 'JavaScript']
---
vue源码分析1

从17年6月开始 接触vue源码 时间过得太快

即便是到现在也只能说自己对vue有了一个大概的了解

看源码是一个痛苦的过程 毕竟别人写的 有时候自己身在其中 有时候根本无法知道所传达的含义

不过学到的也很多 现在讲自己所知道的分享出来

这个系列所用的demo是vue自带的TODO 以及vue版本为2.3.3
<div style="width:300px">
![个人微信](/1020-earn-money-by-js/demo.png)
</div>

先看一下 vue代码总体的流程
	-流程 1 Vue$3 
	-流程 2 $mount 由app.js中的app.$mount引发的 
	-流程 3 template解析 
	-流程 4 render函数生成 
	-流程 5 数据执行 挂载 
	-流程 6 mountComponent
	-流程 7 监视所有对象 
	-流程 8 watch的更新函数 
	-流程 9 render：with函数到VNODE 
	-流程 10 返回vnode 
	-流程 11  update：VNODE到实际节点
	-流程 12 __patch__ 
	-流程 14 createElm


完整的流程代码分析图
<div style="width:500px">
![liuchengall](/1020-earn-money-by-js/liuchengall.png)
</div>
----------------
不得用于商业用途 转载需注明出处

