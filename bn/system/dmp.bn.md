{
  "date" : "2021-07-07",
  "keywords" : [ "DMP", "extension", "file", "format", "system", "MemoryDump", "Minidump", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" : "DMP - MemoryDump ফাইল ফরম্যাট",
  "description":"DMP ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি DMP ফাইল তৈরি এবং খুলতে পারে।",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## একটি DMP ফাইল কি? ##

DMP ফাইলটি প্রাথমিকভাবে MemoryDump বা Minidump ফাইল ফরম্যাটের সাথে যুক্ত। এটি মাইক্রোসফ্ট উইন্ডোজ অপারেটিং সিস্টেমে কম্পিউটারের মেমরি স্পেস থেকে ডাম্প করা ডেটা সংরক্ষণ করতে ব্যবহৃত হয়। সাধারণত, একটি ফাইল ক্র্যাশ বা একটি ত্রুটি ঘটলে DMP ফাইল তৈরি করা হয়। কখনও কখনও ডিএমপি ফাইলগুলি প্রযুক্তিগত বিশেষজ্ঞ বা উন্নত কম্পিউটার ব্যবহারকারীদের জন্য আপনার সম্মুখীন হওয়া সমস্যার সমাধান করতে এবং যেকোন ধরণের অ্যাপ্লিকেশন সমস্যা সমাধানের জন্য অত্যন্ত গুরুত্বপূর্ণ। ডিএমপি ফাইলগুলি মাইক্রোসফ্টের মালিকানাধীন ফর্ম্যাট হিসাবে সংরক্ষণ করা হয় যা অপারেটিং সিস্টেম দ্বারা সিস্টেমে ইনস্টল করা যেকোনো অ্যাপ্লিকেশন ডিবাগ করতে ব্যবহৃত হয়।


## ডিএমপি ফাইল ফরম্যাটের প্রযুক্তিগত স্পেসিফিকেশন

উইন্ডোজে, savedump.exe সিস্টেম টুলটি .dmp ফাইল তৈরি করে যা পরে উপলব্ধ বিভিন্ন ডিবাগিং ইউটিলিটি দ্বারা প্রক্রিয়া করা যেতে পারে। মিনি ডাম্প (64/128 Kb) '%SystemRoot%\Minidump' ডিরেক্টরিতে উইন্ডোজ দ্বারা সংরক্ষণ করা হয়। অন্যদিকে, কার্নেল মেমরি এবং সম্পূর্ণ মেমরি ডাম্পগুলি 'Memory.dmp' ফাইল হিসাবে সিস্টেম রুটে সংরক্ষণ করা হয়। মেমরি ডাম্প ফাইলগুলি তুলনামূলকভাবে বড় ফাইল, তাই পর্যাপ্ত পরিমাণে স্টোরেজ স্পেস নিতে পারে। তাই পরামর্শ দেওয়া হচ্ছে যে অকেজো .dmp ফাইলগুলি যেগুলি আপনার মনে হয় সমস্যা সমাধানের জন্য উপযোগী হবে না তাহলে সেগুলি মুছে ফেলুন৷

আপনি .dmp ফাইলগুলি ম্যানুয়ালি বা আপনার কম্পিউটারে ডিফল্ট ক্লিন ডিস্ক উইজার্ড ব্যবহার করে মুছে ফেলতে পারেন। ডিএমপি এক্সটেনশনগুলি ওরাকল ডাটাবেস পণ্যগুলি দ্বারা তৈরি এবং ব্যবহৃত ব্যাকআপ এবং পুনরুদ্ধার ডেটাবেস ফাইলগুলিতে .dmp ফাইলগুলি ব্যবহার করতে ব্যবহৃত হয়। ওরাকল দ্বারা তৈরি ডিএমপি ফাইলগুলি ডাটাবেস ব্যাকআপ যা একটি ডাটাবেস সার্ভারের মাধ্যমে চলমান ডাটাবেস ইনস্ট্যান্সে আমদানি বা পুনরুদ্ধার করার জন্য ব্যবহার করা যেতে পারে। বেশিরভাগ ক্ষেত্রে, .dmp ফাইলের ফাইলের নাম হিসাবে সময় এবং তারিখ স্ট্যাম্প থাকে।

### ডিএমপি ফাইলের বিষয়বস্তু

একটি মেমরি ডাম্প ফাইল রয়েছে:

* স্টপ স্টেটমেন্ট এবং এর পরামিতি;

* লোড করা ড্রাইভারের তালিকা;

* প্রসেসরের প্রেক্ষাপট (PRCB) প্রসেসের জন্য যা উইন্ডোজের স্বাভাবিক ক্রিয়াকলাপ বন্ধ করে দেয়;

* যে প্রক্রিয়াগুলি বন্ধ করা হয়েছে তার জন্য কার্নেল প্রসঙ্গ এবং প্রসেসরের তথ্য (EPROCESSES);

* থামানো থ্রেডের জন্য কার্নেল প্রসঙ্গ এবং প্রসেসর তথ্য (ETHREAD);

* থ্রেডের জন্য কার্নেল-মোড কল স্ট্যাক যা কার্য সম্পাদন থেকে প্রক্রিয়াটি শেষ করেছে।



## ডিএমপি উদাহরণ

স্টপ ত্রুটি 0XC0000218 (Registry_File_Failure) অনুসরণ করে একটি DMP ফাইল তৈরি করে:

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

## রেফারেন্স ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


