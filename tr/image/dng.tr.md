{
  "date" : "2019-10-11",
  "keywords" :[ "dng dosyası", "dng dosya biçimi", "dng dosyası nedir", "dosya", "dng örneği", "dng dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Dijital Kamera Görüntü Dosyası Formatı",
  "description":"DNG dosya formatı ve DNG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## DNG dosyası nedir?

DNG, ham dosyaların depolanması için kullanılan bir dijital kamera görüntü formatıdır. Eylül 2004'te Adobe tarafından geliştirilmiştir. Temel olarak dijital fotoğrafçılık için geliştirilmiştir. DNG, [TIFF](/tr/image/tiff/)/EP standart biçiminin bir uzantısıdır ve önemli ölçüde meta verileri kullanır. Fotoğrafçılar, dijital kameralardan gelen ham verileri esneklik ve sanatsal kontrol kolaylığıyla işlemek için camera raw dosyalarını tercih ediyor. JPEG ve TIFF formatları, kamera tarafından işlenen görüntüleri saklar, bu nedenle, bu tür formatlarda değişiklik için fazla yer yoktur.

## DNG Dosya Biçiminin Tarihçesi ve Sürümleri

Şimdiye kadar DNG spesifikasyonunun 5 versiyonu olmuştur. Sürüm 1.0.0.0, Eylül 2004'te "2.3" (ACR ve DNG Dönüştürücü) sürümüyle birlikte piyasaya sürüldü. Şubat 2005'te sürüm 1.1.0.0 yayınlandı. Mayıs 2008'de 1.2.0.0 sürümü yayınlandı ve "4.4"te kullanıldı. Sürüm 1.3.0.0, Haziran 2009'da yayınlandı. Sürüm 1.4.0.0, 2012'de çıktı.

## DNG Dosya Biçimi

Camera raw dosyaları ise işlenmemiş veya az işlenmiş verileri doğrudan sensörden yakalar. Film negatiflerine benzedikleri için camera raw formatları “Dijital Negatifler” olarak da bilinir. Ham formatların yararı, son kullanıcı için artan sanatsal kontroldür. Kullanıcı, beyaz dengesi, ton eşleme, gürültü azaltma, keskinleştirme vb. gereksinimlere göre çeşitli parametre aralıklarını ayarlayabilir. Öte yandan, camera raw dosyasının herhangi bir kullanım için herhangi bir yazılım veya bir dönüştürücü aracılığıyla işlenmesi gerekir.

Camera raw dosyaları için standart bir format bulunmadığından, son kullanıcı için birden çok sorun yarattı. Bu sorunlar Adobe tarafından ele alındı ve camera raw dosyaları için tescilli olmayan bir biçim tanımlandı. Biçim, Dijital Negatif veya DNG olarak bilinir. DNG, ham dosyaların işlenmesi için çok çeşitli donanım ve yazılımlar tarafından kullanılabilir. Ayrıca DNG, orijinal olarak kendi özel ham formatlarına sahip kameralar tarafından çekilen görüntüleri depolamak için bir ara format olarak da kullanılabilir.

### DNG Dosya Biçimi Özellikleri

Bu bölümde DNG formatını TIFF 6.0'ın bir uzantısı olarak açıklayacağız.

* **Dosya Uzantıları**: DNG, ".DNG" veya ".TIF" uzantılarını kullanır.
* **SubIFD Ağaçları**: DNG, SubIFD zincirlerini desteklemez, bunun yerine DNG, TIFF-EP spesifikasyonlarında belirtildiği gibi SubIFD ağaçlarının kullanılmasını önerir. En yüksek kalite ve çözünürlük NewSubFileType 0'ı kullanabilirken, düşük kaliteli küçük resimlerde 1'e eşit NewSubFileType kullanılmalıdır. İlk IFD'nin düşük kaliteli veya çözünürlüklü bir küçük resme sahip olması şart olmasa da önerilir.
* **Bayt Sırası**: Bayt sırası, belirli bir kamera modelindeki dosyalar için de DNG okuyucuları tarafından desteklenmelidir.
* **Maskelenmiş Pikseller**: Kamera sensörlerinin çoğu, siyah kodlama yoluyla sensörün kenarındaki tamamen maskelenmiş pikselleri hesaplar. Bu pikseller, görüntü DNG formatında saklanmadan önce dahil edilebilir veya kırpılabilir. Maskelenen pikseller kırpılmamışsa, bu piksellerin alanı ActiveArea etiketinde belirtilmelidir. Bu piksellerden siyah kodlama seviyesi hakkında toplanan bilgiler, ham veri depolanmadan önce kullanılmalıdır veya siyah seviyesini belirten DNG dosyasına dahil edilebilir.
* **Hatalı Pikseller**: Ham verileri DNG olarak kaydetmeden önce hatalı pikseller hariç tutulmalıdır.
* **Meta veriler**: Meta veriler, aşağıdaki yollardan herhangi biriyle DNG'ye dahil edilebilir:
** TIFF-EP veya EXIF meta veri etiketlerini kullanarak
** IPTC meta veri etiketi (33723) aracılığıyla
** XMP meta veri etiketini kullanma (700)
* **Tescilli Veri**: Normalde satıcılar, kendi dönüştürücüleri tarafından kullanılmak üzere ham dosyada özel verileri içerir. DNG, tescilli verilerini özel etiketlerde, özel IFD'lerde ve özel bir MakerNote'ta saklar. Satıcılar, DNG dosyalarını düzenleyen uygulamaların bu tescilli verileri koruduğundan emin olmak için DNGPrivateData ve MakerNoteSafety etiketlerini kullanmalıdır.

Aşağıda bazı önemli kısıtlamalar ve uzantılar TIFF etiketleri bulunmaktadır.

**Örnek Başına Bit**

8 ila 32 bit/örnek desteklenir. SamplesPerPixel 1'e eşit olmadığında her örnek için aynı derinlik olmalıdır. Ancak BitsPerSample 8 veya 16 veya 32'ye eşit değilse, bitler TIFF varsayılan FillOrder 1 (big-endian) kullanılarak baytlara paketlenmelidir.

**Sıkıştırma**

İki Sıkıştırma etiketi değeri desteklenir:

* Değer # 1: Sıkıştırılmamış veri.
* Değer # 7: JPEG sıkıştırılmış veri, temel DCT JPEG veya kayıpsız JPEG sıkıştırma.

**Fotometrik Yorum**

Aşağıdaki değerler yalnızca küçük resim ve önizleme IFD'leri için desteklenir:

* 1 = BlackIsZero. Gama 2.2 renk uzayında olduğu varsayılmıştır.
* 2 = RGB. sRGB renk uzayında olduğu varsayılmıştır.
* 6 = YCbCr. JPEG kodlu ön izleme görüntüleri için kullanılır.

Aşağıdaki değerler ham IFD için desteklenir ve kameranın yerel renk alanı olduğu varsayılır:

* 32803 # CFA (Renk Filtresi Dizisi).
* 34892 # LinearRaw.

**Oryantasyon**

Oryantasyon etiketi, DNG dosyalarının kayıpsız dönüşünü gerçekleştirebilmeleri için dosya tarayıcıları için kullanılır. DNG okuyucuları, yansıtılmış yönler dahil olmak üzere tüm olası yönleri desteklemelidir.

## DNG'nin Son Sürümündeki Özellikler

DNG Sürüm 1.4 Ekim 2012, aşağıdaki gelişmiş özelliklere sahiptir.

* Varsayılan Kullanıcı Kırpma
* Şeffaflık
* Kayan Nokta (HDR)
* Kayıplı Sıkıştırma
* Proxy'ler

## Referanslar ##

* [DNG Spesifikasyonları - Adobe Tarafından](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [Dijital Negatif - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - Dijital kamera ham verileri için genel arşiv formatı](https://helpx.adobe.com/photoshop/digital-negative.html)

