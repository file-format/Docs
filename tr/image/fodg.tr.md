{
  "date" : "2019-10-11",
  "keywords" :[ "fodg dosyası", "fodg dosya biçimi", "fodg dosyası nedir", "dosya", "fodg örneği", "fodg dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument Çizim Dosyası Formatı",
  "description":"FODG dosya formatı ve FODG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Bir FODG dosyası nedir?

.fodg uzantılı bir dosya, çizim öğelerini depolamak için bir Apache OpenOffice Çizim dosya biçimidir. Advancement of Structural Information Standards (OASIS) tarafından belirtilen dosya formatı özelliklerine dayanmaktadır. OpenOffice grafikleri için başka bir benzer dosya biçimi, çizim öğelerini bir vektör görüntüsü olarak depolayan [ODG](/tr/image/odg/) biçimidir. FODG dosyaları OpenOffice ve LibreOffice ile açılabilir. Örneğin, OpenOffice tarafından desteklenen diğer dosya biçimleri arasında [ODT](/tr/word-processing/odt/), ODF, [ODP](/tr/presentation/odp/) ve [ODS](/tr/spreadsheet/ods/) yer alır.

## FODG Dosya Biçimi

FODG, OpenDocument'in OASIS OpenDocument Format ISO/IEC 26300 ile uyumlu XML dosya formatını temel alır. İnternet Medya Türü application/vnd.oasis.opendocument.graphics'e sahiptir ve ayrıca org.oasis-open.opendocument public.composite-content ile uyumludur. . XML yapısı elektronik tablo, çizim dosyaları ve metin belgeleri gibi tüm belge türleri için ortaktır. OpenOffice belgeleri, içeriği, stilleri, meta verileri ve uygulama ayarlarını dört ayrı XML dosyasına ayırarak endişelerin ayrılmasından yararlanır.

`<office:document-content>` - Belge içeriği ve içerikte kullanılan otomatik stiller.
`<office:document-styles>` - Belge içeriğinde kullanılan stiller ve stillerin kendisinde kullanılan otomatik stiller.
`<office:document-meta>` - Yazar veya son kaydetme eyleminin zamanı gibi belge meta bilgileri.
`<office:document-settings>` - Pencere boyutu veya yazıcı bilgileri gibi uygulamaya özel ayarlar.

## Referanslar ##
* [v 1.3 Standardizasyonu için Gelecek Spesifikasyonları](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [Office Uygulamaları için OASIS Açık Belge Formatı](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Biçimi - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

