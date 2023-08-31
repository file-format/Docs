{
  "date" : "2019-10-11",
  "keywords" :[ "rar fil", "rar filformat", "vad är en rar fil", "fil", "rar exempel", "rar filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Vad är ett RAR-filtillägg och API:er som kan skapa och öppna RAR-filer.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en RAR-fil?

Filer med tillägget .rar är arkivfiler som skapas för att lagra information i komprimerad eller normal form. RAR, som står för Roshal ARchive file format, är ett proprietärt filformat skapat av Eugene Roshal 1995 som var en rysk mjukvaruingenjör. Formatet används för att arkivera filer med olika metoder inklusive olika komprimeringstekniker. Det finns flera applikationsprogram tillgängliga för Windows, Linux och MacOS för extrahering av RAR-filer. WinRAR-mjukvaran, av RARLab, är filarkiveringsverktyget för shareware (gratis i 40 dagar) för Microsoft Windows-plattformen; programvaran portades till Linux (endast som extraktor) av samma författare, Eugene Roshal.

## Versionshistorik för RAR-filformat

* v1.3 (original, har ingen "Rar!"-signatur)
* v1.5
* v2.0 - släppt med WinRAR 2.0 och Rar för MS-DOS 2.0
* v2.9 - släppt i WinRAR version 3.00
* v5.0 - stöds av WinRAR 5.0 och senare

## Nyckelfunktioner i RAR-format

RAR har funnits på området ganska länge och har varit ett av favoritformaten för arkivering. Nyckelfunktioner om RAR-formatet är:

**`Högt kompressionsförhållande:`** Överlägset jämfört med [ZIP](/sv/compression/zip/), jämförbart med 7z- och zipx-format.

**`Stark filkryptering genom design:`** Krypterade RAR4-arkiv förlitar sig på AES-128-baserad kryptering medan krypterade RAR5-arkiv förlitar sig på AES-256-kryptering med förbättrad nyckelschemaläggning

**`Avancerad felkorrigering och dataåterställningsfunktioner:`** valfria återställningsposter under skapande av arkiv

**`Filstorlek:`** Minst 20 byte och högst 2^63 byte i storlek (8 exabyte av arkivets totala storlek)

**`RAR-arkiv med flera volymer:`** Möjlighet att dela upp stora arkiv i flera mindre filer för att underlätta överföring över nätverket. I sådana fall ökas filtilläggen med 1 för att representera delade volymer

## RAR filformat

Fullständiga specifikationer för RAR-format är inte tillgängliga offentligt och det är därför som detaljer om formatet inte kan formuleras på ett kortfattat sätt.

### Allmän arkivlayout

Den allmänna layouten för ett RAR-filformat som introducerades i version 5.0 är som följer:

|Filformat
---|
|Självextraherande modul (valfritt)
|RAR 5.0 Signatur
|Arkivkrypteringshuvud (valfritt)
| Huvudarkivhuvud
|Rubrik för arkivkommentartjänst (valfritt)
Filhuvud 1
|Tjänsterubriker (NTFS ACL, strömmar, etc.) för föregående fil (valfritt)
|...
|Filhuvud N
|Tjänsterubriker (NTFS ACL, strömmar, etc.) för föregående fil (valfritt)
|Återställningspost (valfritt)
|Slut på arkivhuvud

Information om varje avsnitt av RAR-filen som nämns ovan finns i dokumentet [RAR 5.0 filformatsspecifikationer](https://www.rarlab.com/technote.htm#arcstruct).

#### Självextraherande RAR-arkiv

Om själva RAR-filen är självextraherande, finns den självextraherande informationen i början av filen som föregår arkivsignaturen. Dess storlek och innehåll är inte definierade.

#### RAR 5.0 Signatur

RAR-signaturen är en 8-byte header som består av följande magiska nummer:

0x 52 61 72 21 1A 07 00

var

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Referenser

* [RAR 5.0 arkivformat](https://www.rarlab.com/technote.htm)
* [RAR - av Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))

