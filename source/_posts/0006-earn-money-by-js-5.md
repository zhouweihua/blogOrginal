---
title: '[earn money by js] 靠着JavaScript赚钱系列5'
date: 2117-11-26 23:59:55
tags: ['earn-money', 'JavaScript']
---
<font size="4" color="#000">img跨域发送请求 代码</font> 

在学习跨域的过程中 很多博客只是提供简单的说明 没有实际的代码

你可以这样写
{% codeblock %}
<script>
var url = "xx/tongjijiekou?xx=xx"; // xx/tongjijiekou 为统计接口
//发送统计数据
var img = new Image(1, 1);
img.src = url
</script>
{% endcodeblock %}

直接这样写 就能发送统计请求了


----------------
不得用于商业用途 转载需注明出处