---
layout: post
title:  docker安装和简单应用
date:   2017-08-03 13:55:11
category: "技术"
tags: docker
---


# docker安装
## 1.ubuntu14.04.5 环境  
apt-get install docker.io    
或安装社区版 https://download.docker.com/linux/ubuntu/dists/trusty/pool/stable/amd64/docker-ce_17.03.2~ce-0~ubuntu-trusty_amd64.deb


2. Description-en  
Linux container runtime   
Docker complements kernel namespacing with a high-level API which operates at the process level. It runs unix processes with strong guarantees of isolation and repeatability across servers.  
        
Docker is a great building block for automating distributed systems:
large-scale web deployments, database clusters, continuous deployment systems, private PaaS, service-oriented architectures, etc. 
    


## 2.windows安装docker

[win7, win8安装docker需要了解的概念](http://www.docker.org.cn/book/install/win7-win8-install-docker-concept-39.html)



简介：在linux下面安装docker和在windows下面安装docker概念有所不同。

在linux下面安装docker和在windows下面安装docker概念有所不同。通常来讲，linux下面安装docker，你的机器既是localhost，同时也是docker主机。Docker的客户端，docker守候进程和容器都是直接运行在你的localhost机器上面的。因为是在一台机器上，所以你可以使用localhost为你的docker容器做端口映射，比如：localhost:8000或者0.0.0.0:8000。

Linux Architecture Diagram

在window下面安装docker，docker的守候进程和容器是运行在linux虚拟机里面，docker命令则是运行在windows系统里面。

Docker主机的地址是linux虚拟机的地址，它被启动的时候，会分到一个ip地址。当你启动一个容器的时候，容器的端口号会映射到虚拟机的一个端口号。

Windows Architecture Diagram

## 3.docker命令使用

- docker tag设置镜像标签


    root@806RTH:~# docker tag --help
    Usage:  docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]
    Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
    Options:
    --help   Print usage


注意： ** source_image格式为： <font color="red">username/repository name<font> **

    root@806RTH:~# docker images
    REPOSITORY          TAG                               IMAGE ID            CREATED             SIZE
    local               ubuntu14.04_chameleon_build_env   ed9ebadb41c9        2 days ago          714 MB
    root@806RTH:~# docker image tag ed9ebadb41c9  local/ubuntu:ubuntu14.04_chameleon_build_env
    root@806RTH:~# docker images
    REPOSITORY          TAG                               IMAGE ID            CREATED             SIZE
    local/ubuntu        ubuntu14.04_chameleon_build_env   ed9ebadb41c9        2 days ago          714 MB
    local               ubuntu14.04_chameleon_build_env   ed9ebadb41c9        2 days ago          714 MB
