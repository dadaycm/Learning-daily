ssh-keygen -t rsa -C "your@email.com"
php artisan key:generate
 chmod -R a+w storage/
 chmod -R a+w bootstrap/cache/

修改 config/APP.php
    'debug' => env('APP_DEBUG'),
修改 config/database.PHP
migrate 报错问题：

        'mysql' => [
            'driver'    => 'mysql',
            'host'      => env('DB_HOST', 'localhost'),
            'database'  => env('DB_DATABASE', 'forge'),
            'username'  => env('DB_USERNAME', 'forge'),
            'password'  => env('DB_PASSWORD', ''),
            'charset'   => 'utf8',
            'collation' => 'utf8_unicode_ci',
            'prefix'    => '',
            'strict'    => true,  // false changed to true
        ],

App/Http/Kernel.php, comment it out:
        // \App\Http\Middleware\VerifyCsrfToken::class,
=============
composer install
npm install
创建.env文件（示例中已包含）
php artisan key:generate
php artisan migrate
在UserTableSeeder.php设置管理员信息
php artisan db:seed
npm install -g gulp
运行gulp或gulp watch
