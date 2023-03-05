{
  "date" : "2021-07-07",
  "keywords" :["DMP", "extension", "file", "format", "system", "MemoryDump", "Minidump", "Programs", "computer", "application"],
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - تنسيق ملف MemoryDump" ,
  "description":"تعرف على تنسيق ملف DMP وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DMP وفتحها." ,
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
} ,
  "lastmod" : "2021-07-07"
}

## ما هو ملف DMP؟ ##

يرتبط ملف DMP بشكل أساسي بتنسيق ملف MemoryDump أو Minidump. يتم استخدامه في نظام التشغيل Microsoft Windows لتخزين البيانات التي تم تفريغها من مساحة ذاكرة الكمبيوتر. عادة ، يتم إنشاء ملفات DMP عند تعطل أحد الملفات أو حدوث خطأ. في بعض الأحيان ، تكون ملفات DMP مهمة جدًا للخبراء التقنيين أو مستخدمي الكمبيوتر المتقدمين لاستكشاف المشكلات التي تواجهها وحل أي نوع من مشكلات التطبيق. يتم تخزين ملفات DMP كتنسيق خاص في Microsoft يستخدمه نظام التشغيل لتصحيح أي تطبيق مثبت على النظام.


## المواصفات الفنية لتنسيق ملف DMP

في نظام التشغيل Windows ، تقوم أداة النظام "saveump.exe" بإنشاء ملفات .dmp والتي يمكن معالجتها بعد ذلك بواسطة أدوات تصحيح أخطاء متنوعة متاحة. يتم تخزين التفريغ الصغير (64/128 كيلو بايت) بواسطة النوافذ في دليل٪ SystemRoot٪ \ Minidump. من ناحية أخرى ، يتم تخزين ذاكرة kernel وتفريغ الذاكرة الكاملة في جذر النظام كملفات 'Memory.dmp'. ملفات تفريغ الذاكرة هي ملفات كبيرة نسبيًا ، وبالتالي يمكن أن تأخذ مساحة تخزين كافية. لذلك يُنصح بأن ملفات .dmp عديمة الفائدة التي تعتقد أنها لن تكون مفيدة لاستكشاف الأخطاء وإصلاحها ثم احذفها.

يمكنك حذف ملفات .dmp إما يدويًا أو باستخدام "معالج القرص النظيف" الافتراضي على جهاز الكمبيوتر الخاص بك. يتم استخدام امتدادات DMP بواسطة منتجات قاعدة بيانات Oracle لاستخدام ملفات .dmp في ملفات قاعدة بيانات النسخ الاحتياطي والاسترداد التي تم إنشاؤها واستخدامها. ملفات DMP التي تم إنشاؤها بواسطة Oracle هي نسخ احتياطية لقاعدة البيانات يمكن استخدامها للاستيراد أو الاستعادة إلى طبعة قاعدة بيانات قيد التشغيل من خلال خادم قاعدة بيانات. في معظم الحالات ، تحتوي ملفات .dmp على طوابع الوقت والتاريخ كأسماء ملفاتهم.

### محتويات ملف DMP

يحتوي ملف تفريغ الذاكرة على:

* بيان الإيقاف ومعلماته ؛
* قائمة السائقين المحملة.
* سياق المعالج (PRCB) للعمليات التي أوقفت التشغيل العادي لنظام التشغيل Windows ؛
* سياق kernel ومعلومات المعالج (EPROCESSES) للعمليات التي تم إيقافها ؛
* سياق kernel ومعلومات المعالج (ETHREAD) لمؤشر الترابط الذي توقف ؛
* مكدس استدعاء وضع kernel لمؤشر الترابط الذي أنهى العملية من الأداء.


## مثال DMP

ينشئ خطأ الإيقاف 0XC0000218 (Registry_File_Failure) ملف DMP على النحو التالي:

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

## المرجعي ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

