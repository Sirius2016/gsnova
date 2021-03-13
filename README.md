## gsnova使用教程

#### gsnova服务端配置

- 服务端监听quic、tls、kcp、http、http2协议
- 服务端需要开放端口：
  - tcp端口: 48100、48101、48102、48103
  - udp端口：48100、48101

- 服务端启动命令

```
gsnova -cmd -server -listen tcp://:48100 -listen quic://:48100 -listen tls://:48101 -listen kcp://:48101 -listen http://:48102 -listen http2://:48103  -key 809240d3a021449f6e67aa73221d42df942a308a -user "*"
```

#### gsnova客户端启动命令

```
#quic协议
gsnova -cmd -client -listen :48100 -remote quic://2.2.2.2:48100  -key 809240d3a021449f6e67aa73221d42df942a308a

#http协议
gsnova -cmd -client -listen :48100 -remote http://2.2.2.2:48102  -key 809240d3a021449f6e67aa73221d42df942a308a

#kcp协议
gsnova -cmd -client -listen :48100 -remote kcp://2.2.2.2:48101  -key 809240d3a021449f6e67aa73221d42df942a308a

#tcp协议
gsnova -cmd -client -listen :48100 -remote tcp://2.2.2.2:48100  -key 809240d3a021449f6e67aa73221d42df942a308a

#tls协议
gsnova -cmd -client -listen :48100 -remote tls://2.2.2.2:48101  -key 809240d3a021449f6e67aa73221d42df942a308a

```



#### 知识扩展

> [gsnova项目地址](https://github.com/yinqiwen/gsnova)
>
> [gsnova编译包下载](https://github.com/yinqiwen/gsnova/releases)

