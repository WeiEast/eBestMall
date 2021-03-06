eBestMall - B2B2C商城系统
===============================
> eBestMall是国内电子商务系统及服务解决方案新创品牌。为传统企业及创业者提供零售网店系统、网上商城系统、分销系统、B2B2C商城系统、微信分销系统、行业ERP等产品和解决方案。

[![Latest Stable Version](https://poser.pugx.org/hongyukeji/ebestmall/v/stable.png)](https://packagist.org/packages/hongyukeji/ebestmall)
[![Total Downloads](https://poser.pugx.org/hongyukeji/ebestmall/downloads.png)](https://packagist.org/packages/hongyukeji/ebestmall)

# 安装与更新

```
运营版：
# composer create-project hongyukeji/ebestmall ebestmall

开发版：
# composer create-project hongyukeji/ebestmall ebestmall dev-master

更新：
# composer update
```

# 运行环境

* PHP版本：>=7.0
* MySQL版本：>=5.5

# 系统开发

* 公司名称：鸿宇科技有限公司
* 公司官网：www.hongyuvip.com
* 系统框架：Laravel 5.5
* 核心技术：PHP7、Html5、Css3、JavaScript ES6、jQuery、Ajax、MySQL、VueJS、Bootstrap
* 开发工具：PhpStorm、Navicat for MySQL、PhotoShop CS6、
* 开发团队：Shadow（项目总监）、Spider（代码审计）、Free(数据库建模)、Wind（PHP后端开发）、Flower（前端UI设计）、Boy(Html5前端开发)
* 项目支持：感谢所有支持鸿宇团队的朋友！

# 系统维护

* Http： www.ebestmall.com
* Author：Shadow
* Email：admin@hongyuvip.com
* QQ：1527200768
* Phone：13952101395

# 伪静态

* Apache
    > Laravel包含一个文件，用于在路径中没有前端控制器的情况下提供URL 。在为Apache服务Laravel之前，请务必启用该模块，以便服务器将该文件保存。public/.htaccess index.php mod_rewrite .htaccess
    ```
    Options +FollowSymLinks
    RewriteEngine On
    
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule ^ index.php [L]
    ```

* Nginx
    > 如果您使用Nginx，您的站点vhost.conf配置中的以下指令将会将所有请求都引导到前台控制器：index.php
    ```
    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }
    ```

# 开发日志

```
2016-10-08 09:30:39 RBAC 权限管理 ( 完成 )
2016-12-18 12:26:58 公共布局页面 ( 完成 )
2017-03-16 20:39:56 管理员模块 ( 完成 )
2017-03-17 17:51:50 后端系统模块 ( 完成 )
2017-04-01 16:07:18 数据库初期建模 ( 完成 )
2017-05-11 16:17:29 前后端html视图 ( 完成 )
2017-06-18 18:18:18 购物功能建模 ( 完成 )
2017-06-27 17:29:39 手机端UI设计 ( 完成 )
2017-07-17 23:53:30 前端代码审计 ( 完成 )
2017-07-18 00:29:56 注册登陆功能 （完成）
2017-07-18 00:43:34 前端会员中心视图 （完成）
2017-07-18 10:28:33 购物车功能模块 （完成）
2017-07-18 11:15:26 会员功能模块 （完成）
2017-07-18 13:56:18 商品展示模块 （完成）
2017-07-18 16:37:56 商品/购物车/订单/商品分类/数据建模 （完成）
2017-07-18 21:22:43 注册->登录->查看商品->加入购物车功能模块 （完成）
2017-07-18 21:22:43 提交订单->付款->查看订单信息->确认收货 （完成）
2017-08-31 13:20:25 eBestMall转移至laravel 5.5 LTS 框架 （进行中）
```

# 其它

* artisan 创建 控制器
```
php artisan make:controller BaseController
```
* artisan 创建 模型
```
php artisan make:model Article
```

* 生成模型的同时生成迁移文件
```
php artisan make:model Article -m
php artisan make:model Models\Article -m
```

* artisan 创建 中间件
```
php artisan make:middleware Article
```

* tinker
```
php artisan tinker
factory(App\Article::class,10)->make(); // 只显示不保存
factory(App\Article::class,10)->create(); // 生成演示数据并插入数据库
```

* 迁移所有文件
```
php artisan migrate
```

* 迁移文件并添加填充文件
```
php artisan migrate --seed
```

* 回滚再重新运行所有迁移
```
php artisan migrate:refresh --seed
```

* 新建一个article表的迁移文件
```
php artisan make:migration create_articles_table --create=articles
```

* 创建一个填充文件
```
php artisan make:seeder ArticlesTableSeeder
```

* 执行单个填充文件
```
php artisan db:seed --class=ArticlesTableSeeder
```

* 批量执行填充文件（在 /database/seeds/DatabaseSeeder.php 添加 $this->call(ArticlesTableSeeder::class);）
```
php artisan db:seed     
```

* composer 重新加载
```
composer dump-autoload
```

* artisan 清理配置文件缓存
```
php artisan config:cache
```

* 回滚再重新运行所有迁移
```
php artisan migrate:refresh --seed
```