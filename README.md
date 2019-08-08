# redis_idempotent
idempotent using redis, inspired by zhss. Home work for 07/08/2019

8月7日作业。接口幂等性设计。
这个工程是一个简单的Redis Util。

可以被其他工程引用。

对Spring Cloud的样例代码的inventory-service进行了改造。

0、引入该工程
![引入该工程](https://github.com/alexjingjing/redis_idempotent/blob/master/screenshots/pom.png?raw=true)

1、修改yml配置
![修改yml配置](https://raw.githubusercontent.com/alexjingjing/redis_idempotent/master/screenshots/yml.png)

2、修改Application，添加scanBasePackages
![修改Application](https://github.com/alexjingjing/redis_idempotent/blob/master/screenshots/Application+scanpackage.png?raw=true)

3、修改Service逻辑
![修改Service逻辑](https://github.com/alexjingjing/redis_idempotent/blob/master/screenshots/service.png?raw=true)

但感觉这样做跟实际业务有耦合。因为需要在inventory-service设置redis地址。

可能需要设计一个通用拦截器。
