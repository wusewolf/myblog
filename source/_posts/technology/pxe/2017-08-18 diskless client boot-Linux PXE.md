---
layout: post
title: Linux pxe servers构建方法推荐(centos7)     
date:   2017-08-18 14:55:11
category: "技术"
tags: "PXE" 
---

## Linux recommended pxe server build steps   
   

- **Recommended method:** [simple steps to build PXE server with centos7](https://www.server-world.info/en/note?os=CentOS_7&p=pxe&f=4)

- PXE Client boot flowsheet:  **kernel(dhcp,tftp)->initramfs(tftp)->nfsroot(nfs)**

## Some tips
1. copy kernel from host
2. build your custom initramfs with dracut tools 
3. use yum groups and [fe]debootstrap to install rootfs files 
4. avoid typing erros


