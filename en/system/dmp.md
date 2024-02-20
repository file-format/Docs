{
  "date": "2021-07-07",
  "keywords": [
    "DMP",
    "extension",
    "file",
    "format",
    "system",
    "MemoryDump",
    "Minidump",
    "programs",
    "computer",
    "application"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "DMP - MemoryDump File Format",
  "description": "Learn about DMP file format and APIs that can create and open DMP files.",
  "linktitle": "DMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dmp"
    }
  },
  "lastmod": "2021-07-07"
}

## What is a DMP file? ##

The DMP file is primarily associated with the MemoryDump or Minidump file format. It is used in Microsoft Windows operating system to store data that has been dumped from the memory space of the computer. Usually, DMP files are created when a file crashes or an error occurs. At times DMP files are very important for technical experts or advanced computer users to troubleshoot the problems you are facing and solve any kind of application issue. The DMP files are stored as a proprietary format in Microsoft which is used by the operating system to debug any application installed on the system.


## Technical Specification of DMP File Format

In Windows, the "savedump.exe" system tool generates .dmp files which can be then processed by various debugging utilities available. Mini dump (64/128 Kb) is stored by windows at the '%SystemRoot%\Minidump' directory. On the other hand, the kernel memory and full memory dumps are stored at the system root as 'Memory.dmp' files. Memory dump files are relatively large files, hence can take a sufficient amount of storage space. So it is advised that the useless .dmp files that you think won't be useful for troubleshooting problems then delete them.

You can delete .dmp files either manually or by using the default "clean disk wizard" on your computer. DMP extensions are used by the Oracle database products to use the .dmp files in backup and recovery database files created and used. The DMP files created by Oracle are database backups that can be used for importing or restoring into a running database instance through a database server. In most cases, .dmp files have time and date stamps as their filenames.

### Contents of DMP File

A memory dump file contains:

* The stop statement and its parameters;
* A list of loaded drivers;
* The processor's context (PRCB) for the processes that halted the normal operation of Windows;
* The kernel context and processor information (EPROCESSES) for the processes that have been halted;
* The kernel context and processor information (ETHREAD) for the thread that halted;
* The kernel-mode call stack for the thread that ended the process from performing.


## DMP Example

The stop error 0XC0000218 (Registry_File_Failure) creates a DMP file as follow:

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

## Reference ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)
