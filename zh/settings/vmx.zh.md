{
"date": "2023-06-08",
  "keywords": [
"vmx 文件",
"什么是 vmx 文件",
"vmx 文件示例",
"如何打开 vmx 文件",
"vmx 文件包含什么",
"vmx 文件的格式是什么",
"文件",
"vmx 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "VMX 文件格式 - VMware 虚拟机配置文件",
  "description":"了解 VMX 格式以及可以创建和打开 VMX 文件的 API。",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## 什么是一 .vmx 文件？

VMX 文件也称为虚拟机配置文件,是 VMware 虚拟化软件用来定义虚拟机 (VM) 设置和配置的纯文本文件。 VMX 文件包含 VM 的硬件配置,虚拟磁盘映射,网络设置和其他参数等信息。

## VMX 文件示例

以下是 VMX 文件的示例：

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## VMX 文件包含什么？

VMX 文件包含虚拟机 (VM) 的各种配置设置。以下是 VMX 文件中的一些常见设置：

- `.encoding:` 指定文件中使用的字符编码。
- `config.version:` 指示 VMX 文件格式的版本。
- `virtualHW.version:` 指定 VM 的虚拟硬件版本。
- `guestOS：` 指定虚拟机中安装的来宾操作系统。
- `memSize:` 定义分配给虚拟机的内存量。
- `displayName:` 设置虚拟机的显示名称或标签。
- `powerType:` 定义不同操作的电源行为（关闭电源,打开电源,重置,挂起）。
- `floppyX：` 与软盘驱动器相关的配置设置,例如存在和文件映射。
- `numvcpus:` 指定分配给 VM 的虚拟 CPU 数量。
- `scsiX：` SCSI 控制器及其关联虚拟磁盘的配置设置。
- `ethernetX：` 网络适配器的配置设置,包括虚拟设备类型,网络名称和地址类型。
- `ideX:` IDE 控制器及其关联虚拟磁盘的配置设置。
- `usbX：` USB 设备的配置设置,例如存在和连接详细信息。
- `声音：` 虚拟声音适配器的配置设置。
- `tools.syncTime:` 指示是否启用与主机系统的时间同步。
- `uuid.bios:` 指定虚拟机的 BIOS UUID。
- `uuid.location:` 指定 VM 的位置 UUID。

## 如何打开 VMX 文件？

不建议手动打开 VMX 文件。当您使用 VMware Fusion 运行虚拟机时,该软件会自动从 VMX 文件加载信息。

但是,如果您想手动编辑 VMX 文件,可以使用任何文本编辑器,例如记事本 (Windows) 或 TextEdit (Mac)。

## VMX 文件的格式是什么？

VMX 文件是具有特定格式的纯文本文件。该格式遵循键值对结构,其中每一行代表单独的配置选项。

VMX文件的一般格式如下：

```
key1 = value1
key2 = value2
key3 = value3
```

每行由键,后跟等号 (=) 和相应的值组成。键代表特定的配置设置,值代表分配给该设置的值。

例如,VMX 文件中的 `memSize = "8192"` 指定虚拟机内存限制为 8192MB RAM。

VMX 文件的格式还可能包含注释,在行开头用井号 (#) 表示,VMware 软件在解析文件时会忽略这些注释。注释通常用于为特定设置提供附加信息或解释。

## 参考
* [示例 VMX 文件](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




