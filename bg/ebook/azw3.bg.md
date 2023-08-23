{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "разширение", "файл", "формат", "електронна книга", "Kindle файлов формат", "AZW3 файлова структура" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за файловия формат AZW3 и API, които могат да създават и отварят AZW3 файлове.",
  "title" :"Какво е AZW3 файл?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Какво е AZW3 файл?

AZW3, известен също като Kindle Format 8 (**KF8**), е модифицираната версия на [AZW](/bg/ebook/azw/) цифровия файлов формат за електронни книги, разработен за устройства Amazon Kindle. Форматът е подобрение на по-стари AZW файлове и се използва на устройства Kindle Fire само с обратна съвместимост за файловия формат на предшественика, т.е. [MOBI](/bg/ebook/mobi/) и AZW. Amazon представи KFX (KF версия 10) формат след KF8, който се използва на най-новите устройства Kindle. Файловете AZW3 имат тип интернет медия application/vnd.amazon.mobi8-ebook. AZW3 файловете могат да бъдат конвертирани в редица други файлови формати като [PDF](/bg/pdf/), [EPUB](/bg/ebook/epub/), [AZW](/bg/ebook/azw/), [DOCX](/bg/ текстообработка/docx/) и [RTF](/bg/word-processing/rtf/).

## AZ3/KF8 файлов формат ##

KF8 файловете са двоични по природа и запазват структурата на MOBI файлов формат като PDB файл. Както споменахме по-рано, KF8 файл може да се състои както от MOBI, така и от по-нова KF8 версия на EPUB по-късно. Вътрешните подробности за формата са декодирани от [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), който е скрипт на Python, който анализира окончателно компилираната база данни и извлича MOBI или AZW изходни файлове от нея. Файловете AZW3 (KF8) са насочени към версия EPUB3 с обратна съвместимост и за EPUB. KF8 компилира EPUB файловете и генерира двоична структура въз основа на файловия формат PDB.

## Препратки ##

* [KF8 – от Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

