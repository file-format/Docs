{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файлов формат CR3 – файл с изображение на Canon Raw 3",
  "description":"Научете за файловия формат CR3 и API, които могат да създават и отварят CR3 файлове.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Какво е CR3 файл?

CR3 файл е RAW файлов формат на Canon, създаден от избрани цифрови фотоапарати на Canon. Въведен е от Canon, за да замени файловия формат CR2 и се използва от някои цифрови устройства на Canon. CR3 файловете съхраняват оригиналните необработени данни за изображения без загуби, заснети от камерата. Използването на тези необработени изображения осигурява висококачествени изображения и предоставя много място за редактиране на фотографите. В допълнение към основните данни за изображението, CR3 файловете също съхраняват информация за метаданни за изображението.

## CR3 файлов формат

CR3 файловете се съхраняват на диск като двоичен файл в ISO Base Media File Format (ISO/IEC 14496-12) и също така включва персонализирани [маркери на Canon](https://exiftool.org/TagNames/Canon.html#uuid). Той също така включва [Canon 'crx' кодека](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), който е смес от JPEG-LS (Rice-Golomb + RLE кодиране) и JPEG-2000 (LeGall 5/3 DWT + количествено определяне).

## CR3 персонализирани етикети

CR3 файловете съдържат персонализирани тагове за различни цели. Някои от тези тагове са както следва.

|ID на етикет| Име на етикет| Записваеми |Стойности / Бележки|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP етикети|
|'CMT1' |IFD0| - |--> EXIF етикети|
|'CMT2' |ExifIFD| - |--> EXIF етикети|
|'CMT3' |MakerNoteCanon| - |--> Етикети на Canon|
|'CMT4' |GPSInfo| - |--> GPS етикети|
|'CNCV' |CompressorVersion| не| |
|'CNOP' |CanonCNOP| - |--> Етикети Canon CNOP|
|'CNTH' |CanonCNTH| - |--> Етикети Canon CNTH|
|'THMB' |Миниатюра| не| |

## Препратки

* [CR2 файлов формат](http://lclevy.free.fr/cr2/)
* [Етикети на Canon](https://exiftool.org/TagNames/Canon.html#uuid)

