{
  "date": "2021-04-15",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MPG filformat",
  "keywords": [
"MPG",
"fil",
"udvidelse",
"format",
"videoformat",
"hvad er et mpg-filformat",
"mpg filformat",
"mpg fil afspiller",
"mpeg komprimering",
"video",
"MPEG",
"MPEG-1",
"MPEG-2"
],
  "description": "Lær om MPG-filformat og API'er, der kan oprette og vise, hvordan man åbner MPG-filer.",
  "linktitle": "MPG",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mp-dag"
}
},
  "lastmod": "2021-07-26"
}

## Hvad er et MPG-filformat? ##

The file with a .mpg extension belongs to the group of file extensions for MPEG-1 or MPEG-2 audio and video compression. MPEG-1 Part 2 video is not easily available, and this extension (MPG file format) typically points to a MPEG program stream which is defined in MPEG-1 and MPEG-2, or an MPEG transport stream which is defined in MPEG-2. Der findes også andre udvidelser, såsom .m2ts, der specificerer den nøjagtige beholder, i dette tilfælde MPEG-2 TS, men dette har kun ringe relevans for MPEG-1-medier. [.mp3](/audio/mp3/) er den mest almindelige udvidelse til filer, der indeholder MP3-lyd. En MP3-fil er en typisk strøm af rå lyd; den traditionelle måde at mærke MP3-filer på er ved at skrive streamdata til skrald-segmenter af hver frame, som gemmer medieoplysningerne, men kasseres af **mpg-filafspilleren**. Dette er en lignende teknik, der bruges til at tagge AAC-filer, men mindre understøttet i dag.

## MPEG-komprimering ##

Navnet MPEG står for Moving Pictures Experts Group. MPEG er et værktøj til videokomprimering, som involverer komprimering af billeder og lyde, samt synkronisering af de to.
Der er i øjeblikket flere MPEG-standarder.

- MPEG-1 foreslås til mellemliggende datahastigheder i størrelsesordenen 1,5 Mbit/sek.
- MPEG-2 foreslås til høje datahastigheder på mindst 10 Mbit/sek.
- MPEG-3 blev foreslået til HDTV-komprimering, men blev fundet at være overflødig og blev slået sammen med MPEG-2.
- MPEG-4 foreslås til meget lave datahastigheder på mindre end 64 Kbit/sek.


## Programstrøm af MPG-filformat ##

Programstrømmen er en beholder til multipleksing af digital lyd, video og mere. Program Stream-formatet er specificeret i 1. del af MPEG-1 (ISO/IEC 11172-1) og 1. del af MPEG-2, Systems (ISO/IEC standard 13818-1/ITU-T H.222.0). MPEG-2 Program Stream er analog-baseret og ligner ISO/IEC 11172 Systems lag og fremadkompatibel.

### Kodningsdetaljer ###

Her er kodningsdetaljerne for delvist MPEG-2 Program Stream pack header format:

| Navn | Antal bits | Beskrivelse |
---|---|---|
| sync bytes | 32 | 0x000001BA |
| markør bits | 2 | 01b til MPEG-2 version. Markørbittene for MPEG-1-versionen er 4 bits med værdien 0010b. |
| Systemur [32..30] | 3 | System Clock Reference (SCR) bit 32 til 30 |
| markør bit | 1 | 1 bit altid indstillet. |
| Systemur [29..15] | 15 | Systemur bits 29 til 15 |
| markør bit | 1 | 1 bit altid indstillet. |
| Systemur [14..0] | 15 | Systemur bits 14 til 0 |
| markør bit | 1 | 1 bit altid indstillet. |
| SCR forlængelse | 9 | |
| markør bit | 1 | 1 bit altid indstillet. |
| bithastighed | 22 | I enheder på 50 bytes i sekundet. |
| markør bits | 2 | 11 bits er altid indstillet. |
| reserveret | 5 | reserveret til fremtidig brug |
| fyldelængde | 3 | |
| udfyldningsbytes | 8*fyldlængde | |
| systemhoved (valgfrit) | 0 eller mere | hvis systemhovedets startkode følger: 0x000001BB |

Følgende tabel viser det delvise systemhovedformat:

| Navn | Antal bytes | Beskrivelse |
---|---|---|
| sync bytes | 4 | 0x000001BB |
| header længde | 2 | |
| rate bundne og markør bits | 3 | |
| lydbundet og flag | 1 | |
| flag, markør bit og video bundet | 1 | |
| Pakkehastighedsbegrænsning og reserveret byte | 1 | |


## Referencer ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



