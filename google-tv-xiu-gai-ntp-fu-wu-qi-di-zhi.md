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





