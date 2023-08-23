{
  "date" : "2019-10-11",
  "keywords" :[ "odt dosyası", "odt dosya biçimi", "odt dosyası nedir", "dosya", "odt örneği", "odt dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - OpenDocument Metin Dosyası",
  "description":"ODT dosya formatı ve ODT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## ODT dosyası nedir?

ODT dosyaları, OpenDocument Metin Dosyası biçimini temel alan kelime işlem uygulamalarıyla oluşturulan belge türüdür. Bunlar, ücretsiz OpenOffice Writer gibi kelime işlemci uygulamalarıyla oluşturulur ve metin, resim, nesne ve stil gibi içerikleri tutabilir. Microsoft Word için [DOCX](/tr/word-processing/docx/) ne ise, Writer kelime işlemcisi için de ODT dosyası odur. Google Docs ve Google'ın Google Drive'a dahil olan web tabanlı kelime işlemcisi dahil olmak üzere çeşitli uygulamalar, ODT dosyalarını düzenleme için açabilir. Microsoft Word ayrıca ODT dosyalarını açabilir ve onu [DOC](/tr/word-processing/doc/) ve DOCX gibi diğer biçimlerde kaydedebilir.

## Kısa Tarih ##

ODP dosya biçimi belirtimleri, ODF belirtimleri olarak geliştirilen standardı temel alır. Bu spesifikasyonlar geçmişte OASIS tarafından geliştirilen ve yayınlanan üç versiyon şeklinde aşağıdaki şekilde gelişmiştir:

**2005** Sürüm 1.0, Mayıs 2005'te yayınlandı

**2007:** Sürüm 1.1, Şubat 2007'de yayınlandı

**2011:** Sürüm 1.2, Eylül 2011'de yayınlandı

ODF 1.0'dan 1.1 sürümlerine geçişte oldukça küçük değişiklikler oldu. [ODF 1.2 sürümü](https://www.oasis-open.org/standards#opendocumentv1.2), ODF spesifikasyonları için en son sürümdür ve ODS okuma/yazma ile ilgili uygulamaların geliştirilmesi için geliştiriciler tarafından danışılmalıdır.

## Dosya Biçimi Özellikleri ##

OpenDocument formatı, tek bir XML belgesi olarak belge temsilini ve [ZIP](/tr/compression/zip/) arşivi olarak bir paket içinde birkaç alt belge koleksiyonunu destekler. ZIP arşivindeki dosyaların her biri, tüm belgenin bir bölümünü saklar. Her alt belge, belgenin belirli bir yönünü saklar. Örneğin, bir alt belge stil bilgilerini içerir ve başka bir alt belge belgenin içeriğini içerir. Tipik bir ODF belgesi aşağıdaki bileşenlere sahiptir:

* content.xml – Belge içeriği ve içerikte kullanılan otomatik stiller.
* styles.xml – Belge içeriğinde kullanılan stiller ve stillerin kendisinde kullanılan otomatik stiller.
* meta.xml – Yazar veya son kaydetme eyleminin zamanı gibi belge meta bilgileri.
* settings.xml – Pencere boyutu veya yazıcı bilgileri gibi uygulamaya özel ayarlar.

Bunların yanı sıra, pakette belge küçük resmi, resimler vb. birçok başka alt belge olabilir. Belge dosyaları, içeriğin (tabloların) //content.xml// alt belgesinde depolandığı ODF dosyalarının alt kümesidir.

## Referanslar ##

* [OpenDocument - Wikipedia Tarafından](https://en.wikipedia.org/wiki/OpenDocument)

