{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "file", "extension", "format", "ses değişim dosyası formatı", "müzik", "aiff dosya formatı", "aiff'ten mp3'e", "aiff'e karşı wav", "aiff'i şuraya dönüştür: mp3"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"AIFF dosya formatı ve AIFF dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"AIFF - Ses Değişim Dosyası Biçimi",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## AIFF dosyası nedir?
AIFF (Ses Değişim Dosyası Formatı), Apple tarafından 1998'de geliştirilen sıkıştırılmamış bir ses dosyası formatıdır, ancak Amiga sistemlerinde kullanılan bir sarmalayıcı format olan **EA IFF 85**'e (Elektronik Sanatlar tarafından geliştirilen Değişim Formatı Dosyaları için Standart) dayanmaktadır. . Bu dosya formatı, örneklenmiş sesleri depolamak için bir standart sunar. Biçim, esneklik açısından yeterince iyidir ve çeşitli örnekleme hızlarında ve örnek genişliklerinde tek veya çok kanallı örneklenmiş seslerin depolanmasını sağlar. AIFF dosyaları sıkıştırılmamış olduğundan, bu durum onları [MP3](https://docs.fileformat.com/audio/mp3/) gibi diğer kayıplı formatlardan daha büyük yapar.

AIFF dosyaları, 44.1 khz'de kaydedilmiş, 16 bitlik örnek boyutuna sahip 2 kanal sıkıştırılmamış stereo sesten oluşur. Yüksek ses kalitesi nedeniyle, 5 dakikalık bir ses, [WAV](https://docs.fileformat.com/audio/wav/) dosya biçimine benzer şekilde 50 MB'a kadar disk alanı kaplayabilir.

## AIFF ve WAV

AIFF ve WAV, kalite açısından neredeyse aynıdır. Her ikisi de, [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Genel farklılıklardan bazıları aşağıdaki tabloda yazılmıştır:

|AIFF|WAV|
---|---|
|Çoğunlukla MAC için kullanılıyor|Çoğunlukla PC'ler için kullanılıyor|
|Meta veriye izin verir| Metadeta'ya izin vermiyor|

## AIFF Dosya Yapısı

**EA IFF 85**, verileri dosyalarda depolamak için genel bir yapı ortaya koyar. Bir **EA IFF 85** dosyası, bir dizi veri parçasından oluşur. AIFF dosyasının bir yapı bloğu, bazı başlık bilgilerinden ve ardından verilerden oluşur:
{{< figure src="../chunk.png" alt="AIFF Yığın" >}}

Bir AIFF dosyası, bir dizi farklı parça türünün bir koleksiyonudur. Bir AIFF dosya öbeği oluşturmak için önemli olan iki genel parça türü vardır:
- **Common Chunk**: Uzunluğu ve örnekleme hızı gibi örneklenen sesi açıklayan önemli parametreleri içerir.
- **Ses Veri Parçası**: Gerçek ses örneklerini içerir.
Cihaz parametrelerini listeleyen, işaretleyicileri tanımlayan, uygulamaya özgü bilgileri depolayan vb. birçok başka isteğe bağlı parça vardır.

### Yerel Öbek Türleri

AIFF oluşturmak için yığın türleri aşağıdaki tabloda verilmiştir:

|Yığın Türü| Açıklama|
---|---|
|Common Chunk|Common Chunk, örneklenen sesin temel parametrelerini açıklar|
|Ses Verisi Yığını|Ses Verisi Yığını gerçek örnek çerçeveleri içerir|
|Marker Chunk|Marker Chunk, ses verilerindeki konumlara işaret eden işaretler içerir|
|Enstrüman Parçası|Enstrüman Parçası, örnekleyici gibi bir enstrümanın ses verilerini çalmak için kullanabileceği temel parametreleri tanımlar|
|MIDI Veri Parçası|MIDI Veri Parçası, MIDI verilerini depolamak için kullanılabilir|
|Ses Kayıt Parçası|Ses Kayıt Parçası, ses kayıt cihazlarıyla ilgili bilgileri içerir|
|Uygulamaya Özel Öbek|Uygulamaya Özel Yığın, uygulama üreticileri tarafından herhangi bir amaç için kullanılabilir|
|Yorum Yığını|Yorum Yığını, AIFF FORMunda yorumları depolamak için kullanılır|
|Metin Yığınları - Ad, Yazar, Telif Hakkı, Ek Açıklama| Hepsi metin parçalarıdır |

## Referanslar ##

* [Ses Değişim Dosyası Formatı - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

