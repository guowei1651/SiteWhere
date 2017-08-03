## 版本检查

先解决问题与总结中所提出的问题：CE是Community Edition的意思，EE是Enterprise Edition的意思。

在[SiteWhere概述] [1]中有一节Build vs. Buy。这一节中介绍SiteWhere的两个版本。以及他们开发情况。

版本检查的内容由几个部分实现：1.SiteWhere系统启动，获取版本检查对象；2.SiteWhere生命周期过程中，使用executor启动版本检查对象。3.执行Runnable的run方法。

**类图**:

![baidu] [2]

**版本检查**:

1. 初始化```VersionChecker```，创建```RestTemplate```对象。
- 运行run方法。
 1. 使用```VersionHelper```类的静态方法```getVersion```获取当前版本类型。在这个方法中用来区分跟系统是CE还是EE。
 - 使用```RestTemplate```对象向 http://www.sitewhere.org/version.php 提交post请求。
 - 获取到的结果
```json
{ "products": [ { "type": "server", "name": "SiteWhere CE", "edition": "Community", "currentVersion": "1.4.0" } ] }
```
 - 解析json数据为```LatestVersion```，获取所有的版本。
 - 比较当前版本与从sitewhere官网获得的版本比较，如果当前版本比官网版本小就直接打印提示更新。
 - 没有就直接完成退出。

[1]: http://www.sitewhere.org/documentation/overview/ "SiteWhere概述"
[2]: /组件/版本检查/SiteWhere版本.jpg "类图"