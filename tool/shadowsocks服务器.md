# shadowsocks服务器搭建
---
`shadowsocks`服务器搭建

`shadowsocks`是基于`python`开发需要安装`python`环境和 `pip` 包管理

#### 默认环境已经安装

#### pip安装shadowsocks
`pip install shadowsocks`

安装完毕创建一个文件`ss.json`(去除注释)
```javascript
{ 
 "server": "104.128.237.85", // 服务器地址
 "server_port": 8388, // 端口
 "local_address": "127.0.0.1",
 "local_port": 1080, 本地 端口
 "port_password": {  // 配置多个端口和密码
    "9000": "nobey",
    "9001": "nobey",
    "9002": "nobey",
    "9003": "nobey",
    "9004": "nobey"
  },
 "password": "nobey", // 密码
 "timeout": 600,
 "method": "aes-256-cfb"  // 加密方式
}

```
#### 启动:`ssserver -c ss.json -d start `
- ``－c`` 是加载配置文件
- ``－d`` 是进入后台开启
