hominlinx.go.blog
=================

####my blog using golang 

我是参考了golang官方博客，修改而成。由于十一白天加班，晚上我加入了两篇我以前
用印象笔记写的文章，在本地部署成功。
今天（10.2号），采用Heroku进行了临时部署，参考文章[Getting Started with Go 
on Heroku](http://mmcgrana.github.io/2012/09/getting-started-with-go-on-heroku.html)

####计划

计划使用[beego](https://github.com/astaxie/beego) 慢慢的详细的学学这个框架。

####感谢

感谢我的女朋友，这个十一是我们工作后的第一个十一，本来出去玩，但是由于我要紧急
搭建一个博客，所以女朋友跟我一起在家宅了一天。谢谢她的理解。

####梦想

能够加入一个创业团队，试着做一些真正有意义的事情。

####Go1.1安装
由于ubuntu本身不是Go1.1，所以采用源码安装。
    $ cd ~
    $ mkdir golang
    $ cd golang
    $ wget http://go.googlecode.com/files/go1.1.linux-amd64.tar.gz
    $ tar zxf go1.1.linux-amd64.tar.gz
    $ cd ~
    $ ln -s golang/go1.1 go
    $go version

####Go环境配置

建立Go的代码代码放置路径：
    mkdir -p $HOME/mygo

配置Go的环境变量：GOPATH，添加如下代码到$HOME/.bashrc；

   export GOROOT=$HOME/go

   export GOPATH=$HOME/mygo
   
   export PATH=${PATH}:${GOPATH}/bin:$GOROOT/bin

   export GOARCH=amd64

   export GOOS=linux

$source ~/.bashrc

####运行

    $cd ~/mygo
    $mdir src 
    $cd src
    $git clone https://github.com/hominlinx/hominlinx.go.blog
    $go get

    这个时候在mygo下面有bin的文件夹。在里面执行hominlinx.go.blog即可
    在浏览器里面：127.0.0.1:8080 即可访问

####部署

使用[Heroku](https://www.heroku.com)进行部署

1. 注册
2. 登陆
    $heroku login
3. git push heroku master



    


