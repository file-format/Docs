{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "extensie", "bestand", "format", "systeem", "MemoryDump", "Minidump", "programma's", "computer", "toepassing" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump-bestandsindeling",
  "description":"Meer informatie over DMP-bestandsindeling en API's die DMP-bestanden kunnen maken en openen.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Wat is een DMP-bestand? ##

Het DMP-bestand wordt voornamelijk geassocieerd met het MemoryDump- of Minidump-bestandsformaat. Het wordt gebruikt in het Microsoft Windows-besturingssysteem om gegevens op te slaan die uit de geheugenruimte van de computer zijn gedumpt. Gewoonlijk worden DMP-bestanden gemaakt wanneer een bestand crasht of er een fout optreedt. Soms zijn DMP-bestanden erg belangrijk voor technische experts of geavanceerde computergebruikers om de problemen op te lossen waarmee u wordt geconfronteerd en om elk soort toepassingsprobleem op te lossen. De DMP-bestanden worden opgeslagen als een eigen indeling in Microsoft die door het besturingssysteem wordt gebruikt om fouten op te sporen in elke applicatie die op het systeem is geïnstalleerd.


## Technische specificatie van DMP-bestandsindeling

In Windows genereert de systeemtool "savedump.exe" .dmp-bestanden die vervolgens kunnen worden verwerkt door verschillende beschikbare foutopsporingsprogramma's. Minidump (64/128 Kb) wordt door Windows opgeslagen in de map '%SystemRoot%\Minidump'. Aan de andere kant worden het kernelgeheugen en de volledige geheugendumps in de systeemhoofdmap opgeslagen als 'Memory.dmp'-bestanden. Geheugendumpbestanden zijn relatief grote bestanden en kunnen daarom voldoende opslagruimte in beslag nemen. Het is dus aan te raden om de nutteloze .dmp-bestanden waarvan u denkt dat ze niet nuttig zijn voor het oplossen van problemen, ze vervolgens te verwijderen.

U kunt .dmp-bestanden handmatig of met behulp van de standaard "clean disk wizard" op uw computer verwijderen. DMP-extensies worden door de Oracle-databaseproducten gebruikt om de .dmp-bestanden te gebruiken in back-up- en hersteldatabasebestanden die zijn gemaakt en gebruikt. De DMP-bestanden die door Oracle zijn gemaakt, zijn databaseback-ups die kunnen worden gebruikt voor het importeren of herstellen in een actieve database-instantie via een databaseserver. In de meeste gevallen hebben .dmp-bestanden tijd- en datumstempels als bestandsnaam.

### Inhoud van DMP-bestand

Een geheugendumpbestand bevat:

* De stop-instructie en zijn parameters;
* Een lijst met geladen stuurprogramma's;
* De processorcontext (PRCB) voor de processen die de normale werking van Windows hebben stopgezet;
* De kernelcontext en processorinformatie (EPROCESSES) voor de gestopte processen;
* De kernelcontext en processorinformatie (ETHREAD) voor de thread die is gestopt;
* De kernelmodus-aanroepstack voor de thread die het uitvoeren van het proces beëindigde.


## DMP-voorbeeld

De stopfout 0XC0000218 (Registry_File_Failure) maakt als volgt een DMP-bestand aan:

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

## Referentie ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

