{
  "date" : "2021-02-15",
  "keywords" :[ "asf dosyası", "asf dosya formatı", "asf dosyası nedir", "dosya", "asf örneği", "asf dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Gelişmiş Sistemler Dosya Biçimi",
  "description":"ASF dosya formatı ve ASF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## ASF dosyası nedir?

.asf uzantılı bir dosya, ağ üzerinden dijital ortam akışlarını depolamak ve oynatmak için kullanılan bir multimedya dosya biçimidir. Çevrimiçi akış için hem video hem de ses içeriğine sahip olabilen bir kapsayıcı dosya biçimidir. ASF dosyalarını nadiren bulacaksınız ve daha büyük olasılıkla her ikisi de ASF dosyalarını belirten Windows Media Audio ([WMA](/tr/audio/wma/)) ve Windows Media Video ([WMV](/tr/video/wmv/)) dosyalarına rastlayacaksınız. ilgili kodeklerle kodlanmış içeriğe sahip olmak. Windows medya dosyaları, Windows Media Format SDK kullanılarak oluşturulabilir ve okunabilir.

## ASF Dosya Biçimi

Bir ASF dosyası, birden çok bağımsız veya bağımlı akış içerebilir. Bu, çok kanallı ses için birden çok ses akışını veya birden çok bit hızlı video akışını içerebilir. Çoklu bit hızları, akışları farklı bant genişlikleri üzerinden iletime uygun hale getirir. Ayrıca, bir ASF dosyasındaki akışlar sıkıştırılmış veya sıkıştırılmamış biçimde olabilir. En iyi sıkıştırma, Microsoft Windows Media Audio ve Video 9 Series codec bileşenleriyle sağlanır. ASF dosya formatının tüm özellikleri [Microsoft Web Sitesinde](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc) mevcuttur.

### ASF Üst Düzey Dosya Yapısı

ASF dosyaları mantıksal olarak üç tür üst düzey nesne içerir:

* `Başlık Nesnesi` - zorunludur ve her ASF dosyasının başına yerleştirilmelidir
* `Veri Nesnesi` - zorunludur ve başlık nesnesini takip etmelidir
* `Dizin Nesneleri` - isteğe bağlıdır, ancak ASF dosyalarına zamana dayalı rasgele erişim sağlamada kullanışlıdır

Aşağıdaki görüntü, ASF dosyalarının üst düzey dosya yapısını göstermektedir.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF Üst Düzey Başlık Nesnesi

Başlık nesnesi, ASF dosyalarının başında iyi bilinen bir bayt dizisi sağlar ve isteğe bağlı olarak bibliyografik bilgiler gibi meta veriler içerebilir. Veri nesnesindeki bilgileri doğru bir şekilde yorumlamak için gereken tüm bilgileri içerir. Başlık Nesnesi, aşağıdakiler dahil ancak bunlarla sınırlı olmamak üzere birkaç standart nesne içerebilir:

* Dosya Özellikleri Nesnesi - Genel dosya özniteliklerini içerir.
* Akış Özellikleri Nesnesi - Bir dijital ortam akışını ve özelliklerini tanımlar.
* Başlık Uzantısı Nesnesi - Geriye dönük uyumluluğu korurken bir ASF dosyasına ek işlevsellik eklenmesine izin verir.
* İçerik Açıklama Nesnesi - Bibliyografik bilgileri içerir.
* Komut Dosyası Komut Nesnesi - Oynatma zaman çizelgesinde yürütülebilen komutları içerir.
* Marker Object - Bir dosya içinde adlandırılmış atlama noktaları sağlar.

Başlık Nesnesi, aşağıdaki yapı kullanılarak temsil edilir:

|Alan adı |Alan türü |Boyut (bit)|
---|---|---|
|Nesne Kimliği| GUID| 128|
|Nesne Boyutu| QWORD| 64|
|Başlık Nesnelerinin Sayısı| DWORD| 32|
|Ayrıldı1| BAYT| 8|
|Ayrıldı2| BAYT| 8|

#### ASF Üst Düzey Veri Nesnesi

Bir ASF dosyası için tüm dijital ortam verileri, veri nesnesinde bulunur ve ASF veri paketleri biçiminde saklanır. Her veri paketi sabit uzunluktadır ve bir veya daha fazla dijital ortam akışı için veri içerir.

#### ASF Üst Düzey Dizin Nesneleri

ASF üst düzey dizin nesneleri aşağıdaki iki türe sahiptir:

* `Basit İndeks Nesnesi` - Bir ASF dosyasındaki video verilerinin zamana dayalı bir indeksini içerir. Dizin girişleri arasındaki zaman aralığı sabittir ve Basit Dizin Nesnesinde saklanır.
* `Dizin Nesnesi` - Biçimleri benzer olan Dizin Nesnesi, Medya Nesnesi Dizin Nesnesi ve Zaman Kodu Dizin Nesnesini ifade eder. Basit Dizin Nesnesi gibi, Dizin Nesnesi de sabit bir zaman aralığıyla zamana göre dizin oluşturur ancak video akışlarıyla sınırlı değildir.

## Referanslar

* [ASF Dosya Biçimi - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime Dosya Biçimi - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

