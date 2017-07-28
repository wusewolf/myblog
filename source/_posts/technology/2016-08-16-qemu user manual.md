---
layout: post
title:  QEMU用户手册和使用
date:   2016-08-16 15:33:11
category: "技术"
tags: QEMU
---
##QEMU的使用
----------------
1. 串口显示  
` qemu-system-x86_64   -kernel  vmlinuz-2.6.32-358.el6.x86_64  -initrd  initramfs-nfs.img  -nographic -append "console=ttyS0"   --enable-kvm -m 1024`


2. [user manual] (/public/doc/qemu-doc.pdf)



