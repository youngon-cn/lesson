# Docker

### 安装
#### Ubuntu 系列安装 Docker

Ubuntu 14.04 版本系统中已经自带了 Docker 包，可以直接安装。

`apt-get install -y docker.io`

`ln -sf /usr/bin/docker.io /usr/local/bin/docker`

``sed -i '$acomplete -F _docker docker' /etc/bash_completion.d/docker.io``

14.04 之前版本 需要先更新内核。


启动docker:`service docker start`
#### CentOS 系列安装 Docker

##### CentOS6

`yum install http://mirrors.yun-idc.com/epel/6/i386/epel-release-6-8.noarch.rpm`

`yum install docker-io`

##### CentOS7
` yum install docker`

启动docker:
`service docker start`

`chkconfig docker on`


### ps:安装完了下面是教程先说说我的使用感觉吧
> Docker 的概念里面有 ``镜像`` `容器` `仓库`

> ``镜像`` `容器` 我觉得这两个就是一个东西 而且很像git的不同版本

>`仓库` 就跟github一个样


### 获取镜像
`docker pull`

### 新建并启动
`docker run`
>-t 选项让Docker分配一个伪终端（pseudo-tty）并绑定到容器的标准输入上。

 >-i 则让容器的标准输入保持打开。

### 查看运行的容器
`docker ps`
> -a 显示全部的容器

> -l 显示上一个

### 进入容器
`docker attach`
这是docker自带的方式 别的方法也行 或者ssh
 ##### 切记 退出容器不要用`exit` 或者 `crtl `+ `c` 会顺带把容器关了
 ##### 使用  `crtl `+ `q` + `p`

### 其他
其他也就没啥了 什么删除 重启 都是基本命令
估计还有一个端口的分配这个估计到使用的时候会用的还有就是`boot2docker`好像是建立容器之间的局域网的还有docker原则一容器一进程我就不多说了
