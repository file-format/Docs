{
  "date": "2021-07-07",
  "keywords": [
"DMP",
"افزونه",
"فایل",
"قالب",
"سیستم",
"MemoryDump",
"مینی دامپ",
"برنامه ها",
"کامپیوتر",
"کاربرد"
]،
  "author": {
    "display_name": "Sami Cheema"
}،
  "draft": "false",
  "toc": true,
  "title": "DMP - فرمت فایل MemoryDump",
  "description": "درباره فرمت فایل DMP و APIهایی که می‌توانند فایل‌های DMP را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "DMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dm-fap"
}
}،
  "lastmod": "2021-07-07"
}

## فایل DMP چیست؟ ##

فایل DMP در درجه اول با فرمت فایل MemoryDump یا Minidump مرتبط است. در سیستم عامل مایکروسافت ویندوز برای ذخیره داده هایی که از فضای حافظه کامپیوتر تخلیه شده اند استفاده می شود. معمولاً فایل‌های DMP زمانی ایجاد می‌شوند که یک فایل از کار بیفتد یا خطایی رخ دهد. گاهی اوقات فایل های DMP برای کارشناسان فنی یا کاربران پیشرفته رایانه برای عیب یابی مشکلاتی که با آن مواجه هستید و حل هر نوع مشکل برنامه بسیار مهم است. فایل های DMP به عنوان یک فرمت اختصاصی در مایکروسافت ذخیره می شوند که توسط سیستم عامل برای رفع اشکال هر برنامه نصب شده روی سیستم استفاده می شود.


## مشخصات فنی فرمت فایل DMP

در ویندوز، ابزار سیستم «savedump.exe» فایل‌های .dmp را تولید می‌کند که سپس می‌تواند توسط ابزارهای مختلف اشکال زدایی موجود پردازش شود. Mini dump (64/128 Kb) توسط ویندوز در دایرکتوری '%SystemRoot%\Minidump' ذخیره می شود. از سوی دیگر، حافظه هسته و تخلیه کامل حافظه در ریشه سیستم به عنوان فایل Memory.dmp ذخیره می شوند. فایل‌های تخلیه حافظه فایل‌های نسبتاً بزرگی هستند، بنابراین می‌توانند فضای ذخیره‌سازی کافی را اشغال کنند. بنابراین توصیه می‌شود فایل‌های .dmp بی‌فایده را که فکر می‌کنید برای عیب‌یابی مشکلات مفید نیستند، حذف کنید.

شما می توانید فایل های .dmp را به صورت دستی یا با استفاده از جادوگر دیسک پاک پیش فرض در رایانه خود حذف کنید. پسوندهای DMP توسط محصولات پایگاه داده Oracle برای استفاده از فایل‌های .dmp در فایل‌های پایگاه داده پشتیبان و بازیابی ایجاد و استفاده می‌شوند. فایل‌های DMP ایجاد شده توسط Oracle پشتیبان‌گیری از پایگاه داده هستند که می‌توانند برای وارد کردن یا بازیابی به یک نمونه پایگاه داده در حال اجرا از طریق یک سرور پایگاه داده استفاده شوند. در بیشتر موارد، فایل های .dmp دارای مهر زمان و تاریخ به عنوان نام فایل خود هستند.

### محتویات فایل DMP

یک فایل تخلیه حافظه شامل:

* دستور توقف و پارامترهای آن.

* لیستی از درایورهای بارگذاری شده؛

* زمینه پردازنده (PRCB) برای فرآیندهایی که عملکرد عادی ویندوز را متوقف می کند.

* زمینه هسته و اطلاعات پردازنده (EPROCESSES) برای فرآیندهایی که متوقف شده اند.

* زمینه هسته و اطلاعات پردازنده (ETHREAD) برای رشته ای که متوقف شده است.

* پشته فراخوانی حالت هسته برای رشته ای که به اجرای فرآیند پایان داد.



## مثال DMP

خطای توقف 0XC0000218 (Registry_File_Failure) یک فایل DMP را به صورت زیر ایجاد می کند:

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

## ارجاع ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


