---
title: '[earn money by js] 靠着JavaScript赚钱系列8'
date: 2117-11-26 23:59:52
tags: ['earn-money', 'JavaScript']
---
300秒延迟

在移动端 我们为了增加用户体验 放弃click事件 转而直接利用touchstart事件
目的就是为了减少用户响应事件

一般情况下 不会有任何问题
但是当界面上的元素因为我们的touch事件改变了 就会产生一些不必要的问题
页面跳转 遮罩层消失等等 
那么touch之后才开始作用的click事件就会导致一些问题


个人写的一个demo 模拟了整个过程

<div style="width:300px">
![300delay](/1008-earn-money-by-js/300delay1.jpg)
</div>

点击button相同位置的遮罩层 在控制台显示出了同时触发了button的click事件

<div style="width:300px">
![300delay](/1008-earn-money-by-js/300delay2.jpg)
</div>

其中关键的js代码如下
{% codeblock %}
<script> 
	layer.addEventListener("touchstart", function(e) {
	  console.log("layer touchstart-->" + (new Date().getTime()));
	  body.removeChild(layer);
	});

	testButton.addEventListener("click", function(e) {
	  console.log("test-button click-->" + (new Date().getTime()));
	});
</script>
{% endcodeblock %}
当点击遮罩层 让遮罩层消失 就有可能同时出发button事件

如果想要避免 在代码里添加 e.preventDefault();

{% codeblock %}
<script> 
	layer.addEventListener("touchstart", function(e) {
	  console.log("layer touchstart-->" + (new Date().getTime()));
	  body.removeChild(layer);
	  e.preventDefault();
	});
</script>
{% endcodeblock %}

以上就是个人理解的300秒延迟

demo地址
https://zhouweihua.github.io/example/300delay.html

----------------
不得用于商业用途 转载需注明出处

