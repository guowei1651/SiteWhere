## JvmHistoryMonitor

在SiteWhere启动过程中，启动了JvmHistoryMonitor。这个类用来检查jvm系统中总内存，free内存。

暂时没有看到这个还有其他作用。在这里先记录相关类： 

1. ```JvmHistoryMonitor```(sitewhere-core)
- ```SiteWhereServerRuntime```(sitewhere-server-api)
- ```ISiteWhereServerRuntime```(sitewhere-server-api)

## ITracer

日志，跟踪等等都是为了调试用的。不过，这里的跟踪不算是跟踪因为从google chubby或者行为跟踪等。而直接就是日志。这里就不对日志做详细介绍了，只简单记录一下关于日志的几个类：

1. ```ITracer```(sitewhere-server-api)
- ```Tracer```(sitewhere-core)
- ```TracerCategory```(sitewhere-server-api)
- ```NullTracer```(sitewhere-server-api)
- ```LoggerTracer```(sitewhere-core)

这里使用log4j进行日志管理。
