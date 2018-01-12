---
title: '[earn money by css] 靠着css赚钱系列5-垂直居中'
date: 2116-11-26 23:59:55
tags: ['earn-money', 'css']
---
垂直居中

一招鲜 吃遍天

<font size="4" color="#000">方法1： positon</font>
{% codeblock %}
<style>
.test {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translateX(-50%) translateY(-50%);
}
</style> 
{% endcodeblock %}

<font size="4" color="#000">方法2：flex</font>
{% codeblock %}
<style>
.test {
	display: flex;
	justify-content: center;
	align-items: center;
}
</style> 
{% endcodeblock %}

<font size="4" color="#000">方法3： 只针对文字垂直居中</font>
{% codeblock %}
<style>
.test {
	text-align: center;
	line-height: $parent-height;
}
</style> 
{% endcodeblock %}

----------------
不得用于商业用途 转载需注明出处