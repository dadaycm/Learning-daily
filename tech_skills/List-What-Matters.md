# contents
 - laravel
 - vue.js
 - AWS
 - NoSql
 - Python Statistics
 - Nginx
 - Mac 强迫症的Mac设置指南  Github
 - Alfred 

## Laravel cheat sheet

## Laravel 5 Faker tutorial  

http://www.tutorials.kode-blog.com/laravel-5-faker-tutorial

Faker can be used to generate the following data types

Numbers
Lorem text
Person i.e. titles, names, gender etc.
Addresses
Phone numbers
Companies
Text
DateTime
Internet i.e. domains, URLs, emails etc.
User Agents
Payments i.e. MasterCard
Colour
Files
Images
uuid
Barcodes
Miscellaneous

```
Route::get('/customers',function(){
    $faker = Faker\Factory::create();

    $limit = 10;

    for ($i = 0; $i < $limit; $i++) {
        $faker->name . ', Email Address: ' . $faker->unique()->email . ', Contact No' . $faker->phoneNumber . '<br>';
    }
});

```

## laravel下有哪些包值得推荐？知乎

Carbon
Laravel 其实已经包含了这个扩展包了，但是我觉得有必要单独提一下，因为用得还是比较多的。在日期处理方面的确帮了很大忙。
Debugbar
这个扩展包能够提供更多深层的运行信息，方便你修复bug，让应用高效、流畅的运行。
Envoy
Envoy 能帮你在远程系统上运行 SSH 命令。在本地系统和远程部署时它都帮了很大的忙。
Laravel DomPDF
这个扩展包将 DomPDF 库包装成 Laravel 化的调用语法，让创建 PDF 很轻松。
Laravel Generators
使用生成器能够加速开发过程。它所包含的指令几乎涵盖了 Laravel 开发中的方方面面。
Laravel IDE Helper
如果你在使用 PhpStorm，那么这个工具包是必须要装的。我在所有项目中都使用了它，这让 IDE 使用起来很 nice。
Intervention
每个项目几乎都要处理图片上传的功能，Intervention 让图片上传和处理 so easy！
Parsedown
解析 Markdown 就靠它了！快速、稳定、易于使用。

原文出处：8 Laravel Packages For Your Next Project
译文出处：推荐8个优秀的Laravel包

补充两个我自己做的包：
laravel-lang Laravel 5 多国语言包，包含37种语言
laravel-pinyin Laravel 5 中文转拼音


## Vue.js
