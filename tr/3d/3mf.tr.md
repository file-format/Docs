{
  "date" : "2019-12-09",
  "keywords" :[ "3mf dosyası", "3mf dosya biçimi", "3mf dosyası nedir", "dosya", "3mf örneği", "3mf dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"3MF dosya formatı ve 3MF dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## 3MF dosyası nedir?

3MF, 3B Üretim Formatı, uygulamalar tarafından 3B nesne modellerini çeşitli başka uygulamalara, platformlara, hizmetlere ve yazıcılara dönüştürmek için kullanılır. 3B yazıcıların en son sürümleriyle çalışmak için [STL](/tr/cad/stl/) gibi diğer 3B dosya biçimlerindeki sınırlamaları ve sorunları ortadan kaldırmak için oluşturulmuştur. 3MF, 3MF konsorsiyumu tarafından geliştirilen ve yayınlanan nispeten yeni bir dosya biçimidir. Bir modeli tam olarak tanımlayacak kadar zengindir, dahili bilgileri, rengi ve onu 3B baskıdaki yeni yenilikleri desteklemek için genişletilebilir kılan diğer özellikleri korur. Format genişletilebilir, geniş çapta benimsenebilir ve yaygın olarak kullanılan diğer dosya formatlarını geride bırakan sorunlar içermez.

## 3MF Dosya Formatının Kısa Tarihi

STL ve diğerleri gibi mevcut model tanımlayıcı dosya formatlarındaki mevcut sınırlamalar, önde gelen markaları bir araya getirmeye ve 3D baskı için daha genişletilebilir bir dosya formatı formüle etmeye yönlendiriyor. Önemli bir husus, uygulamaların model verilerini 3B yazıcılara nasıl iletmesi gerektiğiydi. Bu nedenle 3MF konsorsiyumu, 3D baskı ihtiyaçlarını karşılayacak kadar genişletilebilir hale getirmek amacıyla 3MF adlı yeni bir 3D dosya formatını desteklemek için ortaya çıktı. Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP ve diğerleri dahil olmak üzere birçok şirket bu konsorsiyumun parçasıydı. Microsoft, 3MF Konsorsiyumu'nun spesifikasyonun işbirlikçi geliştirmesi için başlangıç noktası olarak 3D dosya formatı geliştirme çalışmalarını bağışladı.

## 3MF Dosya Biçimi - Daha Fazla Bilgi

3MF, özel veriler için üçüncü taraf genişletilebilirliği de dahil olmak üzere 3B üretimle ilgili verilerin tanımlarını içeren, XML tabanlı bir veri biçimidir - insanlar tarafından okunabilir sıkıştırılmış XML. 3MF dosya formatı, diğer 3D dosya formatlarının karşılaştığı sınırlamalar ve sorunlar göz önünde bulundurularak tasarlanmıştır. Bu, 3MF dosya biçiminin formülasyonuna yol açar:

* **Tam:** Gerekli tüm model, malzeme ve özellik bilgilerini tek bir arşivde içerir
* **İnsan tarafından okunabilir:** Geliştirmeyi kolaylaştırmak için OPC, [ZIP](/tr/compression/zip/) ve XML gibi yaygın yapıları kullanma
* **Basit:** Geliştirmeyi kolaylaştıran ve doğrulamayı hızlandıran kısa, net bir belirtim
* **Genişletilebilir:** XML ad alanlarından yararlanmak, uyumluluğu korurken hem genel hem de özel uzantılara izin verir
* **Kesin:** Anlaşılır dil ve uygunluk testleri, bir dosyanın dijitalden fiziksele her zaman tutarlı olmasını sağlar
* **Ücretsiz:** 3MF spesifikasyonuna erişim ve uygulama, telif hakkı, patent ve lisanslamadan muaftır ve her zaman ücretsiz olacaktır.

3MF dosya biçimi belirtimleri, genel erişim ve sürekli güncellemeler için [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) üzerinde barındırılmaktadır. Mevcut yayınlanmış sürüm, bir veya daha fazla 3B modelin içeriğini ve görünümünü açıklamak için XML ve diğer yaygın olarak bulunan teknolojilerin kullanımına ilişkin kuralları açıklayan 1.2.3 sürümüdür. 3MF dosya biçimlerini işlemek için sistemler oluşturmak isteyen geliştiriciler, uygulama amacıyla bu spesifikasyonlara başvurabilir.

## 3MF Dosya Biçimi Özellikleri

3MF dosya biçimi, fiziksel modeli için ZIP arşivi biçimindeki Açık Paketleme özelliklerini kullanır. Belgedeki belirli bir amacı yerine getiren iyi tanımlanmış bir dizi parça ve ilişki içerir. Bu aynı zamanda formatın, dijital imzalar ve küçük resimler dahil olmak üzere paket özelliğini takip etmesini sağlar.

### 3MF Belgesi - Genel Bakış

Tipik bir 3MF belgesi aşağıdaki gibi görünür:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

Yük, 3B Model parçasını işlemek için gereken tüm parça setini içerir. 3B faydalı yükte açıklanan bir nesneyi üretmek için kullanılacak tüm içerik, 3MF Belgesinde BULUNMALIDIR ZORUNLU. Her bir belge bölümünün açıklaması, gerekli durumu veya seçeneği ile birlikte aşağıdaki tabloda verilmiştir.


|**Ad**|**Açıklama**|**İlişki Kaynağı**|**Gerekli/İsteğe bağlı**
--- | --- | --- | ---
|3B Model|Üretim için bir veya daha fazla 3B nesnenin açıklamasını içerir.|Paket|GEREKLİ
|Çekirdek Özellikler|Çeşitli belge özelliklerini içeren OPC bölümü.|Paket|İSTEĞE BAĞLI
|Dijital İmza Kaynağı|Paketteki dijital imzaların kökü olan OPC kısmı.|Paket|İSTEĞE BAĞLI
|Dijital İmza|Her biri dijital imza içeren OPC parçaları.|Dijital İmza Kaynağı|İSTEĞE BAĞLI
|Dijital İmza Sertifikası|Dijital imza sertifikası içeren OPC parçaları.|Dijital İmza|İSTEĞE BAĞLI
|PrintTicket|3D Model bölümündeki 3D nesne(ler)in çıktısı alınırken kullanılacak ayarları sağlar.|3D Model|İSTEĞE BAĞLI
|Küçük Resim|Paketteki 3B nesneleri veya paketin tamamını temsil eden küçük bir JPEG veya PNG görüntüsü içerir.|Paket|İSTEĞE BAĞLI
|3B Doku|3B Model bölümündeki bir 3B nesneye renk uygulamak için kullanılan bir doku içerir (uzantılarla kullanılabilir)|3B Model|İSTEĞE BAĞLI
|Özel Parçalar|Meta verilerle ilişkili OPC parçaları|Paket|İSTEĞE BAĞLI

[Parçalar ve İlişkiler](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3B Modeller](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Nesne Kaynakları](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) ve [Paket Özellikleri](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) spesifikasyon bölümleri belgesi 3MF belgesi hakkında ayrıntılı bilgi verir.

## Referanslar ##

* [3MF Dosya Biçimi Özellikleri](https://github.com/3MFConsortium/spec_core)
* [3MF - Wikipedia'dan](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

