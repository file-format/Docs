{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "rozšíření", "soubor", "formát", "systém", "MemoryDump", "Minidump", "programy", "počítač", "aplikace" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump File Format",
  "description":"Další informace o formátu souborů DMP a rozhraních API, která mohou vytvářet a otevírat soubory DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Co je soubor DMP? ##

Soubor DMP je primárně spojen s formátem souboru MemoryDump nebo Minidump. Používá se v operačním systému Microsoft Windows k ukládání dat, která byla uvolněna z paměťového prostoru počítače. Soubory DMP se obvykle vytvářejí, když dojde k selhání souboru nebo k chybě. Někdy jsou soubory DMP velmi důležité pro technické odborníky nebo pokročilé uživatele počítačů při odstraňování problémů, kterým čelíte, a řešení jakéhokoli problému s aplikací. Soubory DMP jsou uloženy jako proprietární formát v Microsoftu, který používá operační systém k ladění jakékoli aplikace nainstalované v systému.


## Technická specifikace formátu souboru DMP

Ve Windows generuje systémový nástroj "savedump.exe" soubory .dmp, které mohou být následně zpracovány různými dostupnými ladicími nástroji. Mini výpis (64/128 Kb) je systémem Windows uložen v adresáři '%SystemRoot%\Minidump'. Na druhou stranu paměť jádra a úplné výpisy paměti jsou uloženy v kořenovém adresáři systému jako soubory 'Memory.dmp'. Soubory výpisu paměti jsou relativně velké soubory, a proto mohou zabírat dostatečné množství úložného prostoru. Doporučujeme tedy neužitečné soubory .dmp, o kterých si myslíte, že nebudou užitečné pro řešení problémů, a poté je odstranit.

Soubory .dmp můžete odstranit buď ručně, nebo pomocí výchozího „průvodce vyčištěním disku“ ve vašem počítači. Rozšíření DMP používají databázové produkty Oracle k použití souborů .dmp ve vytvořených a používaných databázových souborech pro zálohování a obnovu. Soubory DMP vytvořené společností Oracle jsou zálohy databáze, které lze použít pro import nebo obnovu do běžící instance databáze prostřednictvím databázového serveru. Ve většině případů mají soubory .dmp jako názvy souborů čas a datum.

### Obsah souboru DMP

Soubor výpisu paměti obsahuje:

* Příkaz stop a jeho parametry;
* Seznam načtených ovladačů;
* Kontext procesoru (PRCB) pro procesy, které zastavily normální provoz Windows;
* Kontext jádra a informace o procesoru (EPROCESSES) pro procesy, které byly zastaveny;
* Kontext jádra a informace o procesoru (ETHREAD) pro vlákno, které se zastavilo;
* Zásobník volání režimu jádra pro vlákno, které ukončilo provádění procesu.


## Příklad DMP

Chyba zastavení 0XC0000218 (Registry_File_Failure) vytvoří soubor DMP následovně:

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

## reference ##

* [DMP – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

