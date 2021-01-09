### git修改user.name 和user.email
 
首先进入git bash
 
0：
输入
$ git config --list 
 
可以查看配置的一些东西。可以看到user.name 和user.email  分别是什么。。
如果你没有初始化过。那么直接：
$  git config --global user.name "输入你的用户名"
$  git config --global user.email "输入你的邮箱"
 
这样就可以初始化了。
1:
如果你已经初始化过了，但是不小心把邮箱和用户名输错了，那么就要修改了。
我看到网上有人说继续$ git config --global user.name "输入你的用户名"或者 $ git config --global user.email "输入你的邮箱" 来修改邮箱和密码。我尝试了一下，是不行的（至少在window10的环境下）会给出这样的错误：
warning: user.name has multiple values
error: cannot overwrite multiple values with a single value
       Use a regexp, --add or --replace-all to change user.name.
 
这边给出了--repalce-all 这个东西。
 
然后我尝试着用
$  git config --global --replace-all user.email "输入你的邮箱" 
$  git config --global --replace-all user.name "输入你的用户名"
 
然后再查看下
$  git config --list 
发现修改成功了。
 
2:
再说说git bash和git cmd的区别啊。。简单一句话，，git cmd是git bash的子集。所以直接用git bash就行了。 然后git gui是图形界面。

Git 
版本控制工具，支持该工具的网站有Github、BitBucket、Gitorious、国内的osChina仓库、csdn仓库等等。

shell
是Linux、unix系统的外壳，也可以理解为命令行，就是你输入并执行命令的地方，git通过命令行和图形界面两种方式使用shell。

bash
是shell的一种，最常用的shell之一。

git Bash
方便你在windows下使用git命令的模拟终端（windows自带的cmd功能太弱）linux、unix可以直接使用git。

git shell
它是安装了git的shell，bash是一种shell。
