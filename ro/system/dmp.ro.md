{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "extensie", "fișier", "format", "sistem", "MemoryDump", "Minidump", "programe", "calculator", "aplicație"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - Format de fișier MemoryDump",
  "description":"Aflați despre formatul de fișier DMP și despre API-urile care pot crea și deschide fișiere DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Ce este un fișier DMP? ##

Fișierul DMP este asociat în principal cu formatul de fișier MemoryDump sau Minidump. Este folosit în sistemul de operare Microsoft Windows pentru a stoca date care au fost descărcate din spațiul de memorie al computerului. De obicei, fișierele DMP sunt create atunci când un fișier se blochează sau apare o eroare. Uneori, fișierele DMP sunt foarte importante pentru experții tehnici sau utilizatorii avansați de computere pentru a depana problemele cu care vă confruntați și pentru a rezolva orice fel de problemă a aplicației. Fișierele DMP sunt stocate ca format proprietar în Microsoft, care este utilizat de sistemul de operare pentru a depana orice aplicație instalată pe sistem.


## Specificația tehnică a formatului de fișier DMP

În Windows, instrumentul de sistem „savedump.exe” generează fișiere .dmp care pot fi apoi procesate de diverse utilitare de depanare disponibile. Mini dump (64/128 Kb) este stocat de Windows în directorul „%SystemRoot%\Minidump”. Pe de altă parte, memoria nucleului și depozitele de memorie completă sunt stocate la rădăcina sistemului ca fișiere „Memory.dmp”. Fișierele de descărcare în memorie sunt fișiere relativ mari, prin urmare pot ocupa o cantitate suficientă de spațiu de stocare. Prin urmare, se recomandă ca fișierele .dmp inutile despre care credeți că nu vor fi utile pentru depanarea problemelor, apoi le ștergeți.

Puteți șterge fișierele .dmp fie manual, fie utilizând „vrăjitorul de curățare a discului” implicit de pe computer. Extensiile DMP sunt folosite de produsele de baze de date Oracle pentru a utiliza fișierele .dmp în fișierele de bază de date de rezervă și de recuperare create și utilizate. Fișierele DMP create de Oracle sunt copii de siguranță ale bazei de date care pot fi utilizate pentru importarea sau restaurarea într-o instanță de bază de date care rulează printr-un server de bază de date. În cele mai multe cazuri, fișierele .dmp au ca nume de fișier ștampile de oră și dată.

### Conținutul fișierului DMP

Un fișier de descărcare a memoriei conține:

* Declarația stop și parametrii acesteia;
* O listă de drivere încărcate;
* Contextul procesorului (PRCB) pentru procesele care au oprit funcționarea normală a Windows;
* Contextul nucleului și informațiile procesorului (EPROCESE) pentru procesele care au fost oprite;
* Contextul nucleului și informațiile procesorului (ETHREAD) pentru firul care s-a oprit;
* Stiva de apeluri în modul kernel pentru firul de execuție care a încheiat procesul.


## Exemplu DMP

Eroarea de oprire 0XC0000218 (Registry_File_Failure) creează un fișier DMP după cum urmează:

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

## Referință ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

