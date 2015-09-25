**inheritances**
{% extends "../chapter4.md" %}

{% block cuizz %}
mycuizz
{% endblock %}


***
**include**

{% include "../book.json" %}


***

**forexample**

{% for cc in book.cc %}
    {{ cc.name }}
{% endfor %}

**if example** <br>
{% if book.ccnazme %}
    ok
{% else %}
    no ok
{% endif %}

boo1k: {{ book.ccname }}
***

file: {{ file.path }}
file: {{ file.mtime }}

---
***
___
page1:{{ book.page1.age }}


<dl>
<dt>标题</dt>
<dd>内容</dd>
</dl>

<ol>
<li>你好</li>
<li>你好</li>
<li>你好</li>
</ol>

>凡是不以结婚为目的恋爱都是耍流氓！！   

|姓名|年龄|
|----|:----:|
|小崔|32|
|小李|25|
|小曹|18|


hello world welcome to `python` world!!

```
multi-line

highlighting !!!!

```




第一小结

#你好

这里曾经有一个故事

一号文字
==
二号文字
--

straw__加粗__luffy

1. 第一行
2. 第二行
  * 无序第三行
3. 第四行
  *  有序第五行
  1. 有序第六行
  1. 有序第七行



    你好我是你的好朋友


* 你好
    1. zzz
    2. zzz
        * 你好
    1. 你好
        * 你好
        - 最好了
        + 哈哈哈
            

[百度](http://www.baidu.com)


[^2]脚注释[^4]
 
 
 
![百度图片](https://mail.aliyun.com/static/2705906/images/logo.png "其实是阿里")
![其他图片][logo]

[zzzz]:http://www.baidu.com

[logo]:http://img1.cache.netease.com/stock/2015/9/22/2015092209455604808.jpg

