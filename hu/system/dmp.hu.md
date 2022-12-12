{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "kiterjesztés", "fájl", "formátum", "rendszer", "MemoryDump", "Minidump", "programok", "számítógép", "alkalmazás" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump fájlformátum",
  "description":"További információ a DMP fájlformátumról és az API-król, amelyek DMP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Mi az a DMP fájl? ##

A DMP fájl elsősorban a MemoryDump vagy Minidump fájlformátumhoz kapcsolódik. A Microsoft Windows operációs rendszerben a számítógép memóriájából kiírt adatok tárolására szolgál. A DMP-fájlok általában akkor jönnek létre, amikor egy fájl összeomlik vagy hiba történik. A DMP-fájlok időnként nagyon fontosak a műszaki szakértők vagy a haladó számítógép-felhasználók számára a felmerülő problémák elhárításához és bármilyen alkalmazási probléma megoldásához. A DMP-fájlokat a Microsoft védett formátumban tárolja, amelyet az operációs rendszer a rendszerre telepített alkalmazások hibakeresésére használ.


## A DMP fájlformátum műszaki specifikációi

Windows rendszerben a "savedump.exe" rendszereszköz .dmp fájlokat hoz létre, amelyeket azután különféle elérhető hibakereső segédprogramok dolgozhatnak fel. A mini kiíratást (64/128 Kb) a Windows a '%SystemRoot%\Minidump' könyvtárban tárolja. Másrészt a kernelmemória és a teljes memória kiíratása a rendszer gyökérjében Memory.dmp fájlokként tárolódik. A memóriakiíratási fájlok viszonylag nagy fájlok, ezért elegendő tárhelyet foglalhatnak el. Ezért tanácsos törölni azokat a haszontalan .dmp fájlokat, amelyekről úgy gondolja, hogy nem lesznek hasznosak a hibaelhárításhoz.

Törölheti a .dmp fájlokat manuálisan vagy a számítógépen található alapértelmezett „lemeztiszta varázsló” használatával. Az Oracle adatbázistermékek DMP-kiterjesztéseket használnak a .dmp fájlok használatára a létrehozott és használt biztonsági mentési és helyreállítási adatbázisfájlokban. Az Oracle által létrehozott DMP-fájlok adatbázis-biztonsági másolatok, amelyek egy futó adatbázis-példányba importálhatók vagy visszaállíthatók egy adatbázis-kiszolgálón keresztül. A legtöbb esetben a .dmp fájlok fájlneveként idő- és dátumbélyeg található.

### A DMP fájl tartalma

A memóriaképfájl a következőket tartalmazza:

* A stop utasítás és paraméterei;
* A betöltött illesztőprogramok listája;
* A processzor környezete (PRCB) a Windows normál működését leállító folyamatokhoz;
* A leállított folyamatok kernelkörnyezete és processzorinformációi (EPROCESSES);
* A leállt szál kernelkörnyezete és processzorinformációja (ETHREAD);
* A kernel módú hívási verem a folyamat végrehajtását lezáró szálhoz.


## DMP példa

A 0XC0000218 leállítási hiba (Registry_File_Failure) a következőképpen hoz létre egy DMP-fájlt:

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

## Hivatkozási szám

* [DMP – Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

