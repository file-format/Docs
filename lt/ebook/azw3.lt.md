{
  "date": "2019-12-12",
  "keywords": [
"KF8",
"pratęsimas",
"failą",
"formatu",
"eBook",
"Kindle failo formatas",
"AZW3 failo struktūra"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie AZW3 failo formatą ir API, kurios gali kurti ir atidaryti AZW3 failus.",
  "title": "Kas yra AZW3 failas?",
  "linktitle": "AZW3",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-azw-lt3"
}
},
  "lastmod": "2021-06-04"
}

## Kas yra AZW3 failas?

AZW3, dar žinomas kaip Kindle Format 8 (**KF8**), yra modifikuota [AZW](/ebook/azw/) el. knygų skaitmeninio failo formato versija, sukurta Amazon Kindle įrenginiams. Formatas yra senesnių AZW failų patobulinimas ir naudojamas Kindle Fire įrenginiuose tik su atgaliniu suderinamumu su pirminio failo formatu, ty [MOBI](/ebook/mobi/) ir AZW. Amazon po KF8 pristatė KFX (KF versija 10) formatą, kuris naudojamas naujausiuose Kindle įrenginiuose. AZW3 failai turi internetinės medijos tipo application/vnd.amazon.mobi8-ebook. AZW3 failus galima konvertuoti į daugybę kitų failų formatų, pvz., [PDF](/pdf/), [EPUB](/ebook/epub/), [AZW](/ebook/azw/), [DOCX](/word-processing/docx/) ir [RTF](/word-processing/rtf/).

## AZ3/KF8 failo formatas ##

KF8 failai yra dvejetainio pobūdžio ir išlaiko MOBI failo formato struktūrą kaip PDB failą. Kaip minėta anksčiau, KF8 failą gali sudaryti ir MOBI, ir vėliau naujesnė KF8 EPUB versija. Vidinę formato informaciją iššifravo [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), kuris yra Python scenarijus, kuris analizuoja galutinę sudarytą duomenų bazę ir iš jos ištraukia MOBI arba AZW šaltinio failus. AZW3 (KF8) failai taikomi EPUB3 versijai su atgaliniu suderinamumu su EPUB. KF8 sukompiliuoja EPUB failus ir generuoja dvejetainę struktūrą pagal PDB failo formatą.

## Nuorodos Nr.

* [KF8 – Vikipedija](https://en.wikipedia.org/wiki/Kindle_File_Format)

* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)


