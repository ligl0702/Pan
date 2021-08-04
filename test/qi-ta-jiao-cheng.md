# 其他教程

## 1、编辑ttyd代码

```
 vi /etc/init.d/ttyd
```

{% hint style="success" %}
 技巧：输入/ 来搜索字符串  ，然后输入N 可以查找下一处，在输入N可以查找下下处
{% endhint %}

## 2、注释代码

{% code title="将此行代码注释掉，注释符号为 \# 如下所示" %}
```css
# ${interface:+-i $interface} \
```
{% endcode %}

## 3、重启ttyd

```css
 /etc/init.d/ttyd restart 
```



