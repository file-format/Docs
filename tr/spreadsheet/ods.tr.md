{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "dosya", "uzantı", "dosya formatı", "OpenDocument Elektronik Tablosu"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ODS dosyasının ne olduğunu ve bunları oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"ODS dosyası nedir?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ODS dosyası nedir?

.ods uzantılı dosyalar, kullanıcı tarafından düzenlenebilen OpenDocument Elektronik Tablo Belge biçimini ifade eder. Veriler, ODF dosyasında satırlar ve sütunlar halinde saklanır. XML tabanlı bir formattır ve Açık Belge Formatları (ODF) ailesindeki çeşitli alt tiplerden biridir. Biçim, OASIS tarafından yayınlanan ve sürdürülen ODF 1.2 belirtimlerinin bir parçası olarak belirtilir. Windows ve diğer işletim sistemlerindeki bir dizi uygulama, Microsoft Excel, NeoOffice ve LibreOffice dahil olmak üzere ODS dosyalarını düzenleme ve işleme için açabilir. ODS dosyaları, farklı uygulamalar tarafından [XLS](/tr/spreadsheet/xls/), [XLSX](/tr/spreadsheet/xlsx/) ve diğerleri gibi diğer elektronik tablo biçimlerine de dönüştürülebilir.

## Kısa Tarih ##

ODS dosya biçimi belirtimleri, ODF belirtimleri olarak geliştirilen standardı temel alır. Bu spesifikasyonlar geçmişte OASIS tarafından geliştirilen ve yayınlanan üç versiyon şeklinde aşağıdaki şekilde gelişmiştir:

`2005`- Sürüm 1.0, Mayıs 2005'te yayınlandı

"2007" - Sürüm 1.1, Şubat 2007'de yayınlandı

"2011" - Sürüm 1.2, Eylül 2011'de yayınlandı

ODF 1.0'dan 1.1 sürümlerine geçişte oldukça küçük değişiklikler oldu. [ODF 1.2 sürümü](https://www.oasis-open.org/standards#opendocumentv1.2), ODF spesifikasyonları için en son sürümdür ve ODS okuma/yazma ile ilgili uygulamaların geliştirilmesi için geliştiriciler tarafından danışılmalıdır.

## ODS Dosya Biçimi ##

OpenDocument formatı, tek bir XML belgesi olarak belge gösterimini ve bir paket içinde [ZIP](/tr/compression/zip/) arşivi olarak birkaç alt belge koleksiyonunu destekler. ZIP arşivindeki dosyaların her biri, tüm belgenin bir bölümünü saklar. Her alt belge, belgenin belirli bir yönünü saklar. Örneğin, bir alt belge stil bilgilerini içerir ve başka bir alt belge belgenin içeriğini içerir. Tipik bir ODF belgesi aşağıdaki bileşenlere sahiptir:

* `content.xml` – Belge içeriği ve içerikte kullanılan otomatik stiller.
* `styles.xml` – Belge içeriğinde kullanılan stiller ve stillerin kendisinde kullanılan otomatik stiller.
* `meta.xml` – Yazar veya son kaydetme eyleminin zamanı gibi belge meta bilgileri.
* `settings.xml` – Pencere boyutu veya yazıcı bilgisi gibi uygulamaya özel ayarlar.

Bunların yanı sıra, pakette belge küçük resmi, resimler vb. birçok başka alt belge olabilir.

Elektronik tablo belge dosyaları, içeriğin (sayfaların) content.xml alt belgesinde depolandığı ODF dosyalarının alt kümesidir.

## Referanslar ##

* [OpenDocument - Wikipedia Tarafından](https://en.wikipedia.org/wiki/OpenDocument)

