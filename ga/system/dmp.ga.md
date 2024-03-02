{
  "date": "2021-07-07",
  "keywords": [
"DMP",
"síneadh",
"comhad",
"formáid",
"córas",
"Dumpáil Cuimhne",
"Minidump",
"cláir",
"ríomhaire",
"iarratas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DMP - Formáid Chomhaid MemoryDump",
  "description": "Foghlaim faoi fhormáid comhaid DMP agus APIanna ar féidir leo comhaid DMP a chruthú agus a oscailt.",
  "linktitle": "DMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dm-gap"
}
},
  "lastmod": "2021-07-07"
}

## Cad is comhad DMP ann? ##

Baineann an comhad DMP go príomha le formáid comhaid MemoryDump nó Minidump. Úsáidtear é i gcóras oibriúcháin Microsoft Windows chun sonraí a dhumpáil ó spás cuimhne an ríomhaire a stóráil. De ghnáth, cruthaítear comhaid DMP nuair a thuairteanna comhad nó nuair a tharlaíonn earráid. Uaireanta bíonn comhaid DMP an-tábhachtach do shaineolaithe teicniúla nó d’úsáideoirí ardleibhéil ríomhairí chun na fadhbanna atá romhat a réiteach agus chun aon cheist iarratais a réiteach. Stóráiltear na comhaid DMP mar fhormáid dhílsithe i Microsoft a úsáideann an córas oibriúcháin chun aon fheidhmchlár atá suiteáilte ar an gcóras a dhífhabhtú.


## Sonraíocht Theicniúil ar Fhormáid Chomhaid DMP

I Windows, gineann an uirlis chórais savedump.exe comhaid .dmp ar féidir iad a phróiseáil ansin trí fhóntais dífhabhtaithe éagsúla atá ar fáil. Stóráiltear miondhumpáil (64/128 Kb) ag fuinneoga san eolaire '%SystemRoot%\Minidump'. Ar an láimh eile, stóráiltear an chuimhne eithne agus na dumpaí cuimhne iomlán ag fréamh an chórais mar chomhaid 'Memory.dmp'. Is comhaid sách mór iad comhaid dumpála cuimhne, mar sin is féidir go dtógfaidh siad go leor spáis stórála. Mar sin moltar na comhaid .dmp gan úsáid a cheapann tú nach mbeidh úsáideach le haghaidh fadhbanna a réiteach ansin iad a scriosadh.

Is féidir leat comhaid .dmp a scriosadh de láimh nó tríd an draoi diosca glan réamhshocraithe a úsáid ar do ríomhaire. Úsáideann táirgí bhunachar sonraí Oracle síntí DMP chun na comhaid .dmp a úsáid i gcomhaid bhunachar sonraí cúltaca agus aisghabhála a chruthaítear agus a úsáidtear. Is cúltacaí bunachar sonraí iad na comhaid DMP a chruthaigh Oracle ar féidir iad a úsáid le hiompórtáil nó le hathchóiriú isteach i mbunachar sonraí reatha trí fhreastalaí bunachar sonraí. I bhformhór na gcásanna, bíonn stampaí ama agus dáta mar chomhadainmneacha ag comhaid .dmp.

### Ábhar an Chomhaid DMP

Tá:

* An ráiteas stad agus a pharaiméadair;

* Tá liosta de na tiománaithe luchtaithe;

* Comhthéacs an phróiseálaí (PRCB) do na próisis a chuir stop le gnáthoibriú Windows;

* An comhthéacs eithne agus faisnéis phróiseálaí (PROCESSES) do na próisis ar cuireadh stop leo;

* An comhthéacs eithne agus faisnéis próiseálaí (ETHREAD) don snáithe a stop;

* Stack glaonna mód eithne don snáithe a chuir deireadh leis an bpróiseas ó fheidhmiú.



## Sampla DMP

Cruthaíonn an earráid stad 0XC0000218 (Registry_File_Failure) comhad DMP mar a leanas:

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

## Tagairt ##

* [DMP - Microsoft]( https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


