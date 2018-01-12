---
title: '[earn money by js] 靠着JavaScript赚钱系列19-yeild'
date: 2117-11-26 23:59:41
tags: ['earn-money', 'JavaScript']
---
yeild


{% codeblock %}
<script>
function *foo(x) {
    var y = 2 * (yield (x + 1));
    var z = yield (y / 3);
    return (x + y + z);
}

var it = foo( 5 );

// note: not sending anything into `next()` here
console.log( it.next() );       // { value:6, done:false }
console.log( it.next( 12 ) );   // { value:8, done:false }
console.log( it.next( 13 ) );   // { value:42, done:true }
</script>
{% endcodeblock %}

var it = foo( 5 ); 
我们在初始化的时候：传入参数x到我们的foo函数中，就像普通函数那样做一样，使得：x=5

console.log( it.next() ); 
第一个it.next()被调用的时候，我们什么都没有传，这是因为没有yeild函数去接受我们的传入的参数 即便是你传入一个从参数到第一个next，该参数会被忽略
在foo函数中，yield (x + 1) 执行 暂停 传出值：6 done:false
--个人理解：这里的yeild应该是已经上一个暂停的yeild，程序一开始运行，没有所谓的暂停的说法 那么参数的说话就无所谓了

console.log( it.next( 12 ) );
当第二个it.next( 12 )被执行的时候，会把参数12放到我们上一次暂停的地方
var y = 2 * (yield (x + 1)); ==> var y = 2 * (12); ==> y = 24
程序继续运行到yield (y / 3) 程序暂停 传出值：8 done:false

console.log( it.next( 13 ) );
当第三个it.next( 13 )被执行的时候，会把参数12放到我们上一次暂停的地方
var z = yield (y / 3); ==> var z = 13;
程序继续运行到return (x + y + z) = 42 传出值：42 done:true


上面所述是按照参考资料中一段进行翻译 如果将这一段看懂 我想yield也就没有任何问题了
参考资料
https://davidwalsh.name/es6-generators

 以上是当年学习koa的时候 见过最好的翻译了 特地分享出来

----------------
不得用于商业用途 转载需注明出处

