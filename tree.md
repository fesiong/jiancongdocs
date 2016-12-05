#简从系统目录结构
```bash
├── Phalcon                         Phalcon额外组件  
├── app                             应用目录  
│   ├── Admin                           网站后台应用  
│   │   ├── Controllers                 后台控制器  
│   │   │   ├── AdminBase.php           后台公共控制器,所有后台控制器都继承于此  
│   │   │   ├── AjaxController.php      ajax处理  
│   │   │   ├── ArticleController.php   文章管理  
│   │   │   ├── CategoryController.php  分类管理  
│   │   │   ├── FinanceController.php   财务管理  
│   │   │   ├── IndexController.php     后台首页  
│   │   │   ├── LoginController.php     后台登录  
│   │   │   ├── ProductController.php   产品管理  
│   │   │   ├── SettingController.php   网站设置  
│   │   │   ├── ShareController.php     代言管理  
│   │   │   ├── UserController.php      用户管理  
│   │   │   └── WeixinController.php    微信相关管理  
│   │   └── views                   后台模板  
│   │       ├── article             文章管理模板  
│   │       │   ├── index.volt          文章添加、编辑  
│   │       │   └── list.volt           文章列表  
│   │       ├── category            分类管理模板  
│   │       │   ├── index.volt          分类编辑  
│   │       │   └── list.volt           分类列表  
│   │       ├── finance             财务管理模板  
│   │       │   ├── flow.volt           流水列表  
│   │       │   ├── flowshow.volt       流水详情  
│   │       │   ├── order.volt          订单列表  
│   │       │   ├── ordershow.volt      订单详情  
│   │       │   ├── refund.volt         退款列表  
│   │       │   ├── refundshow.volt     退款详情  
│   │       │   ├── spread.volt         代言收入列表  
│   │       │   ├── total.volt          汇总  
│   │       │   ├── withdraw.volt       提现申请列表  
│   │       │   └── withdrawshow.volt   提现申请详情  
│   │       ├── index               首页模板  
│   │       │   └── index.volt          首页  
│   │       ├── index.volt          模板主模板,所有模板都继承于此  
│   │       ├── layouts             layouts,每个控制器都会有一个对应的layout,否则会报错  
│   │       │   ├── article.volt        文章管理  
│   │       │   ├── category.volt       分类管理  
│   │       │   ├── finance.volt        财务管理  
│   │       │   ├── index.volt          首页  
│   │       │   ├── login.volt          登录管理  
│   │       │   ├── product.volt        产品管理  
│   │       │   ├── setting.volt        设置管理  
│   │       │   ├── share.volt          代言管理  
│   │       │   ├── user.volt           用户管理  
│   │       │   └── weixin.volt         微信相关  
│   │       ├── login               登录模板  
│   │       │   └── index.volt          登录  
│   │       ├── product             产品管理模板  
│   │       │   ├── index.volt          编辑产品  
│   │       │   ├── list.volt           产品列表  
│   │       │   ├── news.volt           产品动态列表  
│   │       │   └── newscomments.volt   产品动态评论列表  
│   │       ├── setting             网站设置模板  
│   │       │   ├── content.volt        内容设置  
│   │       │   ├── finance.volt        财务设置  
│   │       │   ├── nav.volt            首页导航  
│   │       │   ├── oauth.volt          第三方登录  
│   │       │   ├── payway.volt         支付平台  
│   │       │   ├── register.volt       注册设置  
│   │       │   ├── site.volt           网站设置  
│   │       │   └── sms.volt            短信平台设置  
│   │       ├── share               代言管理  
│   │       │   ├── comments.volt       代言评论列表  
│   │       │   ├── index.volt          代言编辑  
│   │       │   └── list.volt           代言列表  
│   │       ├── user                用户管理  
│   │       │   ├── add.volt            添加用户  
│   │       │   ├── addverify.volt      增加用户认证  
│   │       │   ├── admin.volt          后台管理员  
│   │       │   ├── adminadd.volt       增加管理员  
│   │       │   ├── comments.volt       用户评论  
│   │       │   ├── list.volt           用户列表  
│   │       │   ├── verify.volt         认证列表  
│   │       │   └── verifyinfo.volt     认证详情  
│   │       └── weixin              微信相关管理  
│   │           ├── menu.volt           微信菜单  
│   │           ├── message.volt        微信消息  
│   │           ├── messages.volt       微信群发  
│   │           ├── qrcode.volt         微信二维码  
│   │           ├── reply.volt          自动回复规则  
│   │           ├── replyedit.volt      编辑回复  
│   │           └── replymessage.volt   
│   ├── Controllers                 前台(移动端)控制器  
│   │   ├── AjaxController.php          ajax处理  
│   │   ├── BugfixController.php        调试控制器  
│   │   ├── ControllerBase.php          公共控制器,所有控制器都继承于此  
│   │   ├── ErrorController.php         错误控制器  
│   │   ├── GroupController.php         团购控制器  
│   │   ├── HelpController.php          帮助控制器  
│   │   ├── IndexController.php         首页控制器  
│   │   ├── LoginController.php         登录控制器  
│   │   ├── NotificationController.php  通知控制器  
│   │   ├── OauthController.php         第三方登录控制器  
│   │   ├── PageController.php          单页控制器  
│   │   ├── PaymentController.php       支付控制器  
│   │   ├── ProductController.php       产品控制器  
│   │   ├── PublishController.php       发布产品控制器  
│   │   ├── RefundController.php        退款控制器  
│   │   ├── ShareController.php         代言控制器  
│   │   ├── TokenTrait.php              csrf验证Trait  
│   │   └── UserController.php          用户控制器  
│   ├── Fesiong.php                 应用主控制文件。  
│   ├── Forms                       表单  
│   │   ├── LoginForm.php               登录表单  
│   │   └── RegisterForm.php            注册表单  
│   ├── Library                     Library,一些公共文件作为library放到这里  
│   │   ├── AliPay.php                  支付宝处理类  
│   │   ├── Captcha.php                 验证码生成类  
│   │   ├── Common.php                  公共类  
│   │   ├── Content.php                 内容类  
│   │   ├── Helper.php                  Helper类  
│   │   ├── Image.php                   图像裁剪类  
│   │   ├── OauthQQ.php                 QQ授权类  
│   │   ├── OauthWeixin.php             微信授权类  
│   │   ├── QrCode                      二维码处理类库  
│   │   ├── Queue                       队列处理类,没完成*  
│   │   ├── Sms                         短信接口  
│   │   ├── Tag.php                     标签助手扩展  
│   │   ├── Upload.php                  上传类库  
│   │   ├── Weixin                      微信相关类库  
│   │   │   ├── ***  
│   │   │   ├── apiclient_cert.pem      微信支付证书,放在这里  
│   │   │   └── apiclient_key.pem       微信支付证书    
│   │   └── Weixin.php                  微信处理类库  
│   ├── Models                      数据库表模型,每个模型对应一个表,具体表说明参见[数据库字典  ][dict]
│   │   ├── BaseModel.php               模型公共文件,所有模型都继承于此  
│   ├── Plugins                     插件目录  
│   ├── Www                         桌面端应用  
│   │   ├── Controllers             桌面端控制器  
│   │   │   ├── AjaxController.php      ajax处理  
│   │   │   ├── HelpController.php      帮助  
│   │   │   ├── IndexController.php     首页  
│   │   │   ├── LoginController.php     登录  
│   │   │   ├── NewsController.php      新闻  
│   │   │   ├── OauthController.php     第三方授权  
│   │   │   ├── PageController.php      单页  
│   │   │   ├── ProductController.php   产品  
│   │   │   ├── PublishController.php   发布产品  
│   │   │   ├── RefundController.php    退款  
│   │   │   ├── ShareController.php     代言  
│   │   │   ├── UserController.php      用户中心  
│   │   │   └── WwwBase.php             桌面端公共控制器,所有桌面端控制器都会继承于此  
│   │   └── views                   桌面端模板,结构同移动端。  
│   │       ├── help                    帮助模板  
│   │       │   ├── list.volt  
│   │       │   └── show.volt  
│   │       ├── index                   首页模板  
│   │       │   ├── index.volt  
│   │       │   └── list.volt  
│   │       ├── index.volt              主模板  
│   │       ├── layouts                 layouts,每个控制器都会有一个对应的layout,否则会报错  
│   │       │   ├── help.volt  
│   │       │   ├── index.volt  
│   │       │   ├── login.volt  
│   │       │   ├── news.volt  
│   │       │   ├── oauth.volt  
│   │       │   ├── page.volt  
│   │       │   ├── product.volt  
│   │       │   ├── publish.volt    
│   │       │   ├── refund.volt  
│   │       │   ├── share.volt  
│   │       │   └── user.volt  
│   │       ├── login                   登录模板  
│   │       │   └── index.volt  
│   │       ├── news                    新闻模板  
│   │       │   └── list.volt  
│   │       ├── oauth                   第三方登录模板  
│   │       │   └── bindqq.volt  
│   │       ├── page                    单页展示模板  
│   │       │   └── show.volt  
│   │       ├── partials                模板代码片段  
│   │       │   ├── footer.volt         尾部模板  
│   │       │   ├── header.volt         头部模板  
│   │       │   ├── helpsearch.volt  
│   │       │   ├── userheader.volt  
│   │       │   └── userproduct.volt  
│   │       ├── product                 产品模板  
│   │       │   ├── list.volt  
│   │       │   └── show.volt  
│   │       ├── publish                 发布产品模板  
│   │       │   ├── create.volt  
│   │       │   ├── default.volt  
│   │       │   ├── index.volt  
│   │       │   └── next.volt   
│   │       ├── refund                  退款处理模板  
│   │       │   ├── apply.volt  
│   │       │   ├── detail.volt  
│   │       │   ├── detailinfo.volt  
│   │       │   └── reject.volt  
│   │       ├── share                   代言模板  
│   │       │   ├── list.volt  
│   │       │   └── show.volt  
│   │       └── user                    用户中心模板  
│   │           ├── account.volt  
│   │           ├── accountadd.volt  
│   │           ├── address.volt  
│   │           ├── addressadd.volt  
│   │           ├── buyercode.volt  
│   │           ├── product             用户订购、代言、出售模板  
│   │           │   ├── order.volt  
│   │           │   ├── orderinfo.volt  
│   │           │   ├── publish.volt  
│   │           │   ├── sell.volt  
│   │           │   ├── sellinfo.volt  
│   │           │   └── share.volt  
│   │           ├── product.volt  
│   │           ├── publishnews.volt  
│   │           ├── setting.volt  
│   │           ├── verifyapply.volt  
│   │           ├── wallet.volt  
│   │           └── withdraw.volt  
│   ├── cache                缓存目录  
│   │   ├── captcha             验证码缓存  
│   │   ├── data                数据库缓存  
│   │   ├── metaData            表信息缓存  
│   │   ├── models              模型数据缓存  
│   │   ├── views               视图缓存  
│   │   └── volt                模板缓存  
│   ├── config              网站配置  
│   │   ├── adminRoutes.php     后台路由规则  
│   │   ├── config.php          公共配置  
│   │   ├── development.php     测试环境配置  
│   │   ├── env.php             环境变量  
│   │   ├── routes.php          移动端路由规则  
│   │   ├── site.php            站点配置  
│   │   └── wwwRoutes.php       桌面端路由规则  
│   ├── logs                错误日志  
│   │   ├── application.log     404日志  
│   │   ├── db.log              数据库访问日志,在config.php中开启错误记录为debug的时候才会记录  
│   │   └── error.log           错误日志,当网站打不开的时候,请查阅这个文件  
│   └── views               移动端模板  
│       ├── error               错误显示模板  
│       │   ├── index.volt  
│       │   ├── message.volt  
│       │   └── route404.volt  
│       ├── group               团购模板  
│       │   ├── order.volt  
│       │   └── show.volt  
│       ├── help                帮助模板  
│       │   ├── index.volt  
│       │   ├── list.volt  
│       │   └── show.volt  
│       ├── inbox               消息  
│       │   └── show.volt  
│       ├── index               首页模板  
│       │   ├── index.volt
│       │   └── qrcode.volt  
│       ├── index.volt          主模板,所有模板都继承于此  
│       ├── layouts             layouts,每个控制器都会有一个对应的layout,否则会报错  
│       │   ├── error.volt  
│       │   ├── group.volt  
│       │   ├── help.volt  
│       │   ├── index.volt  
│       │   ├── login.volt  
│       │   ├── notification.volt  
│       │   ├── oauth.volt  
│       │   ├── payment.volt  
│       │   ├── product.volt  
│       │   ├── publish.volt  
│       │   ├── refund.volt  
│       │   ├── share.volt  
│       │   ├── sign.volt  
│       │   └── user.volt  
│       ├── login               登录模板  
│       │   ├── bindmobile.volt  
│       │   ├── index.volt  
│       │   └── sms.volt  
│       ├── notification        通知模板  
│       │   └── list.volt  
│       ├── oauth               第三方登录模板  
│       │   ├── bindqq.volt  
│       │   ├── qq.volt  
│       │   └── weixin.volt  
│       ├── page                单页模板  
│       │   └── show.volt  
│       ├── partials            模板代码片段  
│       │   ├── endorsement.volt  
│       │   ├── endorsementorder.volt  
│       │   ├── endorsementuser.volt  
│       │   ├── footer.volt  
│       │   ├── header.volt  
│       │   ├── helpsearch.volt  
│       │   ├── notice.volt  
│       │   ├── order.volt  
│       │   ├── product.volt  
│       │   ├── productitem.volt  
│       │   ├── userproduct.volt  
│       │   └── wallet.volt  
│       ├── payment             支付模板  
│       │   └── gateway.volt  
│       ├── product             产品模板  
│       │   ├── share.volt  
│       │   └── show.volt  
│       ├── publish             发布产品模板  
│       │   ├── create.volt  
│       │   ├── default.volt  
│       │   ├── index.volt  
│       │   └── next.volt  
│       ├── refund              退款协商模板  
│       │   ├── apply.volt  
│       │   ├── detail.volt  
│       │   ├── detailinfo.volt  
│       │   └── reject.volt  
│       ├── share               代言模板  
│       │   ├── needcode.volt  
│       │   ├── order.volt  
│       │   ├── publish.volt  
│       │   ├── seller.volt  
│       │   ├── share.volt  
│       │   ├── sharecode.volt  
│       │   ├── sharelist.volt  
│       │   ├── show.volt  
│       │   └── user.volt  
│       ├── user                用户中心模板  
│       │   ├── account.volt  
│       │   ├── accountadd.volt  
│       │   ├── address  
│       │   │   ├── add.volt  
│       │   │   └── edit.volt  
│       │   ├── address.volt  
│       │   ├── addressadd.volt  
│       │   ├── buyercode.volt  
│       │   ├── changeorder.volt  
│       │   ├── follow.volt  
│       │   ├── index.volt  
│       │   ├── notice.volt  
│       │   ├── order  
│       │   │   └── show.volt  
│       │   ├── order.volt  
│       │   ├── password.volt  
│       │   ├── product  
│       │   │   ├── order.volt  
│       │   │   ├── orderinfo.volt  
│       │   │   ├── publish.volt  
│       │   │   ├── sell.volt  
│       │   │   ├── sellinfo.volt  
│       │   │   └── share.volt  
│       │   ├── product.volt  
│       │   ├── publishnews.volt  
│       │   ├── refund.volt  
│       │   ├── sale.volt  
│       │   ├── setting.volt  
│       │   ├── share.volt  
│       │   ├── verifyapply.volt  
│       │   ├── wallet.volt  
│       │   ├── withdraw.volt  
│       └── weixin          微信模板  
│           └── authorization.volt  
├── cli                 cli脚本  
│   ├── Crond.php       定时任务处理脚本,每分钟执行一遍  
│   └── cli.php  
├── public              公共资源,网站根目录  
│   ├── css                 css资源  
│   │   ├── adminstyle.css  后台css  
│   │   ├── style.css       移动端css  
│   │   └── wwwstyle.css    桌面端css  
│   ├── favicon.ico  
│   ├── fonts               字体目录  
│   ├── img                 图片目录  
│   ├── index.php  
│   ├── js                  js目录  
│   │   ├── adminapp.js     后台js  
│   │   ├── ajaxfileupload.js  
│   │   ├── app.js          移动端js  
│   │   ├── distpicker.data.min.js  
│   │   ├── distpicker.min.js  
│   │   ├── jquery.fancybox.pack.js  
│   │   ├── mobilesw.js     移动端js  
│   │   ├── sw.js           后台、桌面端js  
│   │   ├── webuploader  
│   │   └── wwwapp.js       桌面端js  
│   ├── mobileeditor        移动端编辑器  
│   ├── t.htm               计时请求文件  
│   ├── umeditor            百度编辑器  
│   ├── uploads             上传目录  
│   └── webuploader  
├── xiaonongbang.sql        sql文件  
└── 配置  
    ├── config.php  
    └── site.php  
```


[dict]:dict.md