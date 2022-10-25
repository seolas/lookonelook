### 环境

> IDEA 2019.3.3
> Tomcat 6.0.29 ==> Tomcat 8.5.57

### 问题

网站可以运行起来，但是点击里面的功能时报错：

![image](https://user-images.githubusercontent.com/59484008/93288988-bac6a580-f80f-11ea-8df9-d9fac36339fb.png)

### 原因

> 参考链接：https://blog.csdn.net/jyxmust/article/details/73743749

使用的 Tomcat 6，不支持 JDK8 版本

### 解决

改为 Tomcat 8 版本，再运行

