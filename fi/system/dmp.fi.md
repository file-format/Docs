{
  "date": "2021-07-07",
  "keywords": [
"DMP",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"Memory Dump",
"Minidump",
"ohjelmia",
"tietokone",
"sovellus"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DMP - MemoryDump-tiedostomuoto",
  "description": "Opi DMP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DMP-tiedostoja.",
  "linktitle": "DMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dm-fip"
}
},
  "lastmod": "2021-07-07"
}

## Mikä on DMP-tiedosto? ##

DMP-tiedosto liitetään ensisijaisesti MemoryDump- tai Minidump-tiedostomuotoon. Sitä käytetään Microsoft Windows -käyttöjärjestelmässä tallentamaan tietoja, jotka on poistettu tietokoneen muistitilasta. Yleensä DMP-tiedostot luodaan, kun tiedosto kaatuu tai tapahtuu virhe. Toisinaan DMP-tiedostot ovat erittäin tärkeitä teknisille asiantuntijoille tai kokeneille tietokoneen käyttäjille ongelmien vianmäärityksessä ja minkä tahansa sovellusongelmien ratkaisemisessa. DMP-tiedostot tallennetaan Microsoftissa omassa muodossa, jota käyttöjärjestelmä käyttää kaikkien järjestelmään asennettujen sovellusten virheenkorjaukseen.


## DMP-tiedostomuodon tekniset tiedot

Windowsissa savedump.exe -järjestelmätyökalu luo .dmp-tiedostoja, jotka voidaan sitten käsitellä erilaisilla käytettävissä olevilla virheenkorjausapuohjelmilla. Ikkunat tallentavat minivedoksen (64/128 kt) hakemistoon %SystemRoot%\Minidump. Toisaalta ytimen muisti ja täyden muistin vedostiedostot tallennetaan järjestelmän juureen Memory.dmp-tiedostoina. Muistin vedostiedostot ovat suhteellisen suuria tiedostoja, joten ne voivat viedä riittävästi tallennustilaa. Joten on suositeltavaa, että hyödyttömät .dmp-tiedostot, jotka eivät mielestäsi ole hyödyllisiä ongelmien vianmäärityksessä, poista ne.

Voit poistaa .dmp-tiedostoja joko manuaalisesti tai käyttämällä tietokoneesi oletusarvoista clean disk Wizard. Oraclen tietokantatuotteet käyttävät DMP-laajennuksia .dmp-tiedostojen käyttämiseen luoduissa ja käytetyissä varmuuskopiointi- ja palautustietokantatiedostoissa. Oraclen luomat DMP-tiedostot ovat tietokannan varmuuskopioita, joita voidaan käyttää tuomiseen tai palauttamiseen käynnissä olevaan tietokanta-ilmentymään tietokantapalvelimen kautta. Useimmissa tapauksissa .dmp-tiedostoissa on aika- ja päivämääräleimat tiedostoniminä.

### DMP-tiedoston sisältö

Muistivedostiedosto sisältää:

* Stop-lause ja sen parametrit;

* Luettelo ladatuista ohjaimista;

* Prosessorin konteksti (PRCB) prosesseille, jotka pysäyttivät Windowsin normaalin toiminnan;

* Ytimen konteksti ja prosessoritiedot (EPROCESSES) pysäytetyille prosesseille;

* Ytimen konteksti ja prosessoritiedot (ETHREAD) keskeytetylle säikeelle;

* Ydintilan kutsupino säikeelle, joka lopetti prosessin suorittamisen.



## DMP esimerkki

Pysäytysvirhe 0XC0000218 (Registry_File_Failure) luo DMP-tiedoston seuraavasti:

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

## Viite ##

* [DMP – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


