{
  "date" : "2019-12-13",
  "keywords" :["AAC", "dosya", "uzantı", "biçim", "Ses Kodlama", "MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"AAC dosya formatı ve AAC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"AAC - Gelişmiş Ses Kodlama Dosyası",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## AAC dosyası nedir?

AAC (Gelişmiş Ses Kodlaması), kayıplı ses sıkıştırmasına dayalı ses dosyalarını temsil eden dijital ses kodlama standardını ifade eder. **[MP3](/tr/audio/mp3/)** dosya biçiminin halefi olarak, veri sıkıştırma yöntemlerinin geliştirilmesine dayalı olarak kodlama sürecinde yeni fikirlerin uygulanmasında yanal olarak karşılaşılan sorunlar göz önünde bulundurularak piyasaya sürüldü. AAC, aynı bit hızında MP3'e kıyasla daha iyi ses kalitesi sağlar. MPEG-2 Bölüm 7'de (ISO/IEC 13818-7) ve güncellenmiş biçimde MPEG-4 Bölüm 3'te (ISO/IEC 14496-3) tanımlanmıştır.

AAC formatı, YouTube, iPhone, iPod, iPad, Apple iTunes ve diğer birçok platform tarafından varsayılan medya formatı olarak kabul edildi. AAC dosya formatının MP3, WMA, M4A, **[WAV](/tr/audio/wav/)** ve diğerleri gibi diğer formatlara dönüştürülmesi için çeşitli uygulamalar ve API'ler mevcuttur.

### AAC Dosyasının Kısa Tarihi

AAC dosya formatı, bazı iyileştirmelerle MP3'ün geliştirilmiş bir versiyonudur. Fraunhofer Enstitüsü (Fraunhofer IIS - MP3 geliştiricileri), Nokia, Dolby, AT&T ve Sony dahil olmak üzere birçok şirketin katkısıyla, format, Nisan 1997'de Hareketli Resim Uzmanları Grubu (MPEG) tarafından uluslararası bir standart olarak ilan edildi. Daha sonra 1999'da, MPEG-2 Part 7 güncellendi ve MPEG-4 standart ailesine dahil edildi. ISO/IEC 14496-3: 1999 veya MPEG-4 Audio olarak tanımlanan MPEG-4 Bölüm 3 olarak biliniyordu.

## AAC Dosya Biçimi Özellikleri

AAC dosya formatı belirtimleri, MP3'ün sağladığından daha fazla codec bileşeni tasarlama esnekliği sağlar, bu da daha fazla eşzamanlı kodlama stratejisi ve verimli sıkıştırma ile sonuçlanır. Biçim, daha düşük bit hızlarında bile daha fazla seçenek için destek sağlama açısından MP3'e göre iyileştirmeleri nedeniyle bir dizi donanım platformunun tercihi olmuştur. AAC dosya biçimi belirtimleri [MPEG-2 Bölüm 7](https://www.iso.org/standard/43345.html) ve [MPEG-4 Bölüm 3](https://www.iso.org) olarak mevcuttur. /standart/53943.html) (indirmek ücretsiz değildir). Biçim, aşağıdaki ortam türlerini kullanır:

* ses/aac
* ses/aacp
* ses/3gpp
* ses/3gpp2
* ses/mp4
* ses/mp4a-latm
* ses/mpeg4-jenerik

## AAC ve MP3 - İyileştirmeler ##

İyileştirmeler açısından AAC ve MP3 arasındaki temel farklar aşağıdaki gibidir:

* AAC, daha geniş bir kanal aralığını (48'e kadar) ve örnekleme oranlarını (8 kHz'den 96 kHz'e) destekler
* AAC, 16 kHz'in üzerinde daha iyi kodlama frekanslarına sahiptir
* AAC, ses sinyalinin geçici ve sabit bölümlerinin daha iyi kodlanmasına yol açan bir filtre bankasının frekans-zaman çözünürlüğünde daha geniş varyasyon sınırlarına sahiptir.
* Daha verimli ve basit filtre bankası: Hibrit filtre bankası standart MDCT (değiştirilmiş ayrık kosinüs dönüşümü) ile değiştirildi
* Geçici Gürültü Şekillendirme (TNS), MDCT-zamanının tahmin katsayıları (uzun vadeli tahmin), parametrik stereo, algısal gürültü ikamesi, spektral bant replikasyonu (SBR) kullanılarak geliştirilmiş sıkıştırma etkinliğini destekler.
* daha esnek birleşik stereo (farklı frekans aralıklarında farklı yöntemler kullanılabilir);

## Referanslar ##

* [AAC - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)

