{
  "date": "2021-07-07",
  "keywords": [
"DMP",
"pratęsimas",
"failą",
"formatu",
"sistema",
"Memory Dump",
"Minidump",
"programas",
"kompiuteris",
"taikymas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DMP – MemoryDump failo formatas",
  "description": "Sužinokite apie DMP failo formatą ir API, kurios gali kurti ir atidaryti DMP failus.",
  "linktitle": "DMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dm-ltp"
}
},
  "lastmod": "2021-07-07"
}

## Kas yra DMP failas? ##

DMP failas pirmiausia siejamas su MemoryDump arba Minidump failo formatu. Jis naudojamas Microsoft Windows operacinėje sistemoje duomenims, kurie buvo išmesti iš kompiuterio atminties, saugoti. Paprastai DMP failai sukuriami, kai failas sugenda arba įvyksta klaida. Kartais DMP failai yra labai svarbūs techniniams ekspertams ar pažengusiems kompiuterių vartotojams, siekiant pašalinti iškilusias problemas ir išspręsti bet kokias programos problemas. DMP failai saugomi kaip patentuotas formatas Microsoft, kurį operacinė sistema naudoja bet kuriai sistemoje įdiegtai programai derinti.


## DMP failo formato techninė specifikacija

Windows sistemoje savedump.exe sistemos įrankis generuoja .dmp failus, kuriuos vėliau gali apdoroti įvairios galimos derinimo priemonės. Mini išrašymas (64/128 Kb) yra saugomas languose %SystemRoot%\Minidump kataloge. Kita vertus, branduolio atmintis ir visos atminties išklotinės yra saugomos sistemos šaknyje kaip Memory.dmp failai. Atminties iškelties failai yra gana dideli failai, todėl gali užimti pakankamai vietos saugykloje. Taigi patariama ištrinti nenaudingus .dmp failus, kurie, jūsų manymu, nebus naudingi trikčių šalinimui.

Galite ištrinti .dmp failus rankiniu būdu arba naudodami numatytąjį išvalymo disko vedlį savo kompiuteryje. DMP plėtinius naudoja Oracle duomenų bazės produktai, norėdami naudoti .dmp failus sukurtuose ir naudojamuose atsarginės kopijos ir atkūrimo duomenų bazės failuose. Oracle sukurti DMP failai yra duomenų bazės atsarginės kopijos, kurias galima naudoti importuojant arba atkuriant į veikiančią duomenų bazės egzempliorių per duomenų bazės serverį. Daugeliu atvejų .dmp failų failų pavadinimai yra laiko ir datos antspaudai.

### DMP failo turinys

Atminties ištraukos faile yra:

* Stop sakinys ir jo parametrai;

* Įkeltų tvarkyklių sąrašas;

* Procesoriaus kontekstas (PRCB) procesams, kurie sustabdė normalų Windows darbą;

* Branduolio kontekstas ir procesoriaus informacija (EPROCESSES) procesams, kurie buvo sustabdyti;

* Sustabdytos gijos branduolio kontekstas ir procesoriaus informacija (ETHREAD);

* Branduolio režimo iškvietimo krūva, skirta gijai, kuri užbaigė procesą.



## DMP pavyzdys

Stabdymo klaida 0XC0000218 (Registry_File_Failure) sukuria DMP failą taip:

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

## Nuoroda ##

* [DMP – „Microsoft“](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


