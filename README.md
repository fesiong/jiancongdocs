#简从二次开发手册

##简从是一个什么样的工具
简从是一款基于微信社群的二级分销系统。后端开发语言是php,使用[Phalcon][phalcon]作为底层框架开发,前端使用的框架是Bootstrap(桌面端)和JQuery-WeUI(移动端)。二次开发需要了解Phalcon框架
##简从推荐运行环境
CentOS6.5 + PHP5.6 + Nginx1.10 + Mysql5.7
##二次开发需要准备的
[Phalcon教程][phalcondocs]  
[Volt模板引擎使用教程][voltdocs]  
[Bootstrap][bootstrap]  
[Jquery-WeUI][jquery-weui]  
[weui][weui]

##简从系统目录结构
[link][tree]
##简从系统数据库字典
[link][dict]
##常用函数
常用函数都放在了app/Library/Helper.php中  
- Helper::isMobile($text)  判断是否是手机号码
- Helper::inWeixin()  是否在微信内
- Helper::dateFriendly($timestamp, $time_limit = 31556926, $out_format = 'Y-m-d H:i', $formats = null, $time_now = null) 友好的时间输出
- volt模板中可以用的php函数
```php
number_format()   
date()  
chr()               
explode()  
dateFriendly()     友好的时间输出  
getSetting($name)  获取系统配置  
```
常用开发请参考Phalcon教程
##二次开发建议
1. URL路由  
URL路由规则需要写到对应的路由规则文件中  
后台的路由规则写在app/config/adminRouter.php里  
桌面端的路由规则写在app/config/wwwRouter.php里
移动端的路由规则写在app/config/router.php里
路由规则编写参照[路由Routing][routing]
2. 控制器规则  
控制器编写,参照[控制器Controller][controller]
3. 模板命名规则  
建立Controller后,需要在模板目录的layouts下,建立一个名称为Controller名称相同的layout,小写字母。如建立了TopicController,那么layouts里面要建立一个topic.volt,否则会报错。  
其他规则参照[使用视图][useingviews]
4. 其他建议  
公共方法,尽量写在Library里面。  
有疑问可以发issue


[phalcon]:https://github.com/phalcon/cphalcon/
[phalcondocs]:https://docs.phalconphp.com/zh/latest/index.html
[voltdocs]:https://docs.phalconphp.com/zh/latest/reference/volt.html
[tree]:tree.md
[dict]:dict.md
[jquery-weui]:https://github.com/lihongxun945/jquery-weui
[weui]:https://github.com/weui/weui
[bootstrap]:https://github.com/twbs/bootstrap/tree/v3.3.7
[routing]:https://docs.phalconphp.com/zh/latest/reference/routing.html
[controller]:https://docs.phalconphp.com/zh/latest/reference/controllers.html
[useingviews]:https://docs.phalconphp.com/zh/latest/reference/views.html