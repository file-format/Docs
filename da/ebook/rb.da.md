{
  "date": "2021-03-08",
  "keywords": [
"RB",
"Nuvo Medias Rocket eBook-enhed",
"fil",
"udvidelse",
"format",
"e-bog"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om RB-filformat til Nuvo Medias Rocket eBook-enhed og API'er, der kan oprette og åbne RB-filer.",
  "title": "RB - Rocket eBook File",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-r-dab"
}
},
  "lastmod": "2021-03-08"
}

## Hvad er en RB fil?

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. Selvom Rocket eBook er i stand til at vise billeder, men kun i sort/hvid visning. Den har en skærm på 106 dpi eller 480 x 320 pixels på en 4,5 x 3-tommer touchskærm. Rocket eBook forbindes til en computer via en seriel portforbindelse for at downloade eBooks i RB-filformat. RB-filerne er i stand til at bruge DRM, men denne teknologi bruges ikke i moderne e-bøger. RB-filen indeholder traditionelt en HTML-fil med billederne og en pseudo-OPF-fil med alle metadataene (.info).

## Teknisk specifikation for RB-filformat ##

Et magisk tal (i hex) vises i filens første 4 bytes: B0 0C B0 0C.

Det ser ud til, at de næste to bytes er et versionsnummer, som 02 00, som står for major version 2 og mindre version 0.

De næste fire bytes indeholder teksten NUVO, efterfulgt af 4 bytes af 00h.

The next 4-byte is the date when the book was created, encoded as an int16. Dette sætter os på offset 0Eh. ORocketLibrarys gamle version kodede årets fulde værdi (dvs. 1999 var CF 07, 2000 var D0 07). I den seneste version er tm_year gemt ordret, dvs. 100 for år 2000 (64 00). Efter året kommer en int8, der repræsenterer det 1-relative månedstal, og en int8, der repræsenterer dagen i måneden.

De næste 6 bytes er 00h. Til tidsindstilling kan disse reserveres.

Den absolutte offset af Indholdsfortegnelsen er indeholdt i en int32 ved offset 18h.

Efter dette er en int32, der indeholder længden af .rb-filen. Dette bruges til at afgøre, om filerne er komplette eller ej.

Hele denne del af bytes (20 timer til 128 timer) ser ud til kun at være nødvendige for en titel, der er krypteret. I ikke-krypterede titler er de altid nul.

I de fleste tilfælde følger indholdsfortegnelsen (ved offset 128). Det begynder med en int32-tælling af antallet af side-indgange (.rb-filsektioner) i ToC'en. Hver post består af et navn (nulpolstret til 32 bytes), efterfulgt af 3 int32s: længden af datasegmentet, positionen i .rb-filen og et flag for denne post. Fra i dag er de kendte værdier: 1 (krypteret), 2 (informationsside) og 8 (deflateret). Navnene er alle skræddersyet efter behov for at sikre, at de alle er unikke.

## Referencer

* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)


