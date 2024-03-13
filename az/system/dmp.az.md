{
  "date": "2021-07-07",
  "keywords": [
"DMP",
"uzadılması",
"fayl",
"format",
"sistemi",
"MemoryDump",
"Minidump",
"proqramlar",
"kompüter",
"tətbiq"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DMP - MemoryDump fayl formatı",
  "description": "DMP faylları yarada və aça bilən DMP fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dm-azp"
}
},
  "lastmod": "2021-07-07"
}

## DMP faylı nədir? ##

DMP faylı ilk növbədə MemoryDump və ya Minidump fayl formatı ilə əlaqələndirilir. O, Microsoft Windows əməliyyat sistemində kompüterin yaddaş yerindən atılmış məlumatları saxlamaq üçün istifadə olunur. Adətən, DMP faylları fayl çökdükdə və ya xəta baş verdikdə yaradılır. Bəzən DMP faylları texniki ekspertlər və ya qabaqcıl kompüter istifadəçiləri üçün qarşılaşdığınız problemləri həll etmək və hər cür proqram problemini həll etmək üçün çox vacibdir. DMP faylları Microsoft-da mülkiyyət formatı kimi saxlanılır və bu, əməliyyat sistemi tərəfindən sistemdə quraşdırılmış hər hansı proqramın sazlanması üçün istifadə olunur.


## DMP Fayl Formatının Texniki Spesifikasiyası

Windows-da savedump.exe sistem aləti .dmp faylları yaradır və sonradan mövcud olan müxtəlif sazlama yardım proqramları tərəfindən emal oluna bilər. Mini dump (64/128 Kb) pəncərələr tərəfindən '%SystemRoot%\Minidump' kataloqunda saxlanılır. Digər tərəfdən, nüvə yaddaşı və tam yaddaş boşluqları sistem kökündə 'Memory.dmp' faylları kimi saxlanılır. Yaddaş boşaltma faylları nisbətən böyük fayllardır, buna görə də kifayət qədər yaddaş yeri tuta bilər. Odur ki, problemlərin aradan qaldırılması üçün faydalı olmadığını düşündüyünüz faydasız .dmp fayllarını silmək tövsiyə olunur.

Siz .dmp fayllarını əl ilə və ya kompüterinizdə standart təmiz disk sehrbazından istifadə edərək silə bilərsiniz. DMP genişləndirmələri Oracle verilənlər bazası məhsulları tərəfindən yaradılmış və istifadə olunan ehtiyat və bərpa verilənlər bazası fayllarında .dmp fayllarından istifadə etmək üçün istifadə olunur. Oracle tərəfindən yaradılmış DMP faylları verilənlər bazası serveri vasitəsilə işləyən verilənlər bazası nümunəsinə idxal etmək və ya bərpa etmək üçün istifadə edilə bilən verilənlər bazası ehtiyat nüsxələridir. Əksər hallarda, .dmp faylları fayl adları kimi vaxt və tarix möhürlərinə malikdir.

### DMP faylının məzmunu

Yaddaş boşaltma faylına aşağıdakılar daxildir:

* Stop bəyanatı və onun parametrləri;

* Yüklənmiş sürücülərin siyahısı;

* Windows-un normal işini dayandıran proseslər üçün prosessorun konteksti (PRCB);

* Dayandırılmış proseslər üçün nüvə konteksti və prosessor məlumatı (EPROCESSES);

* Dayanan mövzu üçün nüvə konteksti və prosessor məlumatı (ETHREAD);

* Prosesi yerinə yetirməkdən qurtaran iplik üçün kernel rejimi çağırış yığını.



## DMP nümunəsi

Dayanma xətası 0XC0000218 (Registry_File_Failure) aşağıdakı kimi bir DMP faylı yaradır:

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

## İstinad ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


