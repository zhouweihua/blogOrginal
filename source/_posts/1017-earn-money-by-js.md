---
title: '[earn money by js] 靠着JavaScript赚钱系列17'
date: 2117-11-26 23:59:43
tags: ['earn-money', 'JavaScript']
---
nginx配置

/nginx/conf/nginx.conf

关于nginx配置只需要知道两点

第一点：知道如果访问资源
1.1 如果nginx和资源文件夹放在同一个目录下
那么访问方法如下
{% codeblock %}
    location /vue {
        alias ../vue;
        index  index.html index.htm;
    }
{% endcodeblock %}

1.2 如果nginx单独在一个地方 统一配置全局所有的网站
那么访问方法如下
{% codeblock %}
    location /vue {
        root "D:\website";
        index  index.html index.htm;
    }
{% endcodeblock %}

第二点：知道如何代理接口
{% codeblock %}

{% endcodeblock %}

----------------
不得用于商业用途 转载需注明出处

