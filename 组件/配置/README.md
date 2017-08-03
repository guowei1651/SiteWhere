# 配置管理组件

配置管理与sitewhere-spring下的sitewhere.xsd和sitewhere-tenant.xsd有关。这里提供了很多sitewhere对外部扩展的支持，提高了sitewhere的灵活性。

sitewhere的配置方式使用对spring的配置文件进行扩展完成。主要扩展内容都在sitewhere-spring包下，这个包负责解析配置文件。

这里使用扩展spring配置文件的方式来实现。具体可以参见[Dubbo中对Spring配置标签扩展] [1], [基于Spring可扩展Schema提供自定义配置支持] [2]

### 用于发现配置的组件： 

 1. **SiteWhereSolrConfiguration**(sitewhere-solr)
     - 设置solr的url
 - **GroovyConfiguration**(sitewhere-groovy)
     - 设置groovyScriptEngine 
 - **SiteWhereMongoClient**(sitewhere-mongodb)
     - 设置mongodb连接 

### Spring配置扩展相关组件： 

 1. **HazelcastDistributedCacheProvider**(sitewhere-core)
 - **MongoInfluxDbTenantDatastore**(sitewhere-wso2)


[1]: http://www.cnblogs.com/ghj1976/p/5379332.html    "Dubbo中对Spring配置标签扩展"
[2]: spring扩展.md "基于Spring可扩展Schema提供自定义配置支持"