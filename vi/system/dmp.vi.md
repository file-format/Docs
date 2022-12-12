{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "phần mở rộng", "tệp", "định dạng", "hệ thống", "MemoryDump", "Minidump", "chương trình", "máy tính", "ứng dụng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - Định dạng tệp MemoryDump",
  "description":"Tìm hiểu về định dạng tệp DMP và các API có thể tạo và mở tệp DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Tệp DMP là gì? ##

Tệp DMP chủ yếu được liên kết với định dạng tệp MemoryDump hoặc Minidump. Nó được sử dụng trong hệ điều hành Microsoft Windows để lưu trữ dữ liệu đã được kết xuất từ không gian bộ nhớ của máy tính. Thông thường, tệp DMP được tạo khi tệp gặp sự cố hoặc xảy ra lỗi. Đôi khi, các tệp DMP rất quan trọng đối với các chuyên gia kỹ thuật hoặc người dùng máy tính nâng cao để khắc phục sự cố bạn đang gặp phải và giải quyết mọi loại sự cố ứng dụng. Các tệp DMP được lưu trữ dưới dạng định dạng độc quyền trong Microsoft, định dạng này được hệ điều hành sử dụng để gỡ lỗi bất kỳ ứng dụng nào được cài đặt trên hệ thống.


## Thông số kỹ thuật của định dạng tệp DMP

Trong Windows, công cụ hệ thống "savedump.exe" tạo ra các tệp .dmp mà sau đó có thể được xử lý bằng nhiều tiện ích sửa lỗi có sẵn. Kết xuất nhỏ (64/128 Kb) được các cửa sổ lưu trữ tại thư mục '%SystemRoot%\Minidump'. Mặt khác, bộ nhớ nhân và các kết xuất bộ nhớ đầy đủ được lưu trữ tại thư mục gốc của hệ thống dưới dạng các tệp 'Memory.dmp'. Các tệp kết xuất bộ nhớ là các tệp tương đối lớn, do đó có thể chiếm đủ dung lượng lưu trữ. Vì vậy, bạn nên xóa các tệp .dmp vô ích mà bạn nghĩ sẽ không hữu ích cho việc khắc phục sự cố.

Bạn có thể xóa các tệp .dmp theo cách thủ công hoặc bằng cách sử dụng "trình hướng dẫn đĩa sạch" mặc định trên máy tính của mình. Các phần mở rộng DMP được các sản phẩm cơ sở dữ liệu Oracle sử dụng để sử dụng các tệp .dmp trong các tệp cơ sở dữ liệu sao lưu và phục hồi được tạo và sử dụng. Các tệp DMP do Oracle tạo là các bản sao lưu cơ sở dữ liệu có thể được sử dụng để nhập hoặc khôi phục vào một phiên bản cơ sở dữ liệu đang chạy thông qua một máy chủ cơ sở dữ liệu. Trong hầu hết các trường hợp, tệp .dmp có dấu thời gian và ngày làm tên tệp.

### Nội dung của tệp DMP

Tệp kết xuất bộ nhớ chứa:

* Câu lệnh dừng và các tham số của nó;
* Một danh sách các trình điều khiển được tải;
* Bối cảnh của bộ xử lý (PRCB) cho các quy trình tạm dừng hoạt động bình thường của Windows;
* Bối cảnh hạt nhân và thông tin bộ xử lý (EPROCESSES) cho các quy trình đã bị tạm dừng;
* Bối cảnh hạt nhân và thông tin bộ xử lý (ETHREAD) cho luồng đã tạm dừng;
* Ngăn xếp cuộc gọi chế độ hạt nhân cho luồng đã kết thúc quá trình thực hiện.


## Ví dụ DMP

Lỗi dừng 0XC0000218 (Registry_File_Failure) tạo tệp DMP như sau:

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

## Tài liệu tham khảo ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

