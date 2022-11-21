{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "นามสกุล", "ไฟล์", "รูปแบบ", "ระบบ", "MemoryDump", "Minidump", "โปรแกรม", "คอมพิวเตอร์", "แอปพลิเคชัน" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - รูปแบบไฟล์ MemoryDump",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DMP และ API ที่สามารถสร้างและเปิดไฟล์ DMP",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## ไฟล์ DMP คืออะไร?? ##

ไฟล์ DMP เกี่ยวข้องกับรูปแบบไฟล์ MemoryDump หรือ Minidump เป็นหลัก ใช้ในระบบปฏิบัติการ Microsoft Windows เพื่อเก็บข้อมูลที่ถูกดัมพ์จากพื้นที่หน่วยความจำของคอมพิวเตอร์ โดยปกติแล้ว ไฟล์ DMP จะถูกสร้างขึ้นเมื่อไฟล์ขัดข้องหรือเกิดข้อผิดพลาด ในบางครั้ง ไฟล์ DMP มีความสำคัญมากสำหรับผู้เชี่ยวชาญด้านเทคนิคหรือผู้ใช้คอมพิวเตอร์ขั้นสูงในการแก้ไขปัญหาที่คุณเผชิญอยู่และแก้ไขปัญหาเกี่ยวกับแอปพลิเคชันทุกประเภท ไฟล์ DMP ถูกจัดเก็บเป็นรูปแบบกรรมสิทธิ์ใน Microsoft ซึ่งระบบปฏิบัติการใช้เพื่อดีบักแอปพลิเคชันใด ๆ ที่ติดตั้งบนระบบ


## ข้อกำหนดทางเทคนิคของรูปแบบไฟล์ DMP

ใน Windows เครื่องมือระบบ "savedump.exe" จะสร้างไฟล์ .dmp ซึ่งสามารถประมวลผลได้โดยใช้โปรแกรมแก้ไขจุดบกพร่องที่มีอยู่ การถ่ายโอนข้อมูลขนาดเล็ก (64/128 Kb) ถูกเก็บไว้โดย windows ที่ไดเรกทอรี '%SystemRoot%\Minidump' ในทางกลับกัน หน่วยความจำเคอร์เนลและดัมพ์หน่วยความจำเต็มจะถูกเก็บไว้ที่รูทระบบเป็นไฟล์ 'Memory.dmp' ไฟล์การถ่ายโอนข้อมูลหน่วยความจำเป็นไฟล์ที่ค่อนข้างใหญ่ ดังนั้นจึงอาจใช้พื้นที่จัดเก็บในปริมาณที่เพียงพอ ดังนั้น ขอแนะนำว่าไฟล์ .dmp ที่ไร้ประโยชน์ซึ่งคุณคิดว่าไม่มีประโยชน์ในการแก้ปัญหา ให้ลบออก

คุณสามารถลบไฟล์ .dmp ด้วยตนเองหรือโดยใช้ "ตัวช่วยล้างดิสก์" ที่เป็นค่าเริ่มต้นในคอมพิวเตอร์ของคุณ ส่วนขยาย DMP ถูกใช้โดยผลิตภัณฑ์ฐานข้อมูล Oracle เพื่อใช้ไฟล์ .dmp ในไฟล์ฐานข้อมูลสำรองและกู้คืนที่สร้างและใช้งาน ไฟล์ DMP ที่สร้างโดย Oracle เป็นข้อมูลสำรองฐานข้อมูลที่สามารถใช้สำหรับการนำเข้าหรือกู้คืนไปยังอินสแตนซ์ฐานข้อมูลที่กำลังทำงานอยู่ผ่านเซิร์ฟเวอร์ฐานข้อมูล ในกรณีส่วนใหญ่ ไฟล์ .dmp จะมีเวลาและวันที่ประทับเป็นชื่อไฟล์

### เนื้อหาของไฟล์ DMP

ไฟล์การถ่ายโอนข้อมูลหน่วยความจำประกอบด้วย:

* คำสั่งหยุดและพารามิเตอร์;
* รายการไดรเวอร์ที่โหลด
* บริบทของโปรเซสเซอร์ (PRCB) สำหรับกระบวนการที่หยุดการทำงานปกติของ Windows
* บริบทเคอร์เนลและข้อมูลตัวประมวลผล (EPROCESSES) สำหรับกระบวนการที่หยุดทำงาน
* บริบทเคอร์เนลและข้อมูลตัวประมวลผล (ETHREAD) สำหรับเธรดที่หยุดทำงาน
* สแตกการเรียกใช้โหมดเคอร์เนลสำหรับเธรดที่สิ้นสุดกระบวนการจากการดำเนินการ


## ตัวอย่าง DMP

ข้อผิดพลาด stop 0XC0000218 (Registry_File_Failure) สร้างไฟล์ DMP ดังนี้:

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

## อ้างอิง ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

