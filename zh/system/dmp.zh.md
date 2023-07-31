{
  "date" : "2021-07-07",
  "keywords" :["DMP","扩展","文件","格式","系统","MemoryDump","Minidump","程序","计算机","应用程序"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump 文件格式",
  "description":"了解 DMP 文件格式和可以创建和打开 DMP 文件的 API。",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## 什么是一 .dmp 文件？ ##

DMP 文件主要与 MemoryDump 或 Minidump 文件格式相关联。它用于 Microsoft Windows 操作系统中，用于存储从计算机内存空间中转储的数据。通常，当文件崩溃或发生错误时会创建 DMP 文件。有时 DMP 文件对于技术专家或高级计算机用户解决您面临的问题并解决任何类型的应用程序问题非常重要。 DMP 文件在 Microsoft 中存储为专有格式，操作系统使用该格式来调试系统上安装的任何应用程序。


## DMP 文件格式技术规范

在 Windows 中，“savedump.exe"系统工具生成 .dmp 文件，然后可以通过各种可用的调试实用程序进行处理。小型转储 (64/128 Kb) 由 Windows 存储在“%SystemRoot%\Minidump"目录中。另一方面，内核内存和完整内存转储作为“Memory.dmp"文件存储在系统根目录中。内存转储文件是相对较大的文件，因此可以占用足够的存储空间。因此，建议您认为对解决问题没有用处的无用 .dmp 文件，然后将其删除。

您可以手动删除 .dmp 文件，也可以使用计算机上的默认“清理磁盘向导"。 Oracle 数据库产品使用 DMP 扩展名来使用创建和使用的备份和恢复数据库文件中的 .dmp 文件。 Oracle 创建的 DMP 文件是数据库备份，可用于通过数据库服务器导入或恢复到正在运行的数据库实例中。在大多数情况下，.dmp 文件都有时间和日期戳作为它们的文件名。

### DMP 文件的内容

内存转储文件包含：

* stop 语句及其参数；
* 加载的驱动程序列表；
* 停止 Windows 正常运行的进程的处理器上下文 (PRCB)；
* 已暂停进程的内核上下文和处理器信息（EPROCESSES）；
* 暂停线程的内核上下文和处理器信息（ETHREAD）；
* 结束进程执行的线程的内核模式调用堆栈。


## DMP 示例

停止错误 0XC0000218 (Registry_File_Failure) 创建一个 DMP 文件，如下所示：

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## 参考 ＃＃

* [DMP - 微软](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

