---
title: '[earn money by js] 靠着JavaScript赚钱系列15-关联对象方法'
date: 2117-11-26 23:59:45
tags: ['earn-money', 'JavaScript']
---
如何关联一个对象上的方法到另一个对象上去

<font size="4" color="#000">方法1： Object.defineProperty</font>

{% codeblock %}
<script>
function proxy (target, sourceKey, key) {
  sharedPropertyDefinition.get = function proxyGetter () {
    return this[sourceKey][key]
  };
  sharedPropertyDefinition.set = function proxySetter (val) {
    this[sourceKey][key] = val;
  };
  Object.defineProperty(target, key, sharedPropertyDefinition);
}
</script>
{% endcodeblock %}


<font size="4" color="#000">方法2：bind</font>
{% codeblock %}
<script>
function bind(fn, thisArg) {
  return function() {
    return fn.apply(thisArg, Array.prototype.slice.call(arguments));
  };
}
</script>
{% endcodeblock %}


----------------
不得用于商业用途 转载需注明出处

