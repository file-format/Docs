{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "Erweiterung", "Datei", "Format", "System", "MemoryDump", "Minidump", "Programme", "Computer", "Anwendung" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump-Dateiformat",
  "description":"Erfahren Sie mehr über das DMP-Dateiformat und APIs, die DMP-Dateien erstellen und öffnen können.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Was ist eine DMP-Datei? ##

Die DMP-Datei ist hauptsächlich dem Dateiformat MemoryDump oder Minidump zugeordnet. Es wird im Microsoft Windows-Betriebssystem verwendet, um Daten zu speichern, die aus dem Speicherplatz des Computers ausgegeben wurden. Normalerweise werden DMP-Dateien erstellt, wenn eine Datei abstürzt oder ein Fehler auftritt. Manchmal sind DMP-Dateien für technische Experten oder fortgeschrittene Computerbenutzer sehr wichtig, um die Probleme zu beheben, mit denen Sie konfrontiert sind, und jede Art von Anwendungsproblem zu lösen. Die DMP-Dateien werden als proprietäres Format in Microsoft gespeichert, das vom Betriebssystem zum Debuggen aller auf dem System installierten Anwendungen verwendet wird.


## Technische Spezifikation des DMP-Dateiformats

Unter Windows generiert das Systemtool „savedump.exe“ .dmp-Dateien, die dann von verschiedenen verfügbaren Debugging-Dienstprogrammen verarbeitet werden können. Minidump (64/128 Kb) wird von Windows im Verzeichnis „%SystemRoot%\Minidump“ gespeichert. Andererseits werden der Kernel-Speicher und vollständige Speicherauszüge im Systemstammverzeichnis als 'Memory.dmp'-Dateien gespeichert. Speicherabbilddateien sind relativ große Dateien und können daher ausreichend Speicherplatz beanspruchen. Es wird daher empfohlen, dass die nutzlosen .dmp-Dateien, von denen Sie glauben, dass sie für die Fehlerbehebung nicht nützlich sind, sie dann löschen.

Sie können .dmp-Dateien entweder manuell oder mithilfe des standardmäßigen „Assistenten zum Reinigen von Datenträgern“ auf Ihrem Computer löschen. DMP-Erweiterungen werden von den Oracle-Datenbankprodukten verwendet, um die .dmp-Dateien in erstellten und verwendeten Sicherungs- und Wiederherstellungsdatenbankdateien zu verwenden. Die von Oracle erstellten DMP-Dateien sind Datenbanksicherungen, die zum Importieren oder Wiederherstellen in eine laufende Datenbankinstanz über einen Datenbankserver verwendet werden können. In den meisten Fällen haben .dmp-Dateien Zeit- und Datumsstempel als Dateinamen.

### Inhalt der DMP-Datei

Eine Speicherauszugsdatei enthält:

* Die Stop-Anweisung und ihre Parameter;
* Eine Liste der geladenen Treiber;
* Der Kontext des Prozessors (PRCB) für die Prozesse, die den normalen Betrieb von Windows angehalten haben;
* Der Kernelkontext und die Prozessorinformationen (EPROCESSES) für die angehaltenen Prozesse;
* Der Kernelkontext und die Prozessorinformationen (ETHREAD) für den angehaltenen Thread;
* Der Aufrufstapel im Kernelmodus für den Thread, der die Ausführung des Prozesses beendet hat.


## DMP-Beispiel

Der Stoppfehler 0XC0000218 (Registry_File_Failure) erstellt eine DMP-Datei wie folgt:

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

## Bezug ##

* [DMP – Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

