{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "розширення", "файл", "формат", "система", "MemoryDump", "Minidump", "програми", "комп'ютер", "програма"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - формат файлу MemoryDump",
  "description":"Дізнайтеся про формат файлу DMP та API, які можуть створювати та відкривати файли DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Що таке файл DMP? ##

Файл DMP насамперед асоціюється з форматом файлу MemoryDump або Minidump. Він використовується в операційній системі Microsoft Windows для зберігання даних, вивантажених із пам’яті комп’ютера. Зазвичай файли DMP створюються, коли файл аварійно завершує роботу або виникає помилка. Іноді файли DMP дуже важливі для технічних експертів або досвідчених користувачів комп’ютерів, щоб усунути проблеми, з якими ви стикаєтеся, і вирішити будь-яку проблему з програмою. Файли DMP зберігаються як власний формат у Microsoft, який використовується операційною системою для налагодження будь-якої програми, встановленої в системі.


## Технічна специфікація формату файлу DMP

У Windows системний інструмент "savedump.exe" створює файли .dmp, які потім можна обробляти різними доступними утилітами для налагодження. Міні-дамп (64/128 Кб) зберігається Windows у каталозі «%SystemRoot%\Minidump». З іншого боку, пам’ять ядра та повні дампи пам’яті зберігаються в корені системи як файли «Memory.dmp». Файли дампа пам’яті є відносно великими файлами, тому можуть займати достатній обсяг пам’яті. Тому радимо видалити непотрібні файли .dmp, які, на вашу думку, не будуть корисними для вирішення проблем.

Файли .dmp можна видалити вручну або за допомогою стандартного «майстра очищення диска» на комп’ютері. Розширення DMP використовуються продуктами баз даних Oracle для використання файлів .dmp у створених і використаних файлах баз даних резервного копіювання та відновлення. Файли DMP, створені Oracle, є резервними копіями бази даних, які можна використовувати для імпорту або відновлення в запущений екземпляр бази даних через сервер бази даних. У більшості випадків назви файлів .dmp мають позначки часу та дати.

### Вміст файлу DMP

Файл дампа пам'яті містить:

* Оператор зупинки та його параметри;
* Список завантажених драйверів;
* Контекст процесора (PRCB) для процесів, які зупинили нормальну роботу Windows;
* Контекст ядра та інформація про процесор (EPROCESSES) для процесів, які були зупинені;
* Контекст ядра та інформація про процесор (ETHREAD) для потоку, який зупинився;
* Стек викликів режиму ядра для потоку, який припинив виконання процесу.


## Приклад DMP

Stop-помилка 0XC0000218 (Registry_File_Failure) створює файл DMP таким чином:

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

## Посилання ##

* [DMP – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

