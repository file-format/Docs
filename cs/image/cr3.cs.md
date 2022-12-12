{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru CR3 – obrazový soubor Canon Raw 3",
  "description":"Další informace o formátu souboru CR3 a rozhraních API, která mohou vytvářet a otevírat soubory CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Co je soubor CR3?

Soubor CR3 je formát obrázkového souboru Canon RAW, který je vytvořen vybranými digitálními fotoaparáty Canon. Byl představen společností Canon, aby nahradil formát souboru CR2 a používají jej některá digitální zařízení Canon. Soubory CR3 ukládají původní nezpracovaná bezztrátová obrazová data zachycená fotoaparátem. Použití těchto nezpracovaných snímků poskytuje vysoce kvalitní snímky a poskytuje fotografům dostatek prostoru pro úpravy. Kromě hlavních obrazových dat ukládají soubory CR3 také metadata o obrazu.

## Formát souboru CR3

Soubory CR3 se ukládají na disk jako binární soubor ve formátu ISO Base Media File Format (ISO/IEC 14496-12) a zahrnují také vlastní [značky Canon] (https://exiftool.org/TagNames/Canon.html#uuid). Zahrnuje také [Canon 'crx' kodek](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), což je mix JPEG-LS (Rice-Golomb + RLE kódování) a JPEG-2000 (LeGall 5/3 DWT + kvantifikace).

## Vlastní štítky CR3

Soubory CR3 obsahují vlastní značky pro různé účely. Některé z těchto značek jsou následující.

|ID značky| Název značky| Zapisovatelné |Hodnoty/Poznámky|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP Tagy|
|'CMT1' |IFD0| - |--> EXIF Tagy|
|'CMT2' |ExifIFD| - |--> EXIF Tagy|
|'CMT3' |MakerNoteCanon| - |--> Štítky Canon|
|'CMT4' |GPSinfo| - |--> GPS tagy|
|'CNCV' |Verze kompresoru| ne| |
|'CNOP' |CanonCNOP| - |--> Štítky Canon CNOP|
|'CNTH' |CanonCNTH| - |--> Štítky Canon CNTH|
|'THMB' |ThumbnailImage| ne| |

## Reference

* [Formát souboru CR2](http://lclevy.free.fr/cr2/)
* [Značky Canon](https://exiftool.org/TagNames/Canon.html#uuid)

