{
  "date": "2021-06-09",
  "keywords": [
"m4p",
"mp3",
"fil",
"udvidelse",
"format",
"hvad er m4p filformat",
"musik",
"m4p filformat",
"M4b vs MP3",
"m4p filformatspecifikation"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om M4P-filformat og API'er, der kan oprette, konvertere og åbne M4P-filer.",
  "title": "M4P - MPEG-4 lydbog filformat",
  "linktitle": "M4P",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-dap"
}
},
  "lastmod": "2021-06-09"
}

## Hvad er en M4P fil?
Filen med filtypenavnet .m4p er en lydfil, som normalt er tilgængelig i Apple iTunes Store til download. Med de andre ord kan vi sige, at M4P er en AAC-fil, men kopibeskyttet ved hjælp af en Digital Rights Management (DRM). Det betyder, at M4P-filer kun kan afspilles på autoriserede systemer eller enheder. Normalt er M4P-filer specifikke for Apples multimedieenheder. Så disse filer kan kun afspilles på Apple macbooks, podcasts, smartphones som iPhone 6 eller iPhone 7.

## M4P filformat
M4P står for MPEG 4 Protected (lyd), og den koder lyden med avanceret audio-codec (AAC) og beskytter filen mod uautoriseret brug af filen. Dette filformat betragtes normalt som et iTunes Music Stores lydfilformat. Apple bruger sit FairPlay Digital Rights Management-system (DRM) til at beskytte M4P-filer. FairPlay DRM er baseret på teknologi udviklet af Veridisc. Dens beskyttelsesmekanisme fungerer ved at kryptere AAC-lydstrømmen ved hjælp af AES-krypteringen. Brugeren modtager en hovednøgle, som er tildelt hans konto til dekryptering. Dette filformat blev introduceret som en erstatning for MP3-filformatet, fordi MP3'en ikke oprindeligt var tænkt som en lydfil, men som lag III i en MPEG 1 eller 2 videofil.


## M4P filformatspecifikationer

I lighed med [M4A](/audio/m4a/) består M4P-filerne også af på hinanden følgende bidder. Hver chunk har 8 byte header og underinddelt som:
- 4-byte chunk størrelse (big-endian, høj byte først)
- 4-byte chunk type - en af foruddefinerede signaturer: mdat, moov, pnot, moof, udta, uuid, free, skip, ftyp, jP2, wide, load, imap, matt, chap, kmat, clip, crgn, sync, tmcd, PICT, scpt , ctab, ssrc.

Similar to M4A the First chunk in M4P will be of type "ftype" and has a sub-type at offset 8. M4P defineret af undertype, som skal være M4P_.

Gentager bidder, indtil bidder af ukendt type er fundet, vil den komponere M4P (MPEG-4 Audio) fil.

## Referencer ##

* [MPEG-4 del 14 - af Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Eksempel](https://www.file-recovery.com/m4a-signature-format.htm)


