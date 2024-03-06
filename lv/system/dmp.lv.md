{
  "date": "2021-07-07",
  "keywords": [
"DMP",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"Memory Dump",
"Minidump",
"programmas",
"dators",
"pieteikumu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DMP — MemoryDump faila formāts",
  "description": "Uzziniet par DMP failu formātu un API, kas var izveidot un atvērt DMP failus.",
  "linktitle": "DMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dm-lvp"
}
},
  "lastmod": "2021-07-07"
}

## Kas ir DMP fails? ##

DMP fails galvenokārt ir saistīts ar MemoryDump vai Minidump faila formātu. To izmanto operētājsistēmā Microsoft Windows, lai saglabātu datus, kas ir izmesti no datora atmiņas vietas. Parasti DMP faili tiek izveidoti, kad fails avarē vai rodas kļūda. Reizēm DMP faili ir ļoti svarīgi tehniskajiem ekspertiem vai pieredzējušiem datoru lietotājiem, lai novērstu problēmas, ar kurām saskaraties, un atrisinātu jebkāda veida lietojumprogrammu problēmas. DMP faili tiek glabāti kā patentēts formāts Microsoft, ko operētājsistēma izmanto, lai atkļūdotu jebkuru sistēmā instalēto lietojumprogrammu.


## DMP faila formāta tehniskā specifikācija

Operētājsistēmā Windows sistēmas rīks savedump.exe ģenerē .dmp failus, kurus pēc tam var apstrādāt ar dažādām pieejamajām atkļūdošanas utilītprogrammām. Mini izdruku (64/128 Kb) logi saglabā direktorijā '%SystemRoot%\Minidump'. No otras puses, kodola atmiņa un pilnas atmiņas izgāztuves tiek glabātas sistēmas saknē kā Memory.dmp faili. Atmiņas dump faili ir salīdzinoši lieli faili, tāpēc tie var aizņemt pietiekami daudz vietas. Tāpēc ir ieteicams dzēst bezjēdzīgos .dmp failus, kas, jūsuprāt, nebūs noderīgi problēmu novēršanai.

Varat dzēst .dmp failus vai nu manuāli, vai izmantojot datora noklusējuma tīra diska vedni. Oracle datu bāzes produkti izmanto DMP paplašinājumus, lai izmantotu .dmp failus izveidotajos un izmantotajos dublēšanas un atkopšanas datu bāzes failos. Oracle izveidotie DMP faili ir datu bāzes dublējumkopijas, kuras var izmantot, lai importētu vai atjaunotu darbojošās datu bāzes instancē, izmantojot datu bāzes serveri. Vairumā gadījumu .dmp failiem ir laika un datuma spiedogi kā failu nosaukumi.

### DMP faila saturs

Atmiņas izdrukas failā ir:

* Stop paziņojums un tā parametri;

* Ielādēto draiveru saraksts;

* Procesora konteksts (PRCB) procesiem, kas apturēja normālu Windows darbību;

* Kodola konteksts un procesora informācija (EPROCESSES) procesiem, kas ir apturēti;

* Kodola konteksts un procesora informācija (ETHREAD) pavedienam, kas tika apturēts;

* Kodola režīma izsaukuma steks pavedienam, kas pārtrauca procesa darbību.



## DMP piemērs

Apturēšanas kļūda 0XC0000218 (Registry_File_Failure) izveido DMP failu šādi:

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

## Atsauce Nr.

* [DMP — Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


