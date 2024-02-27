{
  "date": "2021-07-12",
  "keywords": [
"cmd-fil",
"hvad er en cmd-fil",
"fil",
"cmd eksempel",
"cmd filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om CMD-filformat og API'er, der kan oprette og åbne CMD-filer.",
  "title": "CMD - Windows Command File Format",
  "linktitle": "CMD",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cm-dad"
}
},
  "lastmod": "2021-07-12"
}

## Hvad er en CMD fil?
En CMD-fil består af et script, der indeholder en eller flere kommandoer i form af almindelig tekst, der køres for at udføre forskellige opgaver. Det ligner en [BAT](/executable/bat/) fil, som også generelt bruges til at gemme en batch af eksekverbare kommandoer. CMD-filerne er meget brugt i Microsoft Windows-operativsystemet. Disse filer blev introduceret i næsten i 90'erne, men stadig brugt i det nyeste Windows-operativsystem. Disse filer er generelt skrevet til at udføre mere end én kommando i en sekvens.

## CMD filformat
CMD er et filformat, der bruges af eksekverbare programmer i CP/M-stil. Det er generelt sammenligneligt med [COM](/executable/com/) i CP/M-80 og [EXE](/executable/exe/) i DOS. En CMD-fil indeholder 1 til 8 grupper af kode eller data og en 128-byte header. Hver gruppe kan være op til 1 mb stor. CMD-filer kan også indeholde oplysninger om omplacering og Resident System Extensions (RSX'er) i dens senere versioner. CMD'en er en nykommer sammenlignet med filen [BAT](/executable/bat/); brugt til MS-DOS før udgivelsen af Windows i MS-DOS. Selvom du stadig kan gemme filer med .bat-udvidelsen i dag, bruger mange mennesker .cmd-udvidelsen til at gemme deres eksekverbare scripts.

### CMD-formatspecifikation

Starten af overskriften indeholder listen over de grupper, der er til stede i filen, sammen med deres typer. Hver type kan højst bruges én gang. Disse typer er:

- Kode
- Data
- Ekstra
- Stak
- Bruger 1
- Bruger 2
- Bruger 3
- Bruger 4
- Delt kode

Ligeledes Program Segment Prefix i DOS er de første 256 bytes af datagruppen nul. De vil blive udfyldt af CP/M-86 med nulsiden. Hvis der ikke er nogen datagruppe, vil de første 256 bytes af kodegruppen blive brugt i stedet.
## CMD fil eksempel
Følgende er et eksempel på et CMD-script til at vise systemoplysninger.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Referencer 

* [Sådan skriver man et CMD-script](https://smallbusiness.chron.com/write-cmd-script-53226.html)

* [CMD-fil (CP/M) - af Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))


