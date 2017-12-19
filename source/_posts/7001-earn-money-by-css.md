---
title: '[earn money by css] 靠着css赚钱系列2'
date: 2116-11-26 23:59:58
tags: ['earn-money', 'css']
---
平时动态样式加载 往往就是先写好class类 然后动态的控制样式
例如
{% codeblock %}
<style>
.test {
	width:100%;
	height:100%;
}
.test .ios {
	padding-top:20px !important;
}
</style> 
{% endcodeblock %}
在html中直接针对class添加和删除ios类 控制显示逻辑

但是曾经看过第二种写法 那就是
{% codeblock %}
<script>
    if(isIos()){
        $('#mystyle').html('.test{padding-top:20px !important}') ;
    }
</script>
{% endcodeblock %}

见猎心喜 记录了下来 印象深刻

----------------
多说一句

初级选手很容易的一个错误就是
if语句中的
{% codeblock %}
<script>
    if(isIos())
</script>
{% endcodeblock %}
会写成
{% codeblock %}
<script>
    if(isIos)
</script>
{% endcodeblock %}

嘿嘿 你看出哪里不一样了么

----------------
不得用于商业用途 转载需注明出处