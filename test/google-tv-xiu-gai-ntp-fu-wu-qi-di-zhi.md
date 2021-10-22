---
description: 解决方法 通过修改ntp服务器地址 改成国内NTP服务器即可
---

# Google TV /Shield TV/Tivo Stream 4K 已连接无法访问互联网

## ** 方法1：利用电脑**

## **adb 工具包地址- **[**下载**](https://drive.google.com/drive/folders/1PIT3issyC3qD\_mjt9HRVJkM2qTlphXWk?usp=sharing)**  或者**[**github下载地址**](https://github.com/ligl0702/Pan/releases/tag/ADB)****

{% hint style="danger" %}
#### **注意:若你没有科学上网,出现已连接无法访问互联网的提示属于正常**
{% endhint %}

## 如果下面的教程你看不明白，请看 [苦口婆心 版](https://www.bilibili.com/read/cv9486531)   ←

注：采用无线adb方式 无需连接数据线 只要保证在同一个局域网即可

相关视频：[https://www.youtube.com/watch?v=0H27uZYdkxk](https://www.youtube.com/watch?v=0H27uZYdkxk)

&#x20;1、**打开adb**`设置-系统-关于-连续点击4次 Android TV操作系统版本，此时回到系统就有开发者选项-勾选USB调试`

2、**连接adb**（下载adb工具包-位于网盘） 如果有弹框 请点击确定按钮

```
$ adb connect 192.168.xx.xx
```

3、**写入新的ntp服务器地址**&#x20;

```
adb shell settings put global ntp_server ntp3.aliyun.com 
```

{% hint style="success" %}
&#x20;国内ntp服务器 备用地址&#x20;

ntp1.aliyun.com&#x20;

ntp2.aliyun.com&#x20;

ntp3.aliyun.com&#x20;

ntp4.aliyun.com&#x20;

ntp5.aliyun.com&#x20;

ntp6.aliyun.com&#x20;

ntp7.aliyun.com
{% endhint %}

&#x20;      <mark style="color:red;">**如果你没有使用软路由，而是在电视盒子里使用了代理软件比如clash或者其他vpn**</mark>，那么你会发现，即便修改了时间服务器地址，<mark style="color:red;">**每次重启盒子，首先是wifi并不会自动连接，其次就算连接也还是会提示网络受限**</mark>。这是因为Android原生电视盒子的联网原理导致的，源码中有一个叫做isCaptivePortal() 的函数，用来检查网络状况的判断，它需要一个返回值http 204 （空内容的意思）的网址，源码里默认使用 clients3.google.com/generate\_204 这个网址，很显然这个网址，你若没用代理是访问不到的。<mark style="color:red;">**因此安卓就没法正确判断当前的网络状态**</mark>，所以要想解决此问题，需要我们换成一个能在国内直接访问的，用于返回http 204的网址。我们姑且把它叫做 验证服务器 吧。目前已经有很多公司制作了这样的验证服务器。

{% hint style="info" %}
```
小米： connect.rom.miui.com/generate_204
华为： connectivitycheck.platform.hicloud.com/generate_204
Vivo： wifi.vivo.com.cn/generate_204
```
{% endhint %}

#### 具体修改方法：&#x20;

```java
# 打开网络验
//如果你是Android 11.0 以上的电视盒子（还比较少）
adb shell settings put global captive_portal_mode 1

//Android 10.0 以下的电视盒子（比较多）
adb shell settings put global captive_portal_detection_enabled 1

# 设置一个返回204 空内容的服务器
adb shell settings put global captive_portal_use_https 0
adb shell settings put global captive_portal_http_url http://connect.rom.miui.com/generate_204

```

{% hint style="info" %}
<mark style="color:red;">**⬆️注意上述代码中http\_url 后面是空格，不是换行哦**</mark>
{% endhint %}

**如何查看设置的参数？**

```
adb shell settings list global
```

#### **如何恢复原来的参数？**

```
# 使用默认，即删除配置
adb shell settings delete global captive_portal_http_url
adb shell settings delete global captive_portal_https_url
```

****

**4、重启Google TV后生效**

**mac电脑如何使用adb？**

此 问题可以参考我3年前的视频 [https://www.youtube.com/watch?v=ZK9rJ5w0W4o](https://www.youtube.com/watch?v=ZK9rJ5w0W4o)

也可以参考此人简书：[https://www.jianshu.com/p/1b3fb1f27b67](https://www.jianshu.com/p/1b3fb1f27b67)

## 方法2：利用手机app

&#x20;[**利用我开发的安卓手机app 一键修改NTP服务器地址 ←**](../11.md)** **

![](../.gitbook/assets/ntp-up.png)

