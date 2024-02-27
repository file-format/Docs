{
  "date": "2021-06-09",
  "keywords": [
"m4b",
"mp3",
"fil",
"udvidelse",
"format",
"hvad er m4b filformat",
"musik",
"m4b filformat",
"M4b vs MP3",
"m4b filformatspecifikation"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om M4B-filformater og API'er, der kan oprette, konvertere og åbne M4B-filer.",
  "title": "M4B - MPEG-4 lydbog filformat",
  "linktitle": "M4B",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-dab"
}
},
  "lastmod": "2021-06-09"
}

## Hvad er en M4B fil?

Filen med filtypenavnet .m4b er en lydbog, der generelt bruges af Apple Books og iTunes. Lyden, der bruges i dette format, gemmes i MPEG-4 og komprimeres ved hjælp af AAC-kodning. En M4B-fil minder meget om M4A, men den understøtter de lydbogsrelaterede funktioner, såsom bogmærke og kapitelskift. M4B-filerne er tilgængelige i både DRM-aktiverede og DRM-fri versioner. DRM-krypterede lydbøger er normalt betalte lydbøger fra iTunes Store. Hvorimod DRM-fri nemt kan findes over internettet.

## M4B filformat

Lydbogsfilerne, der indeholder metadata, billeder, bogmærker og hyperlinks, kan gemmes med .m4a-udvidelsen, men generelt bruges .m4b-udvidelsen under lagring, blot for at angive, at filen har et lydbogsfilformat. Fairplay DRM (Digital Rights Management) bruges af application til at beskytte deres M4B-filer. Så de filer, der er downloadet fra iTunes, kan kun afspilles på autoriserede enheder eller computere.


## M4B vs M4A

Både M4B og [MP3](/audio/mp3/) er kun lydfilformater.

**M4B**: Vinder sammenlignet med MP3 med hensyn til kvalitet, hvis begge kodes med samme bithastighed. M4B er en lydbogsfil, som er komprimeret ved hjælp af AAC-kodning. Det er dybest set forbundet med MPEG-4 Audio Layer, filer med .m4b-udvidelse er lydlaget i MPEG-4-film, men med ekstra lydbogsrelaterede funktioner. Dens mål er at overhale MP3 og blive den nye standard inden for lydkomprimering. Det er meget tæt på MP3 på mange måder, men udviklet til at have en bedre kvalitet i samme eller endnu mindre filstørrelse. M4B-formatet blev først introduceret af Apple. Formattypen er også realiseret som Apple Lossless Encoder (ALE).

Derfor kunne M4B i øjeblikket ikke få MP3'ens mainstream-succes, fordi lydformatet ikke almindeligvis kan afspilles endnu.

**Mp3**: Et digitalt lydformat, som er velkendt for alle. Et allerførste komprimeringsformat på scenen og blev meget berømt blandt musiklyttere. Dens mainstream-succes er så hurtig, at filtypen er i stand til at blive afspillet universelt og kompatibel med næsten alt, hardware eller software. I en generel forstand vil M4A producere bedre lydkvalitet, men mange vil hævde, at uanset om det er sandt eller ej, er lydforskellen ikke sammenlignelig, og det ville være spild af tid at forsøge at konvertere MP3-filer til M4A-filer. Endelig vil konverteringen bare få dig til at miste den originale lydkvalitet.

## M4B filformatspecifikation

I lighed med [M4A](/audio/m4a/) består M4B-filerne også af på hinanden følgende bidder. Hver chunk har 8 byte header og underinddelt som:
- 4-byte chunk størrelse (big-endian, høj byte først)
- 4-byte chunk type - en af foruddefinerede signaturer: ftyp, mdat, moov, pnot, moof, udta, uuid, free, ctab, spring over, jP2, bred, indlæs, imap, mat, chap, kmat, klip, crgn, sync, tmcd, PICT , scpt, ssrc.

Similar to M4A the First chunk in M4B will be of type "ftype" and has a sub-type at offset 8. M4B defineret af undertype, som skal være M4B_.

Gentager bidder, indtil bidder af ukendt type er fundet, vil den komponere M4B (MPEG-4 Audio) fil.

## Referencer

* [MPEG-4 del 14 - af Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Eksempel](https://www.file-recovery.com/m4a-signature-format.htm)


