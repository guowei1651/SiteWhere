从租户管理中看到关于设备管理的相关接口有很多，我们这里会详细介绍关于设备管理的所有过程。

总体概述：



详细的接口有：

1. ```IEventProcessing```接口，启用事件处理管道的系统组件。可以参见：[设备事件处理] [1]
- ```IDeviceCommunication```接口，用来描述设备通信。可以参见：[设备通信] [2]
- ```IDeviceManagementCacheProvider```接口，为设备管理对象提供缓存的实体接口。可以参见：[设备Cache] [3]
- ```IDeviceManagement```接口，设备管理接口。可以参见：[设备管理] [4]
- ```IDeviceEventManagement```接口，定义设备事件管理。可以参见：[设备事件管理] [5]

[1]: 事件处理/README.md "设备事件处理"
[2]: 设备通信/README.md "设备通信"
[3]: 设备Cache/README.md "设备Cache"
[4]: 设备管理/README.md "设备管理"
[5]: 设备事件管理/README.md "设备事件管理"