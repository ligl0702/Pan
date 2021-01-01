# Google TV 修改NTP服务器地址

## **adb 工具包地址-** [**下载**](https://drive.google.com/drive/folders/1PIT3issyC3qD_mjt9HRVJkM2qTlphXWk?usp=sharing)\*\*\*\*

注：采用无线adb方式 无需连接数据线 只要保证在同一个局域网即可

 1、打开adb（设置-设备偏好设置-关于-连续点击4次内部版本号，开发者选项-打开usb调试） 

2、连接adb（下载adb工具包-位于网盘） 

```
$ adb connect 192.168.xx.xx
```

3、写入新的ntp服务器地址 

```
$ adb shell settings put global ntp_server ntp1.aliyun.com 
```

{% hint style="info" %}
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

**mac电脑如何使用adb？**

此 问题可以参考我2年前的视频 [https://www.youtube.com/watch?v=ZK9rJ5w0W4o](https://www.youtube.com/watch?v=ZK9rJ5w0W4o)

也可以参考此人简书：[https://www.jianshu.com/p/1b3fb1f27b67](https://www.jianshu.com/p/1b3fb1f27b67)



