{
   "date":"2023-10-18",
   "keywords":[
"stikord",
"cue-fil",
"cue cdrwin cue sheet-fil",
"hvordan man åbner en cue-fil",
"fil",
"cue filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CUE-filformat - CDRWIN Cue Sheet",
   "description":"Lær om CUE CDRWIN Cue Sheet-filformat og API'er, der kan oprette og åbne CUE-filer.",
   "linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin-da",
         "parent":"disc-and-media"
}
},
   "lastmod":"2023-10-18"
}

## Hvad er en CUE fil?

En **.CUE**-fil, også kendt som **CDRWIN Cue Sheet**, er en almindelig tekstfil, der indeholder oplysninger om spor og layout på en lyd-cd eller et diskbillede, typisk i BIN- eller ISO-format. Disse filer bruges ofte til at beskrive strukturen og indholdet af disken, hvilket gør det muligt for CD-brændingssoftware eller virtuelt drevsoftware at gengive den originale disk nøjagtigt.

## Eksempel på CUE-fil

Her er et eksempel på, hvordan .cue-filen kan se ud:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN Cue Sheet

CDRWIN Cue Sheet er en specifik variant af .cue filformat, der bruges af CDRWIN-software. CDRWIN er software til cd/dvd-brænding og redigering, og dets .cue-ark er designet til brug med denne software. Disse .cue-ark indeholder oplysninger, der er nødvendige for, at CDRWIN nøjagtigt kan oprette eller brænde cd'er eller dvd'er.

Her er nogle vigtige detaljer, der er specifikke for CDRWIN Cue Sheets:

1.  **Unik for CDRWIN**: CDRWINs .cue-ark er proprietære formater, der er specifikke for CDRWIN-software. Mens de deler ligheder med standard .cue filer, er de skræddersyet til at arbejde med CDRWINs funktioner og indstillinger.
    
2.  **Brugervenlig grænseflade**: CDRWIN giver en brugervenlig grænseflade til at oprette og redigere sine .cue-ark. Brugere kan tilføje eller ændre oplysninger om spor, indekser, huller og andre parametre på en brugervenlig måde.
    
3.  **Kompatible disktyper**: CDRWIN Cue Sheets bruges primært til at skabe forskellige typer cd'er og dvd'er, herunder datadiske, lyd-cd'er, mixed-mode-diske og mere. Formatet giver brugerne mulighed for at angive type og indhold på disken, de ønsker at oprette.
    
4.  **Kontrol over disklayout**: CDRWIN Cue Sheets giver detaljeret kontrol over diskens layout og struktur, inklusive sporrækkefølge, pause/gab-indstillinger og eventuelle andre specifikke præferencer, som brugeren måtte have.
    
5.  **ISO- og BIN-understøttelse**: CDRWIN kan arbejde med både ISO- og BIN-diskbilledformater. .cue-arket angiver, hvilken billedfil der bruges til disk, hvilket sikrer korrekt synkronisering mellem stikord og billede.
    
6.  **Brænding og ripping**: Disse .cue-ark er afgørende, når du brænder diske eller ripper spor fra diske ved hjælp af CDRWIN. De hjælper med at sikre, at det endelige produkt matcher tiltænkt layout og indhold.
    
7.  **Sikkerhedskopiering og gendannelse**: CDRWIN-brugere opretter ofte .cue-ark, når de laver sikkerhedskopier af deres cd'er eller dvd'er. Disse ark kan senere bruges til at gendanne diskens indhold, inklusive sporlayout og timing.

## Hvordan åbner jeg filen CUE?

CDRWIN Cue Sheets er specielt designet til CDRWIN-software, så de er typisk beregnet til at blive åbnet og brugt i CDRWIN.

Programmer, der åbner eller refererer til CUE filer

- CDRWIN
- Smart Projects IsoBuster
- EZB Systems UltraISO

## Andre CUE-filer

Her er andre filtyper, der bruger filtypen **.cue**.

**Disk og medier**
- [CUE - Cue Sheet File](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## Referencer
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)


