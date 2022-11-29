{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "tillägg", "fil", "format", "system", "MemoryDump", "Minidump", "program", "dator", "applikation" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump filformat",
  "description":"Läs mer om DMP-filformat och API:er som kan skapa och öppna DMP-filer.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Vad är en DMP fil? ##

DMP-filen är i första hand associerad med filformatet MemoryDump eller Minidump. Det används i Microsoft Windows operativsystem för att lagra data som har dumpats från datorns minnesutrymme. Vanligtvis skapas DMP-filer när en fil kraschar eller ett fel uppstår. Ibland är DMP-filer mycket viktiga för tekniska experter eller avancerade datoranvändare för att felsöka problemen du står inför och lösa alla typer av applikationsproblem. DMP-filerna lagras som ett proprietärt format i Microsoft som används av operativsystemet för att felsöka alla program som är installerade på systemet.


## Teknisk specifikation för DMP-filformat

I Windows genererar systemverktyget "savedump.exe" .dmp-filer som sedan kan bearbetas av olika tillgängliga felsökningsverktyg. Minidump (64/128 Kb) lagras av Windows i katalogen '%SystemRoot%\Minidump'. Å andra sidan lagras kärnminnet och fullständiga minnesdumpar i systemroten som 'Memory.dmp'-filer. Minnesdumpfiler är relativt stora filer och kan därför ta tillräckligt med lagringsutrymme. Så det rekommenderas att de onödiga .dmp-filerna som du tror inte kommer att vara användbara för felsökning av problem sedan raderar dem.

Du kan ta bort .dmp-filer antingen manuellt eller genom att använda standardguiden för "rengör disk" på din dator. DMP-tillägg används av Oracles databasprodukter för att använda .dmp-filerna i backup- och återställningsdatabasfiler som skapats och används. DMP-filerna som skapats av Oracle är säkerhetskopior av databas som kan användas för att importera eller återställa till en pågående databasinstans via en databasserver. I de flesta fall har .dmp-filer tids- och datumstämplar som filnamn.

### Innehållet i DMP-filen

En minnesdumpfil innehåller:

* Stop-satsen och dess parametrar;
* En lista över laddade drivrutiner;
* Processorns sammanhang (PRCB) för de processer som stoppade den normala driften av Windows;
* Kärnkontexten och processorinformationen (EPROCESSES) för de processer som har stoppats;
* Kärnkontext och processorinformation (ETHREAD) för tråden som stannade;
* Anropsstacken i kärnläge för tråden som avslutade processen från att utföras.


## DMP Exempel

Stoppfelet 0XC0000218 (Registry_File_Failure) skapar en DMP-fil enligt följande:

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
Unknown bugcheck description,
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

## Referens ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

