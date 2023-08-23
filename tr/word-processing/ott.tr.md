{
  "date" : "2019-10-11",
  "keywords" :[ "ott dosyası", "ott dosya biçimi", "ott dosyası nedir", "dosya", "ott örneği", "ott dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - OpenDocument Şablon Dosyası",
  "description":"OTT dosya formatı ve OTT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## OTT dosyası nedir?

OTT uzantılı dosyalar, uygulamalar tarafından OASIS'in OpenDocument standart formatına uygun olarak oluşturulan şablon belgeleri temsil eder. Bunlar, ücretsiz OpenOffice Writer gibi kelime işlemci uygulamalarıyla oluşturulur ve bu şablon dosyalarından yeni belgeler oluşturmak için kullanılabilecek ayarları tutabilir. Bu ayarlar, sayfa kenar boşluklarını, kenarlıkları, üst bilgileri, alt bilgileri ve diğer sayfa ayarlarını içerir. Bu tür şablonlar, şirket antetli kağıtları ve standartlaştırılmış formlar gibi resmi belgelerde kullanılır.

## Kısa Tarih ##

ODP dosya biçimi belirtimleri, ODF belirtimleri olarak geliştirilen standardı temel alır. Bu spesifikasyonlar geçmişte OASIS tarafından geliştirilen ve yayınlanan üç versiyon şeklinde aşağıdaki şekilde gelişmiştir:

**2005:** Sürüm 1.0, Mayıs 2005'te yayınlandı

**2007:** Sürüm 1.1, Şubat 2007'de yayınlandı

**2011:** Sürüm 1.2, Eylül 2011'de yayınlandı

ODF 1.0'dan 1.1 sürümlerine geçişte oldukça küçük değişiklikler oldu. [ODF 1.2 sürümü](https://www.oasis-open.org/standards#opendocumentv1.2), ODF spesifikasyonları için en son sürümdür ve ODS okuma/yazma ile ilgili uygulamaların geliştirilmesi için geliştiriciler tarafından danışılmalıdır.

## Dosya Biçimi Özellikleri

OpenDocument formatı, tek bir XML belgesi olarak belge temsilini ve [ZIP](/tr/compression/zip/) arşivi olarak bir paket içinde birkaç alt belge koleksiyonunu destekler. ZIP arşivindeki dosyaların her biri, tüm belgenin bir bölümünü saklar. Her alt belge, belgenin belirli bir yönünü saklar. Örneğin, bir alt belge stil bilgilerini içerir ve başka bir alt belge belgenin içeriğini içerir. Tipik bir ODF belgesi aşağıdaki bileşenlere sahiptir:

* content.xml – Belge içeriği ve içerikte kullanılan otomatik stiller.
* styles.xml – Belge içeriğinde kullanılan stiller ve stillerin kendisinde kullanılan otomatik stiller.
* meta.xml – Yazar veya son kaydetme eyleminin zamanı gibi belge meta bilgileri.
* settings.xml – Pencere boyutu veya yazıcı bilgileri gibi uygulamaya özel ayarlar.

Bunların yanı sıra, pakette belge küçük resmi, resimler vb. birçok başka alt belge olabilir. Belge dosyaları, içeriğin (tabloların) //content.xml// alt belgesinde depolandığı ODF dosyalarının alt kümesidir.

## Referanslar ##

* [OpenDocument - Wikipedia Tarafından](https://en.wikipedia.org/wiki/OpenDocument)

