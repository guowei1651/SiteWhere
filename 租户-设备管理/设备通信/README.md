基本设备通信子系统是SiteWhere的最底层系统。我们就从SiteWhere最低层逐层的向上一层一层的解析整个SiteWhere系统。

设备通信子系统，也分了很多层次。

在SiteWhere系统架构中，可以看到SiteWhere最底层分了两个部分：Event Source，Command Destinations。从SiteWhere源代码级别可以找到几个接口：

1. ```IInboundEventSource```接口，用来表示系统架构中的事件源。
- ```ICommandDestination```接口，用来表示系统架构中的命令目标。

有了专门管理具体通信的两个接口，需要有管理通信接口,并完成向事件处理、转发等的消息递交。

1. ```IDeviceCommunication```接口，主要是定义设备通信接口。

