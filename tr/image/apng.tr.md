{
  "date" : "2019-10-11",
  "keywords" :[ "apng dosyası", "apng dosya biçimi", "apng dosyası nedir", "dosya", "apng örneği", "apng dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APNG Dosya Biçimi - Animasyonlu Taşınabilir Ağ Grafik Dosyası",
  "description":"APNG dosya formatı ve APNG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## APNG dosyası nedir?

.apng (Animated Portable Network Graphics) uzantılı bir dosya, raster bir grafik biçimidir ve Portable Network Graphic'in ([PNG](/tr/image/png/) ) resmi olmayan bir uzantısıdır. Bir animasyon dizisini temsil eden birden çok kareden (her biri PNG görüntüsünün) oluşur. Bu, bir [GIF](/tr/image/gif/) dosyasına benzer görselleştirme sağlar. APNG dosyaları, 24 bit görüntüleri ve 8 bit şeffaflığı destekler. APNG, animasyonlu olmayan GIF dosyalarıyla geriye dönük uyumludur. APNG dosyaları aynı .png uzantısını kullanır ve Mozilla Firefox, APNG destekli Chrome, iOS 10 için iMessage uygulamaları gibi uygulamalar tarafından açılabilir.

## Kısa Tarihçe

* APNG spesifikasyonları, animasyonlu PNG Resimlerine destek sağlamak için 2004 yılında oluşturulmuştur.
* APNG kod çözücüler, çok daha küçük boyutta ve PNG kod çözücünün arkası kullanılarak geliştirilmiştir.
* Sürekli görüşmelerden sonra, uzantı .apng yerine .png ile aynı tutularak yeni bir MIME türü image/apng formüle edildi.
* APNG, PNG resimlerine benzerliği ve aynı zamanda farklı özelliklere sahip olması nedeniyle PNG grubu tarafından 20 Nisan 2007'de resmi olarak reddedildi.

## APNG Dosya Biçimi

APNG dosyaları, diskte ikili dosyalar olarak saklanır ve animasyonlu görüntüler için genişletilmiş PNG özelliklerini kullanır. Bir APNG dosyasının ilk karesi, PNG kod çözücüleri tarafından görüntülenmek üzere okunabilen normal bir PNG akışıdır. APNG dosya formatı, PNG spesifikasyonlarına uygundur ve veriler, parça adı verilen bölümlerde depolanır. Ancak, APNG aşağıdaki yeni parçaları tanıttı:

`Animation Control Chunk (acTL)` - Bu dosyanın normal bir PNG dosyası değil, animasyonlu bir PNG dosyası olduğunu belirtir. Bir işaretleyici görevi görür ve IDAT öbeğinden önce gelir. Ayrıca, kare sayısını ve animasyonların döngüye alınma süreleri hakkında bilgi içerir.

"Çerçeve Kontrol Yığını" - Her birinin başlangıcında ve boyutlar, konum, saydamlık uygulaması gibi meta veri bilgileri ve bittiğinde önceki veya sonraki çerçeveye göre değiştirme bilgileri oluşur.

`Çerçeve Veri Parçası` - Çerçevenin içeriğini saklar ve bir sıra numarasıyla başlar. Bu sıra numarası, varsayılan görüntünün IDAT yığınıyla aynı yapıya sahiptir.

{{< figure src="../APNG.png" alt="Hareketli PNG - APNG Dosya Biçimi" >}}

APNG, PNG ile geriye dönük uyumludur, çünkü yanalın özellikleri, bir PNG dosyasını okuyan bir uygulamanın anlamadığı parçaları görmezden gelmesi gerektiği şekilde tasarlanmıştır. Bit derinliği, renk türü, sıkıştırma, filtreler, tarama yöntemleri ve palet bilgileri ile ilgili özellikler, varsayılan PNG formatıyla aynı şekilde kullanılır.

## APNG ve GIF

GIF hali hazırda mevcut ve uzun süredir kullanılıyorken, APNG'nin GIF'ten ne farkı olduğunu merak edebilirsiniz. Aşağıda, her iki dosya formatı hakkında kısa bir fikir veren APNG ve GIF arasında bir dizi karşılaştırma yer almaktadır.

||APNG|GIF|
---|---|---|
|Yayınlandı|2004|1987|
|Renk Derinliği|24 bit|8 bit|
|Kare Hızı|Sınırsız|saniyede 10 kare|
|Şeffaflık|Tam ve kısmi|Tam|
|Sıkıştırma|Çok İyi|İyi|

## Referanslar

* [APNG Dosya Biçimi](https://en.wikipedia.org/wiki/APNG)
* [Resmi PNG Biçim Özellikleri](https://www.w3.org/TR/PNG/)

