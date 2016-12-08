
################################################################## not good
#go to laravel, install laravel, select a location first as root
export PATH=$PATH:/home/hliu/.composer/vendor/bin
######################################################################
############################################################################
sudo composer create-project --prefer-dist laravel/laravel mylove
sudo chmod -R 777 ./storage/
sudo chmod -R 777 ./storage/cache
############################################################################
git clone https://github.com/laravel/quickstart-intermediate quickstart
cd quickstart/
less .env
composer install
php artisan migrate
sudo php artisan serve --port=80
############################################################################
/opt/lampp/xampp restart
#reset ubuntu software update source
htop
iostat
####################################################################
rename "s/laravel.from-scratch.chapter/LFS.chp-" *
####################################################################
简单的  rename   使用命令：
字母的替换
rename "s/AA/aa/" *               //把文件名中的AA替换成aa
修改文件的后缀
rename "s/.html/.php/" *          //把.html 后缀的改成 .php后缀
批量添加文件后缀
rename "s/$/.txt/" *              //把所有的文件名都以txt结尾
批量删除文件名
rename "s/.txt//" *               //把所有以.txt结尾的文件名
####################################################################
 rename 's/Listing-//' *
tar -zxf lnmp1.2-full.tar.gz
 sudo lsattr  default/.user.ini  
 sudo chattr -i -e default/.user.ini  
 sudo rm -rf  default/.user.ini  
####################################################################
find . -type f | xargs -i unzip {} -d {}.unzip
