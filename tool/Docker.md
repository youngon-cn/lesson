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
