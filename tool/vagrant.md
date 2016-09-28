# vagrant

>下载地址：http://downloads.vagrantup.com/ 根据提示一步步安装。

此外，还得下载官方封装好的基础镜像：

Ubuntu precise 32 VirtualBox `http://files.vagrantup.com/precise32.box`

Ubuntu precise 64 VirtualBox `http://files.vagrantup.com/precise64.box`

如果你要其他系统的镜像，可以来这里下载 `http://www.vagrantbox.es/``


```shell

  vagrant init  # 初始化
  vagrant up  # 启动虚拟机
  vagrant halt  # 关闭虚拟机
  vagrant reload  # 重启虚拟机
  vagrant ssh  # SSH 至虚拟机
  vagrant status  # 查看虚拟机运行状态
  vagrant destroy  # 销毁当前虚拟机

```
打包  `` vagrant package ``
打包完成后会在当前目录生成一个 `package.box` 的文件，将这个文件传给其他用户，其他用户只要添加这个 box 并用其初始化自己的开发目录就能得到一个一模一样的开发环境了。
### 注意事项

使用 Apache/Nginx 时会出现诸如图片修改后但页面刷新仍然是旧文件的情况，是由于静态文件缓存造成的。需要对虚拟机里的 Apache/Nginx 配置文件进行修改：

### Apache 配置添加:
EnableSendfile off

### Nginx 配置添加:
sendfile off;
