---
title: '[earn money by js] 靠着JavaScript赚钱系列6'
date: 2117-11-26 23:23:23
tags: ['earn-money', 'JavaScript']
---
<font size="4" color="#000">关于forEach等循环操作的一些警示</font> 

不管是写任何语言 在针对循环操作的过程中 我们有时将寻找的逻辑以及处理的逻辑放在一起 往往造成一些隐藏比较深的bug

特别是是针对数组的增删操作的时候
{% codeblock %}
<script> 
datas.forEach(function (item,i) {
	if (isTrue()) {
		// add
	} else {
		// delete
	}
})
</script>
{% endcodeblock %}

最好将代码拆开来写 防止错误出现
{% codeblock %}
<script> 
var addFlag = -1
var delFlag = -1
datas.forEach(function (item,i) {
	if (isTrue()) {
		// add
		addFlag = i
	} else {
		// delete
		delFlag = i
	}
})

if (addFlag > -1) {
	// add
}
if (delFlag > -1) {
	// delete
}
</script>
{% endcodeblock %}

----------------
还要多说一句

针对数组操作 最好是从后向前寻找 这样就确保我们数组每一个元素都可以被触及一遍 而从前向后往往会有错乱的问题

----------------
不得用于商业用途 转载需注明出处

