{
  "date" : "2019-12-16",
  "keywords" :["OTS", "dosya", "uzantı", "dosya formatı", "Excel", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"OTS dosya formatı ve OTS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"OTS - OpenDocument Elektronik Tablo Şablonu Dosya Biçimi",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## OTS dosyası nedir?

.ots uzantılı bir dosya, Apache OpenOffice'te bulunan Calc uygulama yazılımıyla oluşturulan bir OpenDocument Elektronik Tablo Şablonu dosyasıdır. Calc uygulama yazılımı, Microsoft Office'te bulunan Excel'e benzer. OTS dosya biçimi, stiller, yazı tipi, veriler, elektronik tablo düzeni ve biçimlendirme ile ilgili önceden tanımlanmış ayarları içeren şablonlar oluşturmak için kullanılır. OTF dosyalarında "mime-type application/vnd.oasis.opendocument.spreadsheet-template" bulunur. Bu şablon dosyaları, [ODS dosya biçiminde](/tr/spreadsheet/ods/) kaydedilen gerçek veri dosyalarını oluşturmak ve kaydetmek için bir başlangıç noktası olarak kullanılabilir. OTS dosyaları, OpenOffice ve LibreOffice gibi uygulamalarla kullanılabilir.

## OTS Dosya Biçimi

OTS dosyaları, [ZIP](/tr/compression/zip/) arşivi olarak bir paketle birlikte birkaç alt belge koleksiyonundan oluşan OASIS'in OpenDocument XML tabanlı dosya biçiminde kaydedilir. Her zip arşivi, tüm belgenin bir bölümünü saklar ve her alt belge, belgenin belirli bir yönünü saklar. Örneğin, bir alt belge stil bilgilerini içerir ve başka bir alt belge belgenin içeriğini içerir. Tipik bir ODF belgesi aşağıdaki bileşenlere sahiptir:

### OTS İçeriği.xml

Content.xml dosyası, belgenin gerçek içeriğini içerir. Ancak bu, görüntüler gibi ikili verileri içermez.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml of OTS Dosya Biçimi

styles.xml dosyası stil bilgilerini içerir ve ağırlıklı olarak biçimlendirme ve düzen için kullanılır. Stil türleri şunları içerir:

* Paragraf stilleri
* Sayfa stilleri
* Karakter stilleri
* Çerçeve stilleri
* Liste stilleri

### Meta.xml

Meta.xml dosyası, Yazar, Son Değiştirme Tarihi vb. gibi dosya meta verileri hakkında bilgiler içerir.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Ayarlar.xml

"settings.xml" dosyası, yakınlaştırma faktörü ve imleç konumu gibi belge düzeyi ayarlarını içerir.

## Referanslar ##

* [OpenDocument 1.2 spesifikasyonu](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Wikipedia Tarafından](https://en.wikipedia.org/wiki/OpenDocument)

