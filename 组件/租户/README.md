在SiteWhere中最为核心的组件：租户。从sitewhere官方文档中可以看出租户在系统中起着至关重要的作用，除了全局配置之外几乎所有的配置都是关于租户的。租户的配置项也是最多的。

直接租户数据管理方式：

 1. **MongoTenantManagement**（sitewhere-mongodb）
  - hbase操作数据存储
 - **HBaseTenantManagement**（sitewhere-hbase）
  - hbase操作数据存储
 - **TenantManagementDecorator**（sitewhere-core）
  - 好像就是个委托