{
  "date": "2021-06-30",
  "keywords": [
"exe-fil",
"exe filformat",
"hvad er en exe-fil",
"fil",
"exe eksempel",
"exe filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "En .exe-fil er en Microsoft-eksekverbar fil, der køres på Windows OS. Få mere at vide om EXE-filformat.",
  "title": "Hvad er en eksekverbar EXE-fil?",
  "linktitle": "EXE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ex-dae"
}
},
  "lastmod": "2021-06-30"
}

## Hvad er en EXE-fil?

Ordet EXE er en forkortelse for **eksekverbar**. En .exe-fil er et program, der kan køres på Microsoft Windows-operativsystemet. Applikationsudviklere udgiver for det meste deres programmer til Windows OS i eksekverbart format som exe-filer. Det er standardfilformatet til at køre programmer på Windows. **Setup.exe**, **Install.exe** og **cmd.exe** er nogle almindelige og velkendte navne på EXE-filer.

## EXE filformat

MS-DOS-kompilere blev introduceret med hukommelsesmodellerne med 64K-hukommelsesbegrænsningen. Det generelle koncept er at indstille forskellige segmentregistre i x86 CPU'en (CS, DS, ES, SS) til at pege på de forskellige eller samme segmenter, hvilket giver forskellige grader af adgang til hukommelsen. Nogle specifikke hukommelsesmodeller var:

- **Tiny**: Alle hukommelsesadgange er 16-bit (segmentregistre uændrede). Producerer en .COM-fil i stedet for en .EXE-fil.
- **Lille**: Alle hukommelsesadgange er 16-bit (segmentregistre uændrede).
- **Kompakt**: Dataadresser inkluderer både segment og offset, genindlæsning af DS- eller ES-registrene ved adgang og tillader op til 1M data. Kodeadgange ændrer ikke CS-registret, hvilket tillader 64K kode.
- **Medium**: Kodeadresser inkluderer segmentadressen, genindlæsning af CS ved adgang og tillader op til 1M kode. Dataadgange ændrer ikke DS- og ES-registrene, hvilket tillader 64K data.
- **Stor**: Både kode- og dataadresser er (segment, offset) par, der altid genindlæser segmentadresserne. Hele 1M byte hukommelsesplads er tilgængelig for både kode og data.
- **Kæmpe**: Samme som den store model, med yderligere aritmetik, der genereres af compileren for at give adgang til arrays større end 64K.

Udviklerne skal beslutte, hvilken model der skal vælges, mens de opretter en exe-fil.

### Bærbart EXE-filformat

Det bærbare eksekverbare filformat (PE) indeholder en række informationsoverskrifter, følgende er listen over overskrifter:

- **DOS-header**: MS-DOS-header sikrer enten bagudkompatibilitet eller en yndefuld tilbagegang af nye filtyper.
- **PE Header**: Ved offset 60 (0x3C) fra begyndelsen af DOS-headeren er der en pegepind til PE-filens header
- **COFF Header**: COFF-headeren har nogle oplysninger, der er nyttige for en eksekverbar, og nogle oplysninger, der er mere nyttige for en objektfil.
- **PE valgfri header**: PE valgfri header forekommer direkte efter COFF header, og nogle kilder viser endda de to headers som værende en del af den samme struktur.
- **Sektionstabel**: Umiddelbart efter PE Optional Header finder vi en sektionstabel. Sektionstabellen består af en række IMAGE_SECTION_HEADER-strukturer.
- **Mappable Sections**: Kan spare plads i hukommelsen ved at kortlægge koden for et bibliotek til mere end én proces.

## Kan du køre en EXE-fil på en Mac?

Exe-filer bruges ikke som eksekverbare filer på Mac OS. Men hvis du vil køre en exe-fil på Mac OS, kan følgende metoder bruges.

 1. **Vin** - Vin er den perfekte løsning for folk, der ønsker at bruge deres pc-applikationer på Mac-systemer. Det er et akronym, der står for Wine Is Not A Emulator, hvilket betyder. Wine opretter det samme miljø af mapper som brugt af Microsoft, så du kan køre dit Windows-program ved hjælp af det.
 2. **Virtuelle maskiner** - Opret en virtuel Windows-maskine ved hjælp af Parallel Desktop eller VM Virtual Box og kør dit program inde i den virtuelle maskine.
 3. **Boot Camp** - Installation og konfiguration af Windows Boot Camp på Mac OS lader dig køre Windows OS på Mac-maskine.

## Referencer

* [.exe- af Wikipewdia](https://en.wikipedia.org/wiki/.exe)

* [x86 demontering/Windows eksekverbare filer](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)


