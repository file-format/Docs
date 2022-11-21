{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3 Dosya Biçimi - Canon Raw 3 Görüntü Dosyası",
  "description":"CR3 dosya formatı ve CR3 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## CR3 dosyası nedir?

CR3 dosyası, belirli Canon dijital fotoğraf makineleri tarafından oluşturulan bir Canon RAW görüntü dosyası biçimidir. CR2 dosya formatının yerini alması için Canon tarafından tanıtıldı ve bazı Canon dijital cihazları tarafından kullanılıyor. CR3 dosyaları, kamera tarafından yakalanan orijinal, işlenmemiş, kayıpsız görüntü verilerini depolar. Bu ham görüntülerin kullanılması, yüksek kaliteli görüntüler sağlar ve fotoğrafçılara düzenleme için bolca alan sağlar. CR3 dosyaları, ana görüntü verilerine ek olarak, görüntüyle ilgili meta veri bilgilerini de saklar.

## CR3 Dosya Biçimi

CR3 dosyaları, ISO Temel Ortam Dosyası Biçiminde (ISO/IEC 14496-12) diskte ikili dosya olarak depolanır ve ayrıca özel [Canon etiketleri](https://exiftool.org/TagNames/Canon.html#uuid) içerir. Ayrıca JPEG-LS'nin (Rice-Golomb + RLE) bir karışımı olan [Canon 'crx' codec bileşenini](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) içerir. kodlama) ve JPEG-2000 (LeGall 5/3 DWT + kantifikasyon).

## CR3 Özel Etiketleri

CR3 dosyaları, farklı amaçlar için özel etiketler içerir. Bu etiketlerin bazıları aşağıdaki gibidir.

|Etiket Kimliği| Etiket Adı| Yazılabilir |Değerler / Notlar|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP Etiketleri|
|'CMT1' |IFD0| - |--> EXIF Etiketleri|
|'CMT2' |ExifIFD| - |--> EXIF Etiketleri|
|'CMT3' |MakerNoteCanon| - |--> Canon Etiketleri|
|'CMT4' |GPSBilgisi| - |--> GPS Etiketleri|
|'CNCV' |Kompresör Sürümü| hayır| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP Etiketleri|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Etiketleri|
|'THMB' |Küçük Resim| hayır| |

## Referanslar

* [CR2 Dosya Biçimi](http://lclevy.free.fr/cr2/)
* [Canon etiketleri](https://exiftool.org/TagNames/Canon.html#uuid)

