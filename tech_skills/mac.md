Command Ctrl Option Shift ⌘ ⌃ ⌥ ⇧ ⌘ ⌃ ⌥ ⇧

pbcopy < daily.md
pbpaste > newfile.md
du -sh *
htop
pages file : version control, like time machine.
System preference: share
preview: SPACE key, which applys to pictures
show desktop: ⌘ + F3

Zoom out with Preview: for jpg/pdf,  single `
Hide all other applications: ⌥ + ⌘ + H

Switch between multi-network cofiguration solution

force kill a progress/ quit an application : ⌥ + ⌘ + Esc /
  or ,   ps -ax | grep app-name;   kill -9 id

Keyboard to open Docker : ⌃ + F3, release key, just use up/down to select application and Enter

 __btw, ⌃ + F2 shows menu __

 Block selection : ⌥ + Mouse : 备忘录 works

 ⌥ + Drag: copy files

 ** Spotlight find a file, then Select it, ⌘ + Enter, it will be opened in a new Finder window.

 Alfred : >pwd   directly open a new terminal
 Alfred: ⌥+⌘+C



use SourceTree / Github desktop for mac, to manage github local/remote sync.

Safari常用快捷键

1.标签（tab）操作：
comamnd+shitt+\：所有标签页。对应手势操作：双指捏合、放开

⌘+Z：恢复最近关闭的标签页
⌘+R：刷新重载
⌘+.：停止刷新重载

⌘+L：定位网址
⌘+enter：聚焦地址栏输入时，新标签页后台打开地址或搜索
⌘+⇧+enter：聚焦地址栏输入时，新标签页前台打开地址或搜索
⌘+⌥+enter：聚焦地址栏输入时，新窗口后台打开地址或搜索
⌘+⌥+⇧+enter：聚焦地址栏输入时，新窗口前台打开地址或搜索

⌘+点按：新标签页后台打开链接
⌘+⇧+点按：新标签页前台打开链接
⌘+⌥+点按：在新窗口中打开链接
⌘+⌥+⇧+点按：在新窗口中打开链接，使其成为活跃窗口
⌘+1-9：切换标签页

control+tab：下一个标签页

control+⇧+tab：上一个标签页
⌘+⇧+H：当前标签页打开默认主页


2.书签（bookmarks）操作：
⌘+⇧+L: 显示书签边栏
⌘+D：添加到收藏夹（书签栏）
⌥(alt)+⌘+B：管理/编辑书签页
⌘+⇧+N：新建书签文件夹
control+⌘+1：显示书签边栏
control+⌘+2: 显示阅读列表边栏
control+⌘+3: 显示共享链接边栏


3.阅读列表（Read it later list）：
⌘+⇧+D：将当前页添加到阅读列表
⇧+点按：将链接添加到阅读列表
⌥(alt)+⌘+↑：阅读列表上一个项目
⌥(alt)+⌘+↓：阅读列表下一个项目


4.显示/隐藏：
⌘+⇧+B：收藏栏
⌘+⇧+T：标签页栏
⌘+⌥(alt)+L：下载
⌘+/：状态栏
⌘+Y：显示历史记录

5.查找：
⌘+F：查找
⌘+G/enter：查找下一个
⇧+⌘+G/⇧+enter：查找上一个

6.缩放：
⌘++：放大
⌘+-：缩小
⌘+0：恢复默认
双指点触：智能缩放
⌘+escape：全屏

7.查看扩展：
⌘+,：偏好设置->扩展
⌘+⌥+E：清空浏览器缓存
⌘+⌥+U：查看页面源代码

8.页面
⌘+I：邮寄网页内容
⌘+⇧+I：邮寄网页的链接
↑↓：小范围的垂直滚动页面
←→：小范围的水平滚动页面
⌥＋↑↓：整屏的滚动页面
空格键：整屏滚动
⇧+空格键：整屏上滚
⌘+↑↓：网页上翻下翻到底

⌘+[/]或双指左右滑动：当前标签页内前进/后退
⌘+⇧+R：进入阅读器模式

小技巧：
窗口-合并所有窗口
历史记录-重新打开上次关闭的窗口 ⌘+Z
历史记录-重新打开上次连线时段的所有窗口
设置-高级-勾选“在菜单栏中显示开发菜单”，使用⌘+⇧+J 停用javascript拷贝文字

# pdf 300 mac skills
* ######    删除TimeMachine备份的文件
* ######    移动TimeMachine备份到更大的硬盘
* ######    可选时光机Browse old TimeMachine Disk  -- Option
* ######    行命令技巧的复用：Save As Dialog -- Ctrl A/E/K ; Cmd+D
* ######    命令行快速打开文件Quickly Preview file in terminal: qlmanage -p *.jpg  space
* ######    创建剪贴笔记文件于桌面Create new notepad :  Shift+Command+Y
* ######    打开当前文件夹的finder程序：Open / Save As : Command + R
* ######    命令行调用finder： Open .   : employ finder to open the current folder
* ######    应用程序前进后退：Back/ Forward in application : ⌘+[   / ⌘+]
* ######    任意位置创建新的文件夹：Create a new folder from anywhere:  ⌘+⇧+N   (Desktop/ finder/ save as dialog)

Learning UNIX for OS X  Dave Taylor
mdfind
open
ssh

rm -i .[^.]*  // matches all hidden files except . or ..
du -s *   .[^.]*
df -h
df -H  // 1000 instead of 1024
chmod ug=rw *
chomd go= dirname
chmod go-rwx dirname
chmod u=rwx,go=rx dirname

groups

chgrp
chown
mv *.{jpg, JPG}   jpg\
mkdir -p spy/ch{01,02,03,04,05,intro,toc,index,bio}
cp -i ../john/ch[1-3].doc Documents


grep -s firewall *

m2u  
u2m

tar c|x
tar -czvf ...
tar -xzvf ...
