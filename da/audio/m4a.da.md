{
  "date": "2021-04-26",
  "keywords": [
"m4a",
"mp3",
"fil",
"udvidelse",
"format",
"hvad er m4a filformat",
"musik",
"m4a filformat",
"M4A vs MP3",
"m4a filformatspecifikation"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om M4A-filformat og API'er, der kan oprette, konvertere og åbne M4A-filer.",
  "title": "M4A - MPEG-4 lydfil",
  "linktitle": "M4A",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-daa"
}
},
  "lastmod": "2021-04-26"
}

## Hvad er en M4A fil?

**M4A-filformatet** er en lydfil, der er oprettet ved hjælp af AAC (Advanced Audio Coding), som er kendt som en tabskomprimering. Ordet M4A forkortet til MPEG 4 Audio. Disse lydfiler har normalt filtypenavnet .m4a. Dette gælder især for ubeskyttet indhold. Det kan gemme forskellige typer lydindhold, såsom lydbøger, sange og podcasts. M4A er normalt realiseret som mere avanceret format end MP3, som ikke typisk var designet til kun lyd. Det er blot et lydlag i MPEG 1 eller 2 videofiler.

M4A-formatet er krypteret af FairPlay Digital Rights Management, da det blev solgt via iTunes Store med .m4p-udvidelsen. Apple iPhones bruger MPEG-4-lyd til deres ringetoner, men disse lydfiler bruger .m4r-udvidelsen.


## M4A vs MP3

Både M4A og [MP3](/audio/mp3/) er kun lydfilformater.

**M4A**: Bedre end MP3 med hensyn til kvalitet og størrelser, når den er kodet med samme bithastighed. Filtypenavnet .m4a er så almindeligt, fordi de er blevet brugt af Apple til brug i iTunes Music Store. M4A er en lydfil, som er komprimeret ved hjælp af MPEG-4-teknologi; en algoritme til komprimering med tab. Det er dybest set forbundet med MPEG-4 Audio Layer, filer med filtypenavnet .m4a er lydlaget i MPEG-4-film. Det er beregnet til at overhale MP3 og blive den nye standard inden for lydkomprimering. Det er meget tæt på MP3 på mange måder, men introduceret for at have en bedre kvalitet i samme eller endnu mindre filstørrelse. M4A-formatet blev først introduceret af Apple. Formattypen er også realiseret som Apple Lossless Encoder (ALE).

Derfor kunne M4A i øjeblikket ikke få MP3'ens mainstream-succes, fordi lydformatet generelt ikke kan afspilles endnu. Det er på en eller anden måde kun begrænset til MacOS, iPod og andre Apple-produkter.

**Mp3**: Det mest berømte digitale lydformat. Det var også et af de første komprimeringsformater på scenen og blev meget populært blandt musikelskere. Dens mainstream-succes er så hurtig, at filtypen er i stand til at blive afspillet universelt og med næsten alt, hardware eller software. I en generel forstand vil M4A producere bedre lydkvalitet, men mange vil hævde, at uanset om det er sandt eller ej, er lydforskellen ikke til at skelne, og det ville være spild af tid at forsøge at konvertere MP3-filer til M4A-filer. Til sidst vil konverteringen bare få dig til at miste den originale lydkvalitet.

## M4A filformatspecifikation

M4A-filerne består af på hinanden følgende bidder. Hver chunk har 8 byte header og underinddelt som:
- 4-byte chunk størrelse (big-endian, høj byte først)
- 4-byte chunk type - en af foruddefinerede signaturer: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, wide, load, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt , ssrc, PICT.

First chunk will be of type "ftype" and has a sub-type at offset 8. M4A defineret af undertype, som skal være M4A_, for M4B skal undertype være M4B_ og for M4P skal undertype være M4P_.

Gentager bidder, indtil bidder af ukendt type er fundet, vil den komponere M4A (MPEG-4 Audio) fil.

## Referencer ##

* [MPEG-4 del 14 - af Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Eksempel](https://www.file-recovery.com/m4a-signature-format.htm)


