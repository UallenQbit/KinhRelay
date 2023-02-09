# KinhRelay

> KinhRelay是使用GoLang开发的高性能流量中继（端口转发）简单的 HTTP API 即可调用

# 功能介绍

- 动态查看规则
- 动态添加规则
- 动态更新规则
- 动态删除规则

- 查看规则流量
- 重置规则流量

- 限制规则最大连接数
- 限制规则最大速率

- 协议屏蔽 (Socks5 And TLS)

- 连接IP白名单

# 待完成
- TLS 加密隧道
- WS 加密隧道
- WSS 加密隧道
- QUIC (0RTT) 加密隧道

# 怎么加快更新
在群里催更岛主

# HTTP-API 文档
点击查看 HTTP-API 文档 [查看](https://github.com/UallenQbit/KinhRelay/blob/main/HTTP-API.md)


# 启动

```
/root/KinhRelay -API_Address="0.0.0.0" -API_Port=443 -API_Path="/"
```

```
/root/KinhRelay-linux-386 -API_Address="[HTTP-API监听地址]" -API_Port=[HTTP-API监听端口] -API_Path="[HTTP-API路径]"
```

```
/root/KinhRelay-linux-amd64 -API_Address="[HTTP-API监听地址]" -API_Port=[HTTP-API监听端口] -API_Path="[HTTP-API路径]"
```

```
/root/KinhRelay-linux-arm -API_Address="[HTTP-API监听地址]" -API_Port=[HTTP-API监听端口] -API_Path="[HTTP-API路径]"
```

```
/root/KinhRelay-linux-arm64 -API_Address="[HTTP-API监听地址]" -API_Port=[HTTP-API监听端口] -API_Path="[HTTP-API路径]"
```

```
D:\KinhRelay-windows-386.exe -API_Address="[HTTP-API监听地址]" -API_Port=[HTTP-API监听端口] -API_Path="[HTTP-API路径]"
```

```
D:\KinhRelay-windows-amd64.exe -API_Address="[HTTP-API监听地址]" -API_Port=[HTTP-API监听端口] -API_Path="[HTTP-API路径]"
```

# 性能
### 无转发性能 29.5Gbytes 25.4Gbits/sec
![1-1](https://user-images.githubusercontent.com/72503738/213889538-9205884a-a221-4d4d-b812-284f33a64be3.png)

### 有转发性能 28.6Gbytes 24.5Gbits/sec
![2-2](https://user-images.githubusercontent.com/72503738/213889537-baec9ae5-84d9-44a5-af5e-65aa15e6c66b.png)


# 启动
点击加入Telegram [频道](https://t.me/KinhChannel)
点击加入Telegram [交流群](https://t.me/KinhDownChat)
