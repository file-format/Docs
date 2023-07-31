{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "estensione", "file", "formato", "sistema", "MemoryDump", "Minidump", "programmi", "computer", "applicazione" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - Formato file MemoryDump",
  "description":"Scopri il formato di file DMP e le API che possono creare e aprire file DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Che cos'è un file DMP? ##

Il file DMP è principalmente associato al formato di file MemoryDump o Minidump. Viene utilizzato nel sistema operativo Microsoft Windows per archiviare i dati che sono stati scaricati dallo spazio di memoria del computer. Di solito, i file DMP vengono creati quando un file si arresta in modo anomalo o si verifica un errore. A volte i file DMP sono molto importanti per esperti tecnici o utenti di computer avanzati per risolvere i problemi che stai affrontando e risolvere qualsiasi tipo di problema con l'applicazione. I file DMP vengono archiviati come formato proprietario in Microsoft che viene utilizzato dal sistema operativo per eseguire il debug di qualsiasi applicazione installata sul sistema.


## Specifiche tecniche del formato file DMP

In Windows, lo strumento di sistema "savedump.exe" genera file .dmp che possono essere quindi elaborati da varie utilità di debug disponibili. Il mini dump (64/128 Kb) viene archiviato da Windows nella directory '%SystemRoot%\Minidump'. D'altra parte, la memoria del kernel ei dump della memoria completa sono archiviati nella radice del sistema come file "Memory.dmp". I file di dump della memoria sono file relativamente grandi, quindi possono richiedere una quantità sufficiente di spazio di archiviazione. Quindi si consiglia di eliminare i file .dmp inutili che ritieni non siano utili per la risoluzione dei problemi, quindi eliminarli.

È possibile eliminare i file .dmp manualmente o utilizzando la "procedura guidata di pulizia del disco" predefinita sul computer. Le estensioni DMP vengono utilizzate dai prodotti di database Oracle per utilizzare i file .dmp nei file di database di backup e ripristino creati e utilizzati. I file DMP creati da Oracle sono backup di database che possono essere utilizzati per l'importazione o il ripristino in un'istanza di database in esecuzione tramite un server di database. Nella maggior parte dei casi, i file .dmp hanno l'ora e la data come nomi di file.

### Contenuto del file DMP

Un file di dump della memoria contiene:

* L'istruzione stop e i suoi parametri;
* Un elenco di driver caricati;
* Il contesto del processore (PRCB) per i processi che hanno interrotto il normale funzionamento di Windows;
* Il contesto del kernel e le informazioni sul processore (EPROCESSES) per i processi che sono stati arrestati;
* Il contesto del kernel e le informazioni sul processore (ETHREAD) per il thread interrotto;
* Lo stack di chiamate in modalità kernel per il thread che ha interrotto l'esecuzione del processo.


## Esempio DMP

L'errore di arresto 0XC0000218 (Registry_File_Failure) crea un file DMP come segue:

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

## Riferimento ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

