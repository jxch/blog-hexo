---
title: shadowsocks部署
date: 2022-11-18 08:47:16
categories: 使用手册
tags: 流量转发
---
# shadowsocks 服务端
## docker-compose.yml
```yaml
  shadowsocks: 
    image: appso/shadowsocks-libev 
    ports: 
      - 12346:12346
      - 12346:12346/udp 
    volumes: 
      - ./shadowsocks:/etc/shadowsocks-libev
```

## config.json
```json
{
    "server":"0.0.0.0",
    "server_port":12346,
    "password":"UUID",
    "timeout":300,
    "method":"aes-256-gcm",
    "fast_open":false,
    "mode":"tcp_and_udp"
}
```


