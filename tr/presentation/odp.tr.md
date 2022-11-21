{
  "date" : "2019-10-11",
  "keywords" :[ "odp dosyası", "odp dosya biçimi", "odp dosyası nedir", "dosya", "odp örneği", "odp dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - OpenOffice Sunum Dosyası Formatı",
  "description":"ODP dosya formatı ve ODP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## ODP dosyası nedir?

.odp uzantılı dosyalar, OASISOpen standardında OpenOffice.org tarafından kullanılan sunum dosyası formatını temsil eder. Bir sunum dosyası, her slaydın metin, resimler, biçimlendirme, animasyonlar ve diğer ortamlardan oluşabileceği bir slayt koleksiyonudur. Bu slaytlar, özel sunum ayarları ile slayt gösterileri şeklinde izleyicilere sunulur. ODP dosyaları, OpenDocument biçimine uyan uygulamalar (OpenOffice veya StarOffice gibi) tarafından açılabilir.

## Kısa Tarihçe

ODP dosya biçimi belirtimleri, ODF belirtimleri olarak geliştirilen standardı temel alır. Bu spesifikasyonlar geçmişte OASIS tarafından geliştirilen ve yayınlanan üç versiyon şeklinde aşağıdaki şekilde gelişmiştir:

`2005` - Sürüm 1.0, Mayıs 2005'te yayınlandı
"2007" - Sürüm 1.1, Şubat 2007'de yayınlandı
"2011" - Sürüm 1.2, Eylül 2011'de yayınlandı

ODF 1.0'dan 1.1 sürümlerine geçişte oldukça küçük değişiklikler oldu. [ODF 1.2 sürümü](https://www.oasis-open.org/standards#opendocumentv1.2), ODF spesifikasyonları için en son sürümdür ve ODS okuma/yazma ile ilgili uygulamaların geliştirilmesi için geliştiriciler tarafından danışılmalıdır.

## Dosya Biçimi Özellikleri

OpenDocument formatı, tek bir XML belgesi olarak belge gösterimini ve [ZIP](https://docs.fileformat.com/Compression/ZIP/) arşivi olarak bir paket içinde birkaç alt belge koleksiyonunu destekler. ZIP arşivindeki dosyaların her biri, tüm belgenin bir bölümünü saklar. Her alt belge, belgenin belirli bir yönünü saklar. Örneğin, bir alt belge stil bilgilerini içerir ve başka bir alt belge belgenin içeriğini içerir. Tipik bir ODF belgesi aşağıdaki bileşenlere sahiptir:

* `content.xml` – Belge içeriği ve içerikte kullanılan otomatik stiller.
* `styles.xml` – Belge içeriğinde kullanılan stiller ve stillerin kendisinde kullanılan otomatik stiller.
* `meta.xml` – Yazar veya son kaydetme eyleminin zamanı gibi belge meta bilgileri.
* `settings.xml` – Pencere boyutu veya yazıcı bilgisi gibi uygulamaya özel ayarlar.

Bunların yanı sıra, pakette belge küçük resmi, resimler vb. birçok başka alt belge olabilir.

Elektronik tablo belge dosyaları, içeriğin (tabloların) content.xml alt belgesinde depolandığı ODF dosyalarının alt kümesidir.

## Referanslar

* [OpenDocument - Wikipedia Tarafından](https://en.wikipedia.org/wiki/OpenDocument)

