Chapter1 – introduction
Simple, Clean, Beautiful
Coding in Laravel 5 is great fun.
To make PHP development fun & easy
Chapter2– Required software & component
http://laravelcoding.com/blog/laravel-5-beauty-required-software-and-components

Jeff Jones • 5 months ago

Question regarding where to use the various tools. I'll say up front I'm new to both PHP and Laravel. I'm not questioning your method, rather the reason why and if one method is better than the other. I set up my environment before I ran across your book.
In setting up my environment I followed another guide which only used git, vagrant and homestead in the local environment. Everything else is run in the VM. While installing this way I thought that was nice and compact. I didn't have to set up a duplicate environment on my local that was already installed on the VM. This means that Composer, Artisan, php, node etc. are all run on the VM while the IDE is configured to edit files locally. No need to duplicate the installs locally.
Will there be issues running this way? Your thoughts???? Thanks, Jeff…
Avatar
Chuck Heintzelman Mod Jeff Jones • 5 months ago
Shouldn't be an issue. The reason I went with a few tools available both in the standard console and within the VM is that I find it handy to open up the console to do quick things (like composer, gulp, etc.) without going into the vm.
Jeff Jones Chuck Heintzelman • 5 months ago

Thanks for the quick reply. Makes sense. More of a personal preference than requirement.
Chapter3 – Windows
skipped

Chapter4 – Setting up an OS X or Linux Machine
homestead / laravel installer
TBD
Chapter5 – Exploring installed homestead / laravel installer
yaml
authorize:
keys:
databases:
variables:
adding software to homestead VM
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install unzip
serve command from VM

not really as good as editting ymal

mysql command

mysql –user=homestead –password=secret
drop database xxx
create database xxx
Chapter6 – PhpUnit & Markerdown
http://laravelcoding.com/blog/laravel-5-beauty-testing

npm 是 Node.js 的模块依赖管理工具。作为开发者使用的工具，主要解决开发 Node.js 时会遇到的问题。如同 RubyGems 对于 Ruby 开发者和 Maven 对于 Java 开发者的重要性，npm 对与 Node.js 的开发者和社区的重要性不言而喻。本文包括五点：package.json 、npm 的配置、npm install 命令、npm link 命令和其它 npm 命令。
package.json
npm命令运行时会读取当前目录的 package.json 文件和解释这个文件，这个文件基于 Packages/1.1 规范。在这个文件里你可以定义你的应用名称( name )、应用描述( description )、关键字( keywords )、版本号( version )、应用的配置项( config )、主页( homepage )、作者( author )、资源仓库地址( repository )、bug的提交地址( bugs )，授权方式( licenses )、目录( directories )、应用入口文件( main )、命令行文件( bin )、应用依赖模块( dependencies )、开发环境依赖模块( devDependencies )、运行引擎( engines )和脚本( scripts )等。
In case phpunit does not work, simply remove vendor folder, and run
composer update
to recreate it.

annotation @dataProvider xxxClassName
behavior driven devlopment
SpecBDD – phpspec…
StoryBDD – Behat
Chapter7 – 10 minutes Blog
laravel function:
nl2br(e(…))
str_limit(…)
join(\n\n', …)
config('blog.title')
withPost(...)    same as   , compact('post')
Carbon::now()
faker-> paragraphps/
        DateTimeBetween(  -1day,  +3weeks  )
        mt_rand(3,8)
$this->attributes['field_name']

learn from view
{!! $posts->render() !!} 显示分页导航条
Page {{ posts->currentPage() }} of {{
posts->currentPage() }} of {{
posts->lastPage() }}


{{ config('blog.title') }}
{{ str_limit($post->content) }}
{!! nl2br(e($post->content)) !!} //displays normal

e() The e function runs htmlentities over the given string:
echo e('foo'); // <html>foo</html>
{{ nl2br(e($post->content)) }} // displays

关于分页：

class BlogController extends Controller
{
    public function index()
    {
        $posts = Post::where('published_at', '<=', Carbon::now())
            ->orderBy('published_at', 'desc')
            ->paginate(config('blog.posts_per_page'));
Chapter8 – auth / admin routing (resource routing)
Three types of routing:
basic routing
controller routing
Route::auth();
resource controller 7 / ['except' =>] / 用resource方式创建的路由直接有 route name
insert (get/put) – create/store
update(get/put) – edit/update
delete –destroy
display all – index
display single – show
navbar header, simply copy from offical web site
http://getbootstrap.com/getting-started/
>
 <div class="container">

   <div class="navbar-header">

     <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">

       <span class="sr-only">Toggle navigation</span>

       <span class="icon-bar"></span>

       <span class="icon-bar"></span>

       <span class="icon-bar"></span>

     </button>

     <a class="navbar-brand" href="#">Project name</a>

   </div>
涉及到导航栏的逻辑，与quickM的非常相似。

middleware： guest
protected $routeMiddleware = [
'auth' => \App\Http\Middleware\Authenticate::class,
'auth.basic' => \Illuminate\Auth\Middleware\AuthenticateWithBasicAuth::class,
'can' => \Illuminate\Foundation\Http\Middleware\Authorize::class,
'guest' => \App\Http\Middleware\RedirectIfAuthenticated::class,
'throttle' => \Illuminate\Routing\Middleware\ThrottleRequests::class,
];
Bootstrap仍然需要深入学习
Chapter9 – using bower
Chapter10–Tag
new bootstrap controls, table behavior, sort/search
TBD: Seed: tag data
session('success')
alert
Chapter11 – Upload files
Chapter12 – Post Administration
=======================================================================

KNOWN ISSUES
how to snapshot / box package current homestead for future restore/reusage?
bower/ gulp / why some feature ommitted such as ?
hostonly why port other than 80 not accessible?
TBD
composer global require "laravel/homestead=~2.0" in Chater4
composer global require "laravel/installer=~1.1" in Chater4
Middleware
guest/auth/guard/auth:basic, 深入理解，各自的用法
Chapter 8 ， navigation bar – fixed why not work?
Chapter 12 , sync, lists, detach
class=table table-sripped table-bordered ???
