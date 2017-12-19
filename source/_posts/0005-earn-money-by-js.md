---
title: '[earn money by js] 靠着JavaScript赚钱系列4'
date: 2117-11-26 23:59:56
tags: ['earn-money', 'JavaScript']
---
<font size="4" color="#000">触发事件</font> 

如何主动触发某一个事件

{% codeblock %}
<script>
	var swDom = document.getElementById("sw-done");
	var event = document.createEvent('Events');
	event.initEvent('touchstart', true, true);
	swDom.dispatchEvent(event);
</script>
{% endcodeblock %}

这是通过主动设定事件 然后主动js代码触发事件 非人工触发的一个实例

----------------
多说一句

事件 异步 其实可以简单的理解成事件的回调

也就是利用一个缓冲区存取事件id 执行的时候找到他 并执行

----------------
不得用于商业用途 转载需注明出处