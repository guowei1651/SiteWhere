# 启动过程
**启动过程** 和 **生命周期启动** 都是在SiteWhere.start中顺序调用完成。

从sitewhere-server-1.8.0.zip解压结果中可以找到sitewhere.war包。从sitewhere.war包中可以找到META-INF/MANIFEST.MF
```
Manifest-Version: 1.0
Start-Class: com.sitewhere.web.SiteWhereWebApplication
Spring-Boot-Version: 1.3.2.RELEASE
Main-Class: org.springframework.boot.loader.WarLauncher
```
从上可知，系统的启动函数是类是com.sitewhere.web.SiteWhereWebApplication。从该类可以很见到的找到SiteWhereServer的启动类是SiteWhereApplication。

## 过程
- **SiteWhereApplication的启动过程**
 1. 使用SiteWhere的静态方法start进入启动过程。
 - 在SiteWhere中获取SiteWhereServer类型，并创建SiteWhereServer类型对象
 - 对SiteWhereServer对象调用initialize方法
 - 对SiteWhereServer对象调用lifecycleStart方法
