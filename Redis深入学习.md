## Redis深入学习
### 一、Redis基本数据类型
Redsi支持多种数据类型

* 字符串
* 队列 List
* HASH
* 集合
* HyperLogLog 用于做基数统计


### 二、Redis与Memcache的区别

* Memcache是纯缓存的服务，而Redis是内存型的数据库，支持多种类型，可以持久化到本地硬盘，更支持事务，性能更好

### 三、Redis的队列实现
* 通过LIST操作即可实现队列
### 四、Redis消息队列
redis可实现最基本的消息订阅及发布，从而实现简单的消息队列服务，满足最基本的异步处理需求

### 五、Redis在秒杀中的使用
* 使用Redis的事务功能，Watch功能实现；
* 使用Redis的队列功能实现秒杀，每个库存一条记录，从而实现秒杀功能；
* 写入内存而不是写入硬盘 
* 异步处理而不是同步处理 
* 分布式Redis Cluster实现秒杀处理 参考文章：[http://blog.csdn.net/shendl/article/details/51092916](http://blog.csdn.net/shendl/article/details/51092916)
* 
### 六、Redis的持久化

* RDB持久化方式能够在指定的时间间隔能对你的数据进行快照存储.
* AOF持久化方式记录每次对服务器写的操作,当服务器重启的时候会重新执行这些命令来恢复原始的数据

### 七、Redis数据同步至MySQL
这个需要通过程序或中间件来实现，而不能通过Redis本身实现
### 八、Redis长连接与连接池
对于Redis服务，通常我们推荐用户使用长连接来访问Redis，但是由于某些用户在连接池失效的时候还是会建立大量的短连接或者用户由于客户端限制还是只能使用短连接来访问Redis，而原生的Redis在频繁建立短连接的时候有一定性能损耗，本文从源码角度对Redis短连接的性能进行了优化
参考文章： https://yq.aliyun.com/articles/62593
### 九、Redis高级应用


* 使用Redis bitmaps进行快速、简单、实时统计

### 十、Redis参考学习资料

* 官网：https://redis.io/
* 中文社区：http://www.redis.cn/
* [Redis作者：深度剖析Redis持久化](http://www.iteye.com/news/24675)