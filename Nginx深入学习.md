## Nginx深入学习
### Nginx特点
* 高并发，通过epool
* 反向代理，实现负载
* 可实现缓存服务器，通过cache插件（cache_purge）可以实现类squid等专业的缓存软件实现的功能
* 稳定性高
* 低系统资源的消耗
* 丰富的功能集：IP访问限制功能，限制访问次数，频率等



### Nginx代理实现

### Nginx负载实现

* 加权轮询
* IP hash
* 轮询
	
### Nginx缓存
* Nginx的web缓存功能的主要是由proxy_cache、fastcgi_cache指令集和相关指令集完成，proxy_cache指令负责反向代理缓存后端服务器的静态内容，fastcgi_cache主要用来处理FastCGI动态进程缓存
* Nginx的memcached_module模块可以直接从memcached服务器中读取内容后输出，后续的请求不再经过应用程序处理，如php-fpm、django，大大的提升动态页面的速度。[详情阅读](http://www.open-open.com/lib/view/open1377777147386.html)


### Nginx禁止访问机制

* 限制某个IP的访问，设置IP白名单，设置IP黑名单
* 限制某个IP同一时间段的访问次数
* [Nginx Lua Redis防止CC攻击](http://www.linuxeye.com/security/nginx-lua-redis-waf.html)
* [如何通过配置NGINX和NGINX Plus来缓解DDoS攻击？](http://soledede.iteye.com/blog/2040189)
* 等手段实现简单防DDOS攻击，具体的可看相关的详细资料。

### Nginx地址重写

nginx通过ngx_http_rewrite_module模块支持url重写、支持if条件判断


### Nginx使用过程中的问题
 * 重复请求，如果Nginx配置了轮询机制时，当设置的超时时间过短时，可能会出现重复调用后台服务器的情况；
 * 缓存问题导致后端Session串号，由于使用的缓存机制，可能会出现Sesssion串号的问题。
  

### Nginx与Memcache区别

* [Memcache及Redis的网络原理，存储原理，IO原理，数据结构原理区别](http://www.360doc.com/content/17/0303/13/33667232_633622783.shtml)
* http://gnucto.blog.51cto.com/3391516/998509


### 参考文章：
* [官网](http://nginx.org/)
* [Nginx中文手册内容说明](http://www.cnblogs.com/gxbk629/p/4311984.html)
* 《Nginx高性能Web服务器详解》
* [Nginx的特性和一些知识点](http://www.cnblogs.com/na2po2lun/p/4191156.html)
