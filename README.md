参考文档:  
[nacos-docker/README_ZH](https://github.com/nacos-group/nacos-docker/blob/ac214ac776821dae6a76a7a1ace34eb3081026b3/README_ZH.md)

## 问题描述

启动容器后 nacos 始终无法连接到 mysql, 抛出 `java.lang.IllegalStateException: No DataSource set`, 无论 `MYSQL_SERVICE_HOST`
指定的服务名还是 `container_name`  
因为 `restart` 存在不停的重启重试, 始终失败. 参考 [nacos.log](log/nacos/nacos.log)

**直到我在容器外部主动连接到mysql (我用的 IDEA 的数据库工具, 本质就是JDBC连接), 在下一次重试时才能连接成功**

[compose.yaml](nacos-test/compose.yaml) 我不明白是哪里出了问题

## 环境

docker

```
Client: Docker Engine - Community
 Version:           25.0.0-beta.1
  Version:          25.0.0-beta.1
  API version:      1.44 (minimum version 1.12)
  Go version:       go1.21.3
  Git commit:       6af7d6e
  Built:            Mon Nov 13 16:49:38 2023
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.25
  GitCommit:        d8f198a4ed8892c764191ef7b3b06d8a2eeb5c7f
 runc:
  Version:          1.1.10
  GitCommit:        v1.1.10-0-g18a0cb0
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

docker compose

```
Docker Compose version v2.23.0
```

OS

```
Linux ll 5.15.133.1-microsoft-standard-WSL2 #1 SMP Thu Oct 5 21:02:42 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux
```
