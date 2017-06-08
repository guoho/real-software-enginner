# OAuth2.0原理与实战


## 什么是Oauth

OAuth是一个关于身份授权（authorization）的开放网络标准，目前的版本是2.0版，已成为RFC标准的协议，见RFC 6749

通过OAuth，用户可以允许第三方应用/网站访问该用户在某一网站上存储的私密信息（头像、昵称等），无需将账号和密码提供给第三方应用/网站。
OAuth的基本原理是用户通过网站生成的令牌，而不是账号和密码来获取他们存储在网站的个人信息。


## 为什么使用Oauth

最直接的好处就是可以实现第三方应用/网站免密码统一登陆，以避免要记住各种不同的应用/网站的登陆密码的烦恼。

Oauth具有以下特点：

* 简单：协议简单容易理解，不管是服务端，还是第三方使用都很容易理解并开发；
* 安全：登陆时，无须将账号名跟密码告诉第三方应用，灵活安全；
* 开放：任何服务网站都可以实现自身的OAUTH认证服务；

## 应用场景

Oauth一般用于第三方登陆，如通过微信授权登陆第三方网站，通过QQ,新浪微博、支付宝等

## 实现原理




### Oauth结构

#### 客户端

* Appkey + apptoken保存
* 获取服务端临时授权Token
* 跳转服务端
* 保存access_token回调接口


#### 服务端

* 应用鉴权接口；
* 应用临时Token授权功能；
* 用户登陆
* 用户授权
* 生成应用的授权access_token
* 用户信息获取接口（根据access_token)

#### 用户

* 用户要在网站注册
* 用户授权

#### 数据库设计

##### 服务端
* 应用表
* 用户信息表
* 授权Token表
* 历史记录

##### 客户端

### 授权流程

* 应用注册
* 客户端——>服务端 获取临时授权Token
* 

## Oauth2.0实战

### 原生版
### 已有的类库版
### PHP扩展版
### YII框架的Oauth


## Oauth与OpenId
## Oauth与单点登陆


## 参数资料：

* http://justcoding.iteye.com/blog/1950270
* http://www.cnblogs.com/terryguan/p/4479385.html
* https://my.oschina.net/u/133669/blog/63593
* https://my.oschina.net/kakoi/blog/885369
* https://www.zhihu.com/question/19628327#answer-155694
* http://www.ruanyifeng.com/blog/2014/05/oauth_2_0.html