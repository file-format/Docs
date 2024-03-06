{
  "date": "2019-12-12",
  "keywords": [
"KF8",
"pagarinājumu",
"failu",
"formātā",
"e-grāmata",
"Kindle faila formāts",
"AZW3 faila struktūra"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par AZW3 faila formātu un API, kas var izveidot un atvērt AZW3 failus.",
  "title": "Kas ir AZW3 fails?",
  "linktitle": "AZW3",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-azw-lv3"
}
},
  "lastmod": "2021-06-04"
}

## Kas ir AZW3 fails?

AZW3, kas pazīstams arī kā Kindle Format 8 (**KF8**), ir modificēta [AZW](/ebook/azw/) e-grāmatu digitālā faila formāta versija, kas izstrādāta Amazon Kindle ierīcēm. Formāts ir vecāku AZW failu uzlabojums un tiek izmantots Kindle Fire ierīcēs tikai ar atpakaļejošu saderību ar priekšteča faila formātu, piemēram, [MOBI](/ebook/mobi/) un AZW. Amazon ieviesa KFX (KF versija 10) formātu pēc KF8, kas tiek izmantots jaunākajās Kindle ierīcēs. AZW3 failiem ir interneta multivides tipa aplikācija/vnd.amazon.mobi8-ebook. AZW3 failus var konvertēt uz vairākiem citiem failu formātiem, piemēram, [PDF](/pdf/), [EPUB](/ebook/epub/), [AZW](/ebook/azw/), [DOCX](/word-processing/docx/) un [RTF](/word-processing/rtf/).

## AZ3/KF8 faila formāts ##

KF8 faili ir bināri, un tie saglabā MOBI faila formāta struktūru kā PDB failu. Kā minēts iepriekš, KF8 fails var sastāvēt gan no MOBI, gan no jaunākas EPUB KF8 versijas. Formāta iekšējās detaļas ir atkodētas, izmantojot [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), kas ir Python skripts, kas parsē galīgo apkopoto datu bāzi un izvelk no tās MOBI vai AZW avota failus. AZW3 (KF8) failu mērķauditorija ir EPUB3 versija ar atpakaļejošu saderību arī ar EPUB. KF8 apkopo EPUB failus un ģenerē bināro struktūru, pamatojoties uz PDB faila formātu.

## Atsauces Nr.

* [KF8 — Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)

* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)


