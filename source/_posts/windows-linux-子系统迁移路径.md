---
title: windows linux 子系统迁移路径
date: 2022-12-30 04:21:35
categories: 使用手册
tags: 虚拟化
---

1. `wsl -l -v` 查看需要迁移的子系统
2. `wsl --export  docker-desktop-data D:\virtual\docker-desktop-data.tar` 导出子系统
3. `wsl --unregister docker-desktop-data` 注销子系统
4. `wsl --import docker-desktop-data D:\virtual\docker-desktop-data D:\virtual\docker-desktop-data.tar --version 2` 导入子系统
5. 删除`tar`文件: `D:\virtual\docker-desktop-data.tar`
6. `wsl -l -v` 查看是否导入成功
