## <center>服务器常见问题</center>

### 1.SSH连接VPS乱码
```shell
[root@host ~]# ll
������ 0
```

```
//安装中文包
[root@host /]# yum install fonts-chinese.noarch
//生成指定编码文件
[root@host /]# localedef -c -f UTF-8 -i zh_CN zh_CN.utf8
//指定字符分类
[root@host /]# export LC_ALL=zh_CN.utf8
//设置系统locale语言
[root@host /]# vim /etc/sysconfig/i18n
    LANG=zh_CN.UTF-8
    LC_ALL=zh_CN.UTF-8
```