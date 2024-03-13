{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR3 Fayl Format - Canon Raw 3 Şəkil Faylı",
  "description":"CR3 faylları yarada və aça bilən CR3 fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3-az",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## CR3 faylı nədir?

CR3 faylı seçilmiş Canon rəqəmsal kameraları tərəfindən yaradılmış Canon RAW şəkil fayl formatıdır. O, CR2 fayl formatını əvəz etmək üçün Canon tərəfindən təqdim edilib və bəzi Canon rəqəmsal cihazları tərəfindən istifadə olunur. CR3 faylları kamera tərəfindən çəkilmiş orijinal emal olunmamış itkisiz görüntü məlumatlarını saxlayır. Bu xam şəkillərin istifadəsi yüksək keyfiyyətli şəkillər təqdim edir və fotoqraflara redaktə etmək üçün çox yer verir. Əsas şəkil məlumatlarına əlavə olaraq, CR3 faylları təsvir haqqında metadata məlumatlarını da saxlayır.

## CR3 Fayl Formatı

CR3 faylları ikili fayl kimi diskdə ISO Əsas Media Fayl Formatında (ISO/IEC 14496-12) saxlanılır və həmçinin xüsusi [Canon tags](https://exiftool.org/TagNames/Canon.html#uuid) daxildir. Buraya həmçinin JPEG-LS (Rice-Golomb + RLE kodlaşdırma) və JPEG-2000 (LeGall 5/3 DWT + kəmiyyət) qarışığı olan [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) daxildir.

## CR3 Xüsusi Teqlər

CR3 fayllarında müxtəlif məqsədlər üçün xüsusi etiketlər var. Bu etiketlərdən bəziləri aşağıdakı kimidir.

|Tag ID| Etiket Adı| Yazıla bilən |Dəyərlər / Qeydlər|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP Teqləri|
|'CMT1' |IFD0| - |--> EXIF Teqləri|
|'CMT2' |ExifIFD| - |--> EXIF Teqləri|
|'CMT3' |MakerNoteCanon| - |--> Canon Teqləri|
|'CMT4' |GPSInfo| - |--> GPS Teqləri|
|'CNCV' |CompressorVersion| yox| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP Teqləri|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Teqləri|
|'THMB' |ThumbnailImage| yox| |

## İstinadlar

 * [CR2 Fayl Format](http://lclevy.free.fr/cr2/)
 * [Canon teqləri](https://exiftool.org/TagNames/Canon.html#uuid)

