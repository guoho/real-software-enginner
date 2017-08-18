PHP扩展开发

* 为什么要开发PHP扩展 
* 扩展开发掌握的工具；
* MAC下的扩展开发
* PHP7下的扩展开发；
* 扩展的测试；
* 扩展开发需要的基础知识
* 


### 为什么要开发PHP扩展

PHP能够成功的一个重要原因，便是在于其扩展性，只有需求几乎可以在标准类发行包及PHP扩展库（PECL）中里找到。PHP标准类发行包及PHP扩展库（PECL）包括支持各种数据库、文件、字符串、图形、网络、压缩、XML技术等扩展在内的许多扩展。

但既然PHP已经有这么多的类库与扩展了，你为什么还要编写PHP扩展呢。 有如下几个理由支撑你去进行PHP扩展开发。

1. PHP需要支持一项未支持的技术。通常情况下是一种API接口，如市场上新推出了一种数据库Youbase，非常符合公司的业务需求，但官方没有开发类似PHP接口，故需要进行对接的PHP扩展开发。
2. 项目安全或商业的角度需要把一些逻辑算法写成扩展，以避免知识产权信息泄漏；
3. 性能上的需求：现有的PHP扩展性能上无法满足业务需求，要进行定制化的扩展开发。
4. 现有的PHP扩展有Bug需要进行修复，没有程序是完美的，只要你的业务够复杂总是发现程序有这些或那样的Bug需要你进行修复；
4. 对个人来说，写PHP扩展是自己深入学习PHP的必经之路，作为PHP工程师，你需要会写PHP扩展。



### PHP加密扩展开发中遇到的问题

* C语言字符串长度的问题，strlen函数在计算字符串长度时，是以'\0'来作为结束符进行计算的，但在一些需要进行位移的字符串处理程序中，很容易出现'\0'字符，故在计算这一类字符串时，长度计算总是会有问题；
* AES数据加密是块加密，
* 字符串加密时，密文结果后面几位是随机的，即是随机填充的，需要设置更长的长度来避免随机填充。
* 

**参考书籍：**

1. Extending and embedding php
2. [PHP扩展开发与内核应用](http://www.cunmou.com/phpbook/index.md)

**参考文章：**

2. [http://www.laruence.com/php-internal](http://www.laruence.com/php-internal)
3. [菜鸟学php扩展](http://blog.csdn.net/u011957758/article/details/72234075)
1. [PHP扩展开发--01.编写一个helloWorld扩展](http://www.cnblogs.com/linzhenjie/p/5485512.html)
2. [PHP扩展开发--02.包裹第三方的扩展](http://www.cnblogs.com/linzhenjie/p/5485519.html)
3. [AES加密解密算法的C代码实现](http://blog.csdn.net/langeldep/article/details/6265680)
4. [AES加密的C语言实现](http://www.cnblogs.com/starf/p/3657747.html)
5. [php7扩展开发](http://www.cnblogs.com/djhull/p/5383067.html
)
寸谋首页 


