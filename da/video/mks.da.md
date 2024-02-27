{
  "date": "2021-24-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MKS filformat",
  "keywords": [
"mks",
"matroska video",
"mkv format",
"fil",
"format",
"video"
],
  "description": "Lær om MKS-filformat for undertekster, der kun er oprettet af Matroska og API'er, der kan oprette og åbne MKS-filer.",
  "linktitle": "MKS",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-das"
}
},
  "lastmod": "2021-25-02"
}

## Hvad er en MKS fil?

The MKS files are generally known as Matroska files containing subtitles only. Although the Matroska is a general file container, it avoids keeping the information of specific formats. Since subtitles are being used in some of the audio or video containers, Matroska is paying attention to store some common subtitle formats. It helps Matroska to be consistent with the growth rate. You need to follow the points as given below to store the subtitles in Matroska:

- .mks. udvidelsen vil blive brugt af Matroska-filen (der kun indeholder undertekster).
- **CodecPrivate** bruges til at gemme alle codecs-relaterede oplysninger, der er globale for en hel stream.
- Fjern de start- og stoptidsstempler, der bruges i et tidsstemplets oprindelige lagerformat. Brug i stedet blokkens tidsstempling og varighed.
- Du kan bruge alt med et gennemsigtigt lag, inklusive en video.

## Almindelige undertekstformater

Here are some brief notes about more common subtitle formats stored in Matroska:

### Billeder undertekster
VobSub-undertekstformatet er det første billedundertekstformat, der importeres til Matroska. Dette format genereres ved at eksportere underteksterne fra en DVD. Sporene skal adskilles under lagring i Matroska, hvis VobSub'en består af et sæt af flere streams.

### SRT-undertekster
The SRT is the most simple and basic of all subtitle formats. It consists of four parts as given below:
 
 1. Et tal, der angiver rækkefølgen af underteksten.
 2. Undertekster vises og forsvinder tid på skærmen.
 3. Selve underteksten.
 4. En tom linje for at angive starten på den næste undertekst.
 
### SSA/ASS undertekster
Sub Station Alpha (SSA) er et filformat, der bruges af den populære underteksteditor SubStation Alpha. SSA-underteksterne er meget brugt af fansubbere. Den har mulighed for at vise moderne funktioner, fx karaoke, positionering, styling mv.
 
### WebVTT-undertekster
World Wide Web Consortium (W3C) udviklede WebVTT, som er forkortet som Web Video Text Tracks Format. Dette format bruges til at markere eksterne tekstsporressourcer i forbindelse med HTML-elementet.

### HDMV præsentation grafik undertekster
HDMV-præsentationsgrafikundertekstformatet (HDMV PGS) er en serie af bitmaps, og vi kan slet ikke sige det tekst. Med andre ord kan man sige, at det kun er en tidsindstillet sekvens af grafiske billeder. For at udtrække informationen er konvertering af PGS til SRT en nødvendig proces.

### HDMV-tekstundertekster
HDMV-teksten er kendt som det tekstmæssige undertekstformat, der bruges på Blu-rays. Matroska tillader kun UTF-8-tegnsæt When gemmer TextST-underteksterne.

### Digital Video Broadcasting (DVB) undertekster
DVB undertekstformatet blev introduceret til regulering af transmission og visning af flere sprog undertekstning på tv-signaler. Et typisk undertekstformat ville også give enhver seer mulighed for at se DVB-underteksttransmissioner, uanset hvilken producent der er af transmissionssystemerne.


## Referencer ##

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)

