{
  "date": "2019-10-11",
  "keywords": [
"rar fil",
"rar filformat",
"hvad er en rar-fil",
"fil",
"rar eksempel",
"rar filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RAR",
  "description": "Hvad er en RAR filtypenavn og API'er, der kan oprette og åbne RAR filer.",
  "linktitle": "RAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ra-dar"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en RAR fil?

Filer med filtypenavnet .rar er arkivfiler, der er oprettet til lagring af information i komprimeret eller normal form. RAR, som står for Roshal ARchive filformat, er et proprietært filformat skabt af Eugene Roshal i 1995, som var en russisk softwareingeniør. Formatet bruges til at arkivere filer med forskellige metoder, herunder forskellige komprimeringsteknikker. Der findes adskillige applikationssoftware til Windows, Linux og MacOS til udtrækning af RAR-filer. WinRAR-software fra RARLab er shareware-filarkiveringsværktøjet (gratis i 40 dage) til Microsoft Windows-platformen; softwaren blev overført til Linux (kun som udtrækker) af den samme forfatter, Eugene Roshal.

## Versionshistorik for RAR-filformat

* v1.3 (original, har ikke "Rar!"-signatur)

* v1.5

* v2.0 - udgivet med WinRAR 2.0 og Rar til MS-DOS 2.0

* v2.9 - udgivet i WinRAR version 3.00

* v5.0 - understøttet af WinRAR 5.0 og nyere


## Nøglefunktioner i RAR-format

RAR har været i feltet i ret lang tid og har været et af de foretrukne arkiveringsfilformater. Nøglefunktioner ved RAR-formatet er:

**`Højt kompressionsforhold:`** Overlegen sammenlignet med [ZIP](/compression/zip/), sammenlignelig med 7z- og zipx-format.

**`Stærk filkryptering ved design:`** Krypterede RAR4-arkiver er afhængige af AES-128-baseret kryptering, mens krypterede RAR5-arkiver er afhængige af AES-256-kryptering med forbedret nøgleplanlægning

**`Avanceret fejlkorrektion og datagendannelsesfunktioner:`** valgfri gendannelsesposter under oprettelse af arkiv

**`Filstørrelse:`** Minimum 20 bytes og maksimalt 2^63 bytes i størrelse (8 exabytes af den samlede størrelse af arkivet)

**`Multi-volume RAR Archives:`** Mulighed for at opdele store arkiver i flere mindre filer for at lette overførsel over netværket. I sådanne tilfælde øges filtypenavnene med 1 for at repræsentere opdelte volumener

## RAR filformat

Fuldstændige specifikationer af RAR-format er ikke tilgængelige offentligt, og det er grunden til, at detaljer om formatet ikke kan formuleres på en kortfattet måde.

### Generelt arkivlayout

Det generelle layout af et RAR-filformat introduceret i version 5.0 er som følger:

|Filformat
---|
|Selvudpakkende modul (valgfrit)
|RAR 5.0 Signatur
|Arkivkrypteringshoved (valgfrit)
| Hovedarkivhoved
|Arkiv kommentartjenesteoverskrift (valgfrit)
Filoverskrift 1
|Tjenestehoveder (NTFS ACL, streams osv.) for foregående fil (valgfrit)
|...
|Filhoved N
|Tjenestehoveder (NTFS ACL, streams osv.) for foregående fil (valgfrit)
|Recovery Record (valgfrit)
|Slut på arkivhoved

Oplysninger om hver del af RAR-filen nævnt ovenfor kan findes i [RAR 5.0 File Format specifications](https://www.rarlab.com/technote.htm#arcstruct)-dokumentet.

#### Selvudpakkende RAR-arkiver

Hvis selve RAR-filen er selvudpakkende, er den selvudpakkende information indeholdt i starten af filen forud for arkivsignaturen. Dens størrelse og indhold er ikke defineret.

#### RAR 5.0 Signatur

RAR-signaturen er en 8-bytes header, der består af følgende magiske tal:

0x 52 61 72 21 1A 07 00

hvor

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Referencer

* [RAR 5.0 arkivformat](https://www.rarlab.com/technote.htm)

* [RAR - Af Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))


