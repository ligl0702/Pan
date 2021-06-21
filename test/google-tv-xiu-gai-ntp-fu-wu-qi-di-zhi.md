---
description: 解决方法 通过修改ntp服务器地址 改成国内NTP服务器即可
---

# Google TV /Shield TV/Tivo Stream 4K 已连接无法访问互联网

##  **方法1：利用电脑**

## **adb 工具包地址-** [**下载**](https://drive.google.com/drive/folders/1PIT3issyC3qD_mjt9HRVJkM2qTlphXWk?usp=sharing)  **或者**[**github下载地址**](https://github.com/ligl0702/Pan/releases/tag/ADB)\*\*\*\*

{% hint style="danger" %}
#### **注意:若你没有科学上网,出现已连接无法访问互联网的提示属于正常**
{% endhint %}

## 如果下面的教程你看不明白，请看 [苦口婆心 版](https://www.bilibili.com/read/cv9486531)   ←

注：采用无线adb方式 无需连接数据线 只要保证在同一个局域网即可

相关视频：[https://www.youtube.com/watch?v=0H27uZYdkxk](https://www.youtube.com/watch?v=0H27uZYdkxk)

 1、**打开adb**`设置-系统-关于-连续点击4次 Android TV操作系统版本，此时回到系统就有开发者选项-勾选USB调试`

2、**连接adb**（下载adb工具包-位于网盘） 如果有弹框 请点击确定按钮

```
$ adb connect 192.168.xx.xx
```

3、**写入新的ntp服务器地址** 

```
$ adb shell settings put global ntp_server ntp1.aliyun.com 
```

{% hint style="success" %}
 备用地址 

dns1.synet.edu.cn 

news.neu.edu.cn 

dns.sjtu.edu.cm 

dns2.synet.edu.cn 

ntp.glnet.edu.cn 

ntp1.aliyun.com 

ntp2.aliyun.com 

ntp3.aliyun.com 

ntp4.aliyun.com 

ntp5.aliyun.com 

ntp6.aliyun.com 

ntp7.aliyun.com
{% endhint %}

**4、重启Google TV后生效**

**mac电脑如何使用adb？**

此 问题可以参考我2年前的视频 [https://www.youtube.com/watch?v=ZK9rJ5w0W4o](https://www.youtube.com/watch?v=ZK9rJ5w0W4o)

也可以参考此人简书：[https://www.jianshu.com/p/1b3fb1f27b67](https://www.jianshu.com/p/1b3fb1f27b67)

## 方法2：利用手机app

 [**利用我开发的安卓手机app 一键修改NTP服务器地址 ←**](../11.md) ****



