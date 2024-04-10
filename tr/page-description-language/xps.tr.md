{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "XML Kağıt Özellikleri", "Dosya", "Uzantı", "Dosya Biçimi", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Sayfa Düzeni Dosya Biçimi",
  "description":"XPS dosya formatı ve XPS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## XPS dosyası nedir? ##

Bir XPS dosyası, Microsoft tarafından oluşturulan XML Kağıt Belirtimlerini temel alan sayfa düzeni dosyalarını temsil eder. EMF dosya formatının yerine geliştirilmiştir ve [PDF](/tr/pdf/) dosya formatına benzer, ancak bir belgenin düzeninde, görünümünde ve yazdırma bilgilerinde XML kullanır. Aslında, XPS'nin PDF üzerinde bir deneme olduğunu söylemek daha doğru olur, ancak birçok nedenden dolayı PDF'nin sahip olduğu kadar popülerlik kazanamadı. Microsoft, XPS dosyalarının oluşturulması için Windows 7'den itibaren varsayılan olarak XPS Belge Yazıcısı sağlar. Belge yazdırılırken yazıcı olarak "Microsoft XPS Document Writer" seçilerek XPS dosyaları oluşturulabilir.

XPS görüntüleyiciler, Windows Vista, Windows 7, Windows 8 ve Internet Explorer 6 veya sonraki sürümlerinin bir parçası olarak tümleşik olarak gelir. XPS dosyaları oluşturulduktan sonra salt okunur hale gelir. Bu, kullanıcının, belgenin orijinalliği için XPS olarak gönderilen alınan belgelere olan güvenini artırır. Bir XPS belgesi, orijinal belgeden dönüştürüldüğü şekliyle bir veya daha fazla sayfa içerebilir.

## Kısa Tarih ##

Microsoft, XPS spesifikasyonunu Ecma International'a gönderdi. Haziran 2007'de Ecma Teknik Komitesi 46 (TC46), OpenXPS Kağıt Spesifikasyonlarına dayalı bir standart geliştirmek için kuruldu. Ecma International, Ecma Standardını (ECMA-388) [XPS spesifikasyonlarını](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) Haziran 2009'da 97. Genel Kurul'da onayladı.

## XPS Dosya Biçimi ##

XPS formatı, bir belgenin bileşimini ve her sayfanın görsel görünümünü tanımlayan XML işaretlemesinin yanı sıra belgeyi görüntülemek veya yazdırmak için işleme kurallarından oluşur. Herhangi bir sistemde bir belgeyi yeniden oluşturmak için tüm bilgileri tutar, bu da onu o sistemdeki mevcut kaynaklardan bağımsız kılar. Biçim esas olarak bir ZIP arşividir ve dosya uzantısını ZIP olarak yeniden adlandırırsanız, belge verilerini içeren kurucu dosyaları görürsünüz. Bu belgeler şunları içerir:

* belge sayfası dosyaları (.fpage) - Belge içeriğini ve belge biçimi ayarlarını içerir. XPS belgesindeki her sayfanın bir FPAGE dosyası vardır.
* belge ayarları dosyası (.fdoc) - XPS arşivindeki ayarları saklar.
* belge parça dosyaları (.frag) - Gerçek XPS dosyası için ayarları tanımlar ve belgedeki her sayfanın kendi .frag dosyası vardır.

{{< figure src="../XPS-1.png" alt="XPS Dosya Biçimi" >}}

Bu dosyalar, belge içeriğini öyle bir şekilde korurlar ki, örneğin, birinin makinesinde aynı yazı tipleri yüklü değilse, XPS görüntüleyici bu orijinal yazı tiplerini işlemeye devam eder. Bu, her biri için XML biçimlendirme dosyasının eklenmesi anlamına gelir:

* Sayfa
* Metin
* Gömülü yazı tipleri
* Raster görüntüler
* 2B vektör grafikleri
* Dijital haklar yönetimi

XPS Belge formatı, her biri belgede belirli bir amacı yerine getiren, iyi tanımlanmış bir dizi parça ve ilişki içerir. Biçim aynı zamanda dijital imzalar, küçük resimler ve serpiştirme gibi paket özelliklerini de genişletir.

Tipik bir XPS belgesi aşağıdaki gibi görünür ve XPS dosya formatı özellikler ışığında analiz edilebilir.

{{< figure src="../XPS-2.png" alt="XPS Dosya Biçimi" >}}


## Referanslar ##

* [XPS Dosya Biçimi Özellikleri](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

