{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "разширение", "файл", "формат", "система", "MemoryDump", "Minidump", "програми", "компютър", "приложение"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump файлов формат",
  "description":"Научете за DMP файловия формат и API, които могат да създават и отварят DMP файлове.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Какво е DMP файл? ##

DMP файлът е свързан предимно с файловия формат MemoryDump или Minidump. Използва се в операционната система Microsoft Windows за съхраняване на данни, които са били изхвърлени от паметта на компютъра. Обикновено DMP файловете се създават, когато даден файл се срине или възникне грешка. Понякога DMP файловете са много важни за техническите експерти или напредналите компютърни потребители, за да отстранят проблемите, пред които сте изправени, и да разрешат всякакъв вид проблем с приложението. DMP файловете се съхраняват като патентован формат в Microsoft, който се използва от операционната система за отстраняване на грешки във всяко приложение, инсталирано в системата.


## Техническа спецификация на DMP файлов формат

В Windows системният инструмент "savedump.exe" генерира .dmp файлове, които след това могат да бъдат обработени от различни налични помощни програми за отстраняване на грешки. Мини дъмп (64/128 Kb) се съхранява от Windows в директорията „%SystemRoot%\Minidump“. От друга страна, паметта на ядрото и пълните дъмпове на паметта се съхраняват в корена на системата като файлове „Memory.dmp“. Файловете за дъмп на паметта са относително големи файлове, следователно могат да заемат достатъчно място за съхранение. Затова се препоръчва безполезните .dmp файлове, които смятате, че няма да бъдат полезни за отстраняване на проблеми, след това да ги изтриете.

Можете да изтриете .dmp файлове ръчно или като използвате "съветника за почистване на диска" по подразбиране на вашия компютър. DMP разширенията се използват от продуктите за бази данни на Oracle за използване на .dmp файловете в създадените и използвани файлове на базата данни за архивиране и възстановяване. DMP файловете, създадени от Oracle, са резервни копия на база данни, които могат да се използват за импортиране или възстановяване в работещ екземпляр на база данни чрез сървър на база данни. В повечето случаи .dmp файловете имат щампи за време и дата като имена на файлове.

### Съдържание на DMP файл

Файл с дъмп памет съдържа:

* Инструкцията за спиране и нейните параметри;
* Списък на заредените драйвери;
* Контекст на процесора (PRCB) за процесите, които са спрели нормалната работа на Windows;
* Контекста на ядрото и информацията за процесора (EPROCESSES) за процесите, които са били спрени;
* Контекстът на ядрото и информацията за процесора (ETHREAD) за нишката, която е спряла;
* Стекът за извикване в режим на ядрото за нишката, която е прекратила изпълнението на процеса.


## Пример за DMP

Стоп грешката 0XC0000218 (Registry_File_Failure) създава DMP файл, както следва:

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

## Референция ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

