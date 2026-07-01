---
title: 基于VMware安装CentoOS7搭建宝塔面板
published: 2022-06-18
pinned: false
tags: [CentOS7, VMware, 宝塔]
category: 技术分享
draft: false
image: https://api.boxmoe.com/random.php?7
---

最近专业结课作业要求使用虚拟机搭建VPN服务器连接外网和内网，做完之后想到还可以使用虚拟机安装 Linux 系统来搭建本地服务器

首先下载VMware，在这里我们下的是官方版本 [官方下载](https://www.vmware.com/cn/products/workstation-pro/workstation-pro-evaluation.html)

![](https://image.x1anyu.cn/PicGO/202206211100667.png)

然后我们下载CentOS7 [官方下载](https://www.centos.org/download/)

![](https://image.x1anyu.cn/PicGO/202206211207362.png)

![](https://image.x1anyu.cn/PicGO/202206211206686.png)

在列表里的是国内镜像站，随便选一个，这里我们选择阿里的

![](https://image.x1anyu.cn/PicGO/202206211211370.png)

第一个是直接下载镜像文件，第二个是下载文件种子

如果你觉得直接下载太慢可以下种子用迅雷下载

现在打开虚拟机，新建虚拟机

![](https://image.x1anyu.cn/PicGO/202206211213534.png)

![](https://image.x1anyu.cn/PicGO/202206211214262.png)

选择安装程序光盘映像文件，在浏览里选择你下载好的映像文件

![](https://image.x1anyu.cn/PicGO/202206211216143.png)

![](https://image.x1anyu.cn/PicGO/202206211217334.png)

![](https://image.x1anyu.cn/PicGO/202206211218357.png)

根据自己需求来选择磁盘大小

![](https://image.x1anyu.cn/PicGO/202206211219930.png)

到这一步我们点击自定义硬件

![](https://image.x1anyu.cn/PicGO/202206211220968.png)

![](https://image.x1anyu.cn/PicGO/202206211220967.png)

![](https://image.x1anyu.cn/PicGO/202206211244926.png)

内存和处理器根据自己的需求来选择，点击网络适配器选择NAT模式，再然后将打印机设备移除

做完就可以关闭完成安装了

进入系统后显示login，这是让你输入账号

输入账号后回车会让你输入密码

![](https://image.x1anyu.cn/PicGO/202206211257842.png)

登陆成功之后输入su切换到root权限，同样要输入密码

![](https://image.x1anyu.cn/PicGO/202206211328719.png)

切换到root权限后输入下面的安装命令

```
yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh ed8484bec
```

![](https://image.x1anyu.cn/PicGO/202206211333216.png)

这里输入y按回车

![](https://image.x1anyu.cn/PicGO/202206211341487.png)

安装完成之后显示如图，因为我们是虚拟机，所以我们访问的是第二个地址，也就是 http://192.168.236.135:8888/3d752248

当然还有一种可能，就是内网地址也显示不正确，那么我们需要输入ip a来查看适配器的ip地址

![](https://image.x1anyu.cn/PicGO/202206211339348.png)

我们真正的ip是192.168.236.135，我们现在的地址是正确的的，那么现在可以使用浏览器访问了

![](https://image.x1anyu.cn/PicGO/202206211346343.png)

输入宝塔提供的账号密码登陆

进去后注册宝塔账号绑定

![](https://image.x1anyu.cn/PicGO/202206211353790.png)

安装套件选择Nginx，等待安装完成之后即搭建完成