{
  "date" : "2021-08-31",
  "keywords" :[ "xbe fil", "xbe filformat", "vad är en xbe fil", "fil", "xbe exempel", "xbe filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om XBE-filformat och API:er som kan skapa och öppna XBE-filer.",
  "title" :"XBE - iOS Application Package File",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Vad är XBE fil?
En fil med filtillägget .xbe är ett körbart program från en Xbox-videospelskiva. XBE-filerna är huvudfilerna som körs i Xbox-systemet och är inte tänkta att normalt öppnas på en dator, men de kan öppnas på en PC med ett Xbox-emuleringsprogram. Dessa filer skapas vanligtvis av spelutvecklare och signeras sedan av Microsoft. Filstrukturen liknar Windows PE-filerna, men några viktiga ändringar enligt XBox-inställningarna tillämpas för att göra den körbar på XBox.

## XBE filformat
XBE-filen består av en bildrubrik, en samling sektionsrubriker, ett certifikat, lokal lagringsdata för tråd, en samling biblioteksversioner, Microsoft bitmapp och sektionerna som innehåller koden och resurserna.

### Bildhuvud
Bildrubriken innehåller informationen som förklarar var de andra komponenterna i den körbara filen finns i filen och hur den körbara ska behandlas och laddas.

### TLS-tabell
TLS-tabellen består av all information som behövs av XBE för att korrekt konfigurera trådlokal lagring. Den är i grunden unik för TLS-katalogen som finns i PE32-filer och kan kopieras direkt därifrån. Denna tabell kan utelämnas om XBE-filen inte använder någon trådlokal lagring och respektive fält i bildhuvudet är nollställt.

| Offset | Storlek | Namn | Beskrivning |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Raw Data Start | Absolut (dvs inte en RVA) adress för start av TLS-variabeldata i programbilden. |
| 0x0004 | 0x0004 | Rådata slut | Absolut (dvs inte en RVA) adress för slutet av TLS-variabeldata i programbilden. |
| 0x0008 | 0x0004 | Adress till index | Absolut (dvs inte en RVA) adress för variabeln TLS Index. |
| 0x000C | 0x0004 | Adress för återuppringningar | Absolut (dvs inte en RVA) adress för tabellen med nullterminerade TLS-återuppringningsfunktioner. |
| 0x0010 | 0x0004 | Storlek på nollfyllning | Antalet byte efter rådata som ska nollställas i minnet. |
| 0x0014 | 0x0004 | Egenskaper | Beskriver inriktning. |

### Certifikat

Ett certifikat är obligatoriskt för varje körbar Xbox som innehåller information om titlarna:
 


- Tid och datum när certifikatet skapades
- Titel-ID
- Titelnamn
- Alternativa titel-ID:n
- Tillåtna typer av media som den körbara filen kan köras från (HD, DVD, CD, etc.)
- Viltregion
- Spelbetyg
- Disknummer
- Version
- LAN-nyckel rådata som används för System Link
- Signaturnyckelrådata (används för att signera savegames)
- Alternativa signaturnycklar
- Intygets originalstorlek
- Onlinetjänstnamn (finns inte i tidiga körbara filer)
- Säkerhetsflaggor för körtid (finns inte i tidiga körbara filer)
 


### Tillåtna mediatyper
Medietyper som tillåts av den körbara filen att köras från. Följande värden är kända:
| Medietyp | Värde |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Avsnitt
Avsnitten uttrycks av avsnittsrubriker. Sektionsrubrikerna börjar direkt efter certifikatet och innehåller information var i filen de faktiska sektionerna finns. Minst två sektioner finns alltid i en körbar Xbox:


- .text


- .rdata


## Referenser



* [Xbe - XBox Executable](https://xboxdevwiki.net/Xbe)


