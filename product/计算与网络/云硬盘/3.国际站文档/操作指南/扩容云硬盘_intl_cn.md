云硬盘是云上可扩展的存储设备，用户可以在创建云硬盘后随时扩展其大小，以增加存储空间，同时不失去云硬盘上原有的数据。要达到扩容并使用扩容空间的目的，用户需要扩容实体云硬盘大小，然后扩展其上的文件系统以识别新近可用的空间。

> 如果云硬盘的最大容量（4T）都无法满足您的需求，您可以使用 RAID 跨多个物理硬盘来创建一个逻辑上的超大空间。有关更多信息，请参阅 [配置云硬盘 RAID 组](/document/product/362/2932)。

## 扩容弹性云盘
### 通过控制台扩容弹性云盘

1) 打开云服务器 [CVM控制台](https://console.cloud.tencent.com/cvm)。

2) 单击导航窗格中的【云硬盘】。

3) 只有显示为【未挂载】状态且【支持挂载/卸载】的硬盘可以扩容（即未挂载状态的弹性云盘），点击末尾【更多】-【扩容】按钮，选择需要的新大小（必须大于或等于当前大小）并支付即完成了实体硬盘的扩容操作。

> 对于已经连接到了实例的弹性云盘请先执行 [卸载云硬盘](/doc/product/362/6740) 操作

### 通过API扩容弹性云盘
请参考 [ResizeCbsStorage 接口](https://cloud.tencent.com/doc/api/364/2527)。

## 扩容非弹性云硬盘
### 通过控制台扩容非弹性云盘
1) 打开云服务器 [CVM控制台](https://console.cloud.tencent.com/cvm)。

2) 单击导航窗格中的【云主机】。

3) 只有显示为【关机】状态且系统盘、数据盘均为云硬盘的实例可以扩容，点击末尾【更多】-【云主机设置】-【调整硬盘】按钮，选择需要的新大小（必须大于或等于当前大小）并支付即完成了实体硬盘的扩容操作。

> 对于正在运行的系统盘、数据盘均为云硬盘的实例，需要扩容请先执行 [实例关机](/doc/product/213/4929) 操作。

### 通过API扩容非弹性云盘
请参考 [ResizeInstance 接口](https://cloud.tencent.com/doc/api/229/1306) 和 [ResizeInstanceHour 接口](https://cloud.tencent.com/doc/api/229/1344)。