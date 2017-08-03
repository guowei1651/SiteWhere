

1. ```ITenantConfigurationResolver```接口，租户配置解析接口。
- ```FileSystemTenantConfigurationResolver```抽象类，文件系统配置解析，实现了```ITenantConfigurationResolver```接口。
- ```DefaultTenantConfigurationResolver```继承自```FileSystemTenantConfigurationResolver```类，在租户引擎中使用这个类来进行租户配置解析。
- ```TomcatTenantConfigurationResolver```继承自```FileSystemTenantConfigurationResolver```类，这个类看起来像是tomcat租户配置解析，但是从代码上看没有直接应用，之后接触到再说。