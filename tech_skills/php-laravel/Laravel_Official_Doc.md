laravel5.2官网文档学习笔记

实践到哪里，就记录到哪里。
install
sample：quickBasic，quick mediate
基础篇
Routing：
    实验，从浏览器页面自由输入，instead of 仅仅从页面导航进入。
    路由返回view的多种方式，最简单的有return一个字符串的。
    参数携带到view
    通过controller对route进行二级分发。
    --分为single route 和 route group （middleware => web 常态）
中间件MiddleWare
    对于Request进行过滤或者限制。例如：Authentication。
Controller
    --路由的二级分发。
    -- PHP artisan make:controller xxxxx --resource  将会自带若干函数：index，show，delete等等。通过 Route：：resource（‘model名称’， ‘controller名称’）进行路由分配。
Request
    --进行解析 Request：：all（）注意use后面完整路径需要变通成facade
    --解析session数据。 	dd(Session::all()); 注意路由需要包到web中间件，否则没有session数据。
            Route::group(['middleware' => ['web']], function () {
Response
Views
    *.blade.php
Blade模板：
    {{ $变量名 }}
    一些特殊的语法，例如 @foreach...
架构篇
一次请求的生命周期Request
    **Public/index.php是入口。加载composer的autoloader。取出bootstrap/app.php定义的laravel application的instance
    **app/Http/Kernel.php是个黑盒子。Kernel的handle方法读取request，给出response。
    **Kernel引导actions中，有重要的一项是：加载 service providers（它们配置在config/app。php文件的providers数组）。每个service provider中定义了两个重要的方法：register，boot。
    **缺省的service provider定义在app/Providers路径。
    **AppServiceProvider缺省是一个empty。此处可以定制引导bootstrap。
Application结构
    --App
    --App/Http
    --Resource/View
    --.env
    --tests单元测试
    --storage存储cache，compiled blade，session等，甚至临时view
    --database包含migration和seed
Service Provider
    居于laravel Application引导（bootstrapping）的核心位置。
    如何register Provider？在config/app。php文件中的数组providers里面加入这个class即可。
Service contatiner
    一个工具，用于管理class依赖，执行dependency的injection
Contract抽象

    一组interface，用于定义framework提供的核心service
    大多数情况下，facade够用了；但是contract提供更好的loose couple，simplicity。
Facade门面
    static interface？
数据库篇
支持的类型：MySql / SQLite/ Postgres / SQL Server
读写分离：可以分别指定。read  ，  write
支持使用SQL语句的查询
    $users = DB::select( 'select * from users where ...' );
    $afftected = DB::insert('insert into users (...) values(...)')
    $affected   = DB::update('update users set votes=100 where name=?', ['John'])
    affected = DB::delete('delete from users where...')
    DB::statement('drop table users') // general SQL , don't return any value
监听查询事件（用于查询日志，调试）
在ServiceProvider的boot（）方法中加入：
        DB：：listen（）
// php artisan tinker
DB::listen(function($sql){ var_dump($sql);  });
