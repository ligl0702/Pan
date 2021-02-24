---
description: ​《让玩客云不再下蛋 安静做NAS 联动软路由 曲线实现tr下载 随时随地高速观影》
---

# 玩客云技巧

{% embed url="https://youtu.be/MP5jo4bsROs" %}

\*\*\*\*[**《让玩客云不再下蛋 安静做NAS 联动软路由 曲线实现tr下载 随时随地高速观影》**](https://www.ixigua.com/6932813391962571272)\*\*\*\*

## 在linux上做的3件事

1、 把玩客云的硬盘格式化为ext4

 2、 新建文件夹： `mkdir .onething_data` 

3、 给文件夹加权限 sudo chattr +i .onething\_data

## 在OpenWrt下做2件事 

1、新建文件夹 mkdir movie 

2、挂载玩客云的硬盘： 

`mount -t cifs -o username=root,password=123456 //192.168.6.181/e503/onecloud/tddownload /movie`

## 在玩客云app做2件事

 1、设置磁盘共享大小为 0 GB 

2、开启Sambe共享 设置用户名root 密码123456

虚拟机下载地址：[https://www.vmware.com/products/fusion/fusion-evaluation.html](https://www.vmware.com/products/fusion/fusion-evaluation.html) 

Ubuntu下载地址：[https://releases.ubuntu.com/18.04/](https://releases.ubuntu.com/18.04/)



