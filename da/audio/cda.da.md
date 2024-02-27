{
  "date": "2021-06-09",
  "keywords": [
"cda",
"fil",
"udvidelse",
"format",
"hvad er en cda-fil",
"musik",
"cda filformat",
"cda filformatspecifikation"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om CDA-filformater og API'er, der kan oprette, konvertere og åbne CDA-filer.",
  "title": "CDA - CD-lydsporsgenvejsfil",
  "linktitle": "CDA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-cda"
}
},
  "lastmod": "2021-06-09"
}

## Hvad er en CDA fil?

En fil med filtypenavnet .cda er en lille stubfil genereret af Microsoft Windows for hvert lydspor på en lyd-cd. Disse filer indeholder en typisk information såsom sportider og en Windows-genvej, der giver brugerne adgang til de specifikke lydspor. CDA-filerne er ikke musik, men de peger på en musikfil, der findes et sted på lageret. Vi kan sige det som en genvej til en lydfil, som er placeret på en cd.

## CDA filformat

CDA-filformatet bruges til at fortælle en computer, hvilken lydfil der skal afspilles på en cd. Så CDA-filerne bliver ubrugelige adskilt fra en cd, de repræsenterer. CDA-filerne betragtes almindeligvis som RIFF-ressourcer. Der er kun én del, der hedder CDDA og kun indeholder en datablok kaldet FMT i den aktuelle version af .cda-filen. Denne blok er 24 byte lang. Identifikationen, der er oprettet af Windows, bruges af det Windows 95- og Windows 98-relaterede cd-drev, og dets afspiller kan ikke oprette forbindelse til FreeDB eller CDDB. For at den kan vise sangtitel og kunstnernavn, som du skal manuelt indtaste disse oplysninger i filen cdplayer.ini.

### Organisering af en CDA-fil

Følgende tabel viser oplysningerne om typiske forskydninger:
| forskydning | længde | indhold |
---|---|---|
| 0x00 | 4 | de 4 ASCII-tegn RIFF |
| 0x04 | 4 | størrelsen af følgende chunk: altid 36 (44 - 8), på 4 bytes (Intel orden) |
| 0x08 | 4 | chunk identifier: the 4 ASCII characters "CDDA"-da |
| 0x0C | 4 | de 3 ASCII-tegn fmt efterfulgt af et mellemrum |
| 0x10 | 4 | længden af klumpen: altid 24, på 4 bytes (Intel rækkefølge) |
| 0x14 | 2 | version of the CD format, on 2 bytes (Intel order). In May 2006, always equal to 1. |
| 0x016 | 2 | number of the range, on 2 bytes (Intel order). The first track has the number 1. |
| 0x18 | 4 | identifikator beregnet af Windows for cdplayer.exe. |
| 0x1c | 4 | rækkevidde offset, i antal billeder (Intel rækkefølge) |
| 0x20 | 4 | sporets varighed, samlet antal billeder (Intel-rækkefølge) |
| 0x24 | 1 | rækkevidde position: rammer |
| 0x25 | 1 | rækkevidde position: sekunder |
| 0x26 | 1 | rækkevidde position: minutter |
| 0x27 | 1 | en nulbyte (binær værdi 0) |
| 0x28 | 1 | sporets varighed: rammer |
| 0x29 | 1 | sporets varighed: sekunder |
| 0x2a | 1 | sporets varighed: minutter |
| 0x2b | 1 | en nulbyte (binær værdi 0) |

## Referencer

* [.cda-fil - af Wikipedia](https://en.wikipedia.org/wiki/.cda_file)


