在事件处理下还有更为底层的处理，就是命令处理，过滤器，设备通信层等。

- ```IEventProcessing```接口，启用事件处理管道的系统组件。
- ```EventProcessing```类，实现了```IEventProcessing```。系统中只有这么一个类实现```IEventProcessing```接口。
- ```IDeviceCommandInvocation```

- ```IInboundProcessingStrategy```
- ```IInboundEventProcessorChain```
- ```IOutboundProcessingStrategy```
- ```IOutboundEventProcessorChain```