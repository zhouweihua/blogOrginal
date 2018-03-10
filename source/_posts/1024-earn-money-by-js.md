---
title: '[earn money by js] 靠着JavaScript赚钱系列24-简化版vuex'
date: 2117-11-26 23:59:36
tags: ['earn-money', 'JavaScript']
---
vuex源码分析

vuex的基本代码 大部分功能属于辅助性质 

在通过简化操作之后 你就会发现 vuex真正核心的代码只有那么几句

话不多少 请看代码


{% codeblock %}
	import Vue from 'vue';
	 
	function Store(options) {

	  var state = {
	    a: 'a',
	  }

	  this.setA = function (para) {
	    this.state.a. = para
	  }

	  this._vm = new Vue({
	    data: {
	      $$state: state
	    }
	  });
	}


	var prototypeAccessors = {
	  state: {}
	};
	prototypeAccessors.state.get = function () {
	  return this._vm._data.$$state
	};
	Object.defineProperties(Store.prototype, prototypeAccessors);

	export default new Store()

{% endcodeblock %}

这个精简版的代码没有所谓的action mutation commit 比较简单粗暴 ~_~

----------------
网页看不清可以下载下来看

----------------
不得用于商业用途 转载需注明出处

