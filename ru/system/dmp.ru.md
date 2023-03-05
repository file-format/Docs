{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "расширение", "файл", "формат", "система", "Дамп памяти", "Минидамп", "программы", "компьютер", "приложение" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP — формат файла дампа памяти",
  "description":"Узнайте о формате файла DMP и API-интерфейсах, которые могут создавать и открывать файлы DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## .DMP вариант № ##

Файл DMP в основном связан с форматом файла MemoryDump или Minidump. Он используется в операционной системе Microsoft Windows для хранения данных, выгруженных из памяти компьютера. Обычно файлы DMP создаются при сбое файла или возникновении ошибки. Иногда файлы DMP очень важны для технических экспертов или опытных пользователей компьютеров для устранения проблем, с которыми вы сталкиваетесь, и решения любых проблем приложений. Файлы DMP хранятся в Microsoft в собственном формате, который используется операционной системой для отладки любого приложения, установленного в системе.


## Техническая спецификация формата файла DMP

В Windows системный инструмент savedump.exe создает файлы .dmp, которые затем могут быть обработаны различными доступными утилитами отладки. Мини-дамп (64/128 Кб) хранится Windows в каталоге '%SystemRoot%\Minidump'. С другой стороны, память ядра и полные дампы памяти хранятся в корне системы в виде файлов «Memory.dmp». Файлы дампа памяти являются относительно большими файлами, поэтому могут занимать достаточно места для хранения. Поэтому рекомендуется удалить бесполезные файлы .dmp, которые, по вашему мнению, не будут полезны для устранения неполадок.

Вы можете удалить файлы .dmp либо вручную, либо с помощью стандартного «мастера очистки диска» на вашем компьютере. Расширения DMP используются продуктами баз данных Oracle для использования файлов .dmp в создаваемых и используемых файлах базы данных резервного копирования и восстановления. Файлы DMP, созданные Oracle, представляют собой резервные копии базы данных, которые можно использовать для импорта или восстановления в работающий экземпляр базы данных через сервер базы данных. В большинстве случаев файлы .dmp имеют метки времени и даты в качестве имен файлов.

### Содержимое файла DMP

Файл дампа памяти содержит:

* Оператор остановки и его параметры;
* Список загружаемых драйверов;
* Контекст процессора (PRCB) для процессов, прервавших нормальную работу Windows;
* Контекст ядра и информация о процессоре (EPROCESSES) для остановленных процессов;
* Контекст ядра и информация о процессоре (ETHREAD) для остановленного потока;
* Стек вызовов режима ядра для потока, завершившего выполнение процесса.


## Пример платформы управления данными

Стоп-ошибка 0XC0000218 (Registry_File_Failure) создает файл DMP следующим образом:

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

## Ссылка ##

* [DMP — Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

