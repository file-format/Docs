{
  "date": "2019-12-12",
  "keywords": [
"CBC",
"udvidelse",
"fil",
"format",
"Tegneserier",
"Tegneserie-filformat",
"e-bog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om CBC-filformat og API'er, der kan oprette og åbne CBC-filer.",
  "title": "CBC - Comic Book Collection File Format",
  "linktitle": "CBC",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-cb-dac"
}
},
  "lastmod": "2021-03-03"
}

## Hvad er en CBC fil?

En fil med filtypen .cbc er en komprimeret samling af tegneseriefiler til e-bøger og indeholder [CBZ](/ebook/cbz/)- og [CBR](/ebook/cbr/)-filer. Det bruges af [Calibre](https://calibre-ebook.com/), en e-bogskonverteringsapplikation, som er en open source e-bogsmanager på tværs af platforme og lader dig administrere dine e-bøger og konvertere disse til forskellige formater. En CBC-fil indeholder en .txt-fil, comics.txt, der viser andre filer, som er en del af arkivet. Adskillige applikationer er tilgængelige online, der kan konvertere CBC-filer til [AZW3](/ebook/azw3/), [EPUB](/ebook/epub/), [FB2](/ebook/fb2/), [MOBI](/ebook/mobi/), [TXT](/word-processing/txt/), [PDF](/pdf/) og andre populære filformater.

## CBC filformat

CBC-filer er komprimerede arkiver, der indeholder CBZ, CBR og en tekstfil til at angive indholdet. Tekstfilen comics.txt er UTF8-kodet og indeholder en liste over de CBC-filer, der skal bruges af læsere til at organisere deres samlinger. En CBC-fil har normalt flere attributter, der tillader organiseringen af denne samling, såsom tegneserie, kategori, udgiver, serie, udgave og kunstner.

Indholdet af en CBC-eksempel-fil er angivet som følger:

 * comics.txt - Tekstfil, der indeholder en liste over CBR- og CBZ-filer
 * 1.cbz
 * 2.cbz
 * 3.cbz
 * CBZ fil(er)

hvor comics.txt-filen viser indholdet som følger:

 * 1.cbz: Første kapitel
 * 2.cbz: Andet kapitel
 * 3.cbz: Tredje kapitel

Læsere behandler comics.txt-filen og genererer indholdsfortegnelsen baseret på de angivne data.

## Referencer

* [Kaliber](https://calibre-ebook.com/)


