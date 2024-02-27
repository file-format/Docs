{
  "date": "2021-07-07",
  "keywords": [
"DMP",
"udvidelse",
"fil",
"format",
"system",
"MemoryDump",
"Minidump",
"programmer",
"computer",
"Ansøgning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DMP - MemoryDump filformat",
  "description": "Lær om DMP-filformat og API'er, der kan oprette og åbne DMP-filer.",
  "linktitle": "DMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dm-dap"
}
},
  "lastmod": "2021-07-07"
}

## Hvad er en DMP fil? ##

DMP-filen er primært forbundet med MemoryDump- eller Minidump-filformatet. Det bruges i Microsoft Windows-operativsystemet til at gemme data, der er blevet dumpet fra computerens hukommelsesplads. Normalt oprettes DMP-filer, når en fil går ned, eller der opstår en fejl. Til tider er DMP-filer meget vigtige for tekniske eksperter eller avancerede computerbrugere til at fejlfinde de problemer, du står over for, og løse enhver form for applikationsproblem. DMP-filerne gemmes som et proprietært format i Microsoft, som bruges af operativsystemet til at fejlsøge enhver applikation, der er installeret på systemet.


## Teknisk specifikation af DMP-filformat

I Windows genererer systemværktøjet savedump.exe .dmp-filer, som derefter kan behandles af forskellige tilgængelige fejlfindingsværktøjer. Minidump (64/128 Kb) er gemt af windows i mappen '%SystemRoot%\Minidump'. På den anden side er kernehukommelsen og fuld hukommelsesdumps gemt i systemroden som 'Memory.dmp'-filer. Hukommelsesdumpfiler er relativt store filer, og kan derfor tage en tilstrækkelig mængde lagerplads. Så det anbefales, at de ubrugelige .dmp-filer, som du tror ikke vil være nyttige til fejlfinding af problemer, så sletter dem.

Du kan slette .dmp-filer enten manuelt eller ved at bruge standard ren disk wizard på din computer. DMP-udvidelser bruges af Oracle-databaseprodukterne til at bruge .dmp-filerne i backup- og gendannelsesdatabasefiler, der er oprettet og brugt. DMP-filerne oprettet af Oracle er databasesikkerhedskopier, der kan bruges til at importere eller gendanne til en kørende databaseinstans gennem en databaseserver. I de fleste tilfælde har .dmp-filer tids- og datostempler som deres filnavne.

### Indhold af DMP-fil

En hukommelsesdumpfil indeholder:

* Stop-sætningen og dens parametre;

* En liste over indlæste drivere;

* Processorens kontekst (PRCB) for de processer, der stoppede den normale drift af Windows;

* Kernekonteksten og processorinformationen (EPROCESSES) for de processer, der er blevet stoppet;

* Kernekonteksten og processorinformationen (ETHREAD) for den tråd, der stoppede;

* Kernel-mode opkaldsstakken for den tråd, der afsluttede processen med at udføre.



## DMP eksempel

Stopfejlen 0XC0000218 (Registry_File_Failure) opretter en DMP-fil som følger:

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

## Reference ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


