{
  "date" : "2021-07-07",
  "keywords" :["DMP", "rozszerzenie", "plik", "format", "system", "MemoryDump", "Minidump", "programy", "komputer", "aplikacja"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - format pliku zrzutu pamięci",
  "description":"Poznaj format plików DMP i interfejsy API, które mogą tworzyć i otwierać pliki DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Czym jest plik DMP? ##

Plik DMP jest przede wszystkim powiązany z formatem pliku MemoryDump lub Minidump. Jest używany w systemie operacyjnym Microsoft Windows do przechowywania danych, które zostały zrzucone z pamięci komputera. Zwykle pliki DMP są tworzone, gdy plik ulega awarii lub występuje błąd. Czasami pliki DMP są bardzo ważne dla ekspertów technicznych lub zaawansowanych użytkowników komputerów, aby rozwiązać problemy, z którymi się borykasz, i rozwiązać wszelkiego rodzaju problemy z aplikacjami. Pliki DMP są przechowywane jako zastrzeżony format w firmie Microsoft, który jest używany przez system operacyjny do debugowania dowolnej aplikacji zainstalowanej w systemie.


## Specyfikacja techniczna formatu pliku DMP

W systemie Windows narzędzie systemowe „savedump.exe” generuje pliki .dmp, które można następnie przetwarzać za pomocą różnych dostępnych narzędzi do debugowania. Mini zrzut (64/128 Kb) jest przechowywany przez system Windows w katalogu „%SystemRoot%\Minidump”. Z drugiej strony pamięć jądra i pełne zrzuty pamięci są przechowywane w katalogu głównym systemu jako pliki „Memory.dmp”. Pliki zrzutu pamięci są stosunkowo dużymi plikami, dlatego mogą zająć wystarczającą ilość miejsca. Dlatego zaleca się usunięcie bezużytecznych plików .dmp, które Twoim zdaniem nie będą przydatne do rozwiązywania problemów.

Pliki .dmp można usuwać ręcznie lub za pomocą domyślnego „kreatora czyszczenia dysku” na komputerze. Rozszerzenia DMP są używane przez produkty bazodanowe Oracle do używania plików .dmp w tworzonych i używanych plikach bazy danych kopii zapasowych i odzyskiwania. Pliki DMP utworzone przez Oracle to kopie zapasowe bazy danych, których można użyć do importowania lub przywracania do działającej instancji bazy danych za pośrednictwem serwera bazy danych. W większości przypadków nazwy plików .dmp zawierają znaczniki czasu i daty.

### Zawartość pliku DMP

Plik zrzutu pamięci zawiera:

* Instrukcja stop i jej parametry;
* Lista załadowanych sterowników;
* Kontekst procesora (PRCB) dla procesów, które zatrzymały normalne działanie systemu Windows;
* Kontekst jądra i informacje o procesorze (EPROCESSES) dla zatrzymanych procesów;
* Kontekst jądra i informacje o procesorze (ETHREAD) dla zatrzymanego wątku;
* Stos wywołań trybu jądra dla wątku, który zakończył wykonywanie procesu.


## Przykład DMP

Błąd zatrzymania 0XC0000218 (Registry_File_Failure) tworzy plik DMP w następujący sposób:

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

## Odniesienie ##

* [DMP — Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

