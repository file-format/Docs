{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","xbrl dosyası", "xbrl dosya formatı", "xbrl dosya türü", "dosya", "tür", "xbrl dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - İş ve Finansal Raporlama Dosya Formatı",
  "description":"XBRL dosya formatı ve XBRL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## XBRL dosyası nedir?

.xbrl (eXtensible Business Reporting Language) uzantılı bir dosya, işletme bilgilerini değiş tokuş etmek için ücretsiz olarak kullanılabilen ve küresel bir çerçevedir. Artık, eski kağıt tabanlı raporları daha kullanışlı ve doğru dijital kayıtlarla değiştiren standart biçimlerden biri olarak yaygın şekilde kullanılmaktadır. XBRL dosyaları kullanılarak değiş tokuş edilen veriler, defterleri, finansal ayrıntıları ve bilançoları içerir. Her türlü iş bilgisinin hazırlanmasından analiz aşamasına kadar veri işlemeye izin veren veri etiketlerini destekler. XBRL dosyaları, Rivet Software Dragon View XBRL Viewer gibi yazılımlar ve [Aspose.Finance](https://products.aspose.com/finance) gibi API'ler kullanılarak açılabilir.

## XBRL Dosya Biçimi

XBRL, dünya çapında yaygın olarak kullanılan, dijital iş raporlaması için açık bir uluslararası standarttır. Rapor sıralama ve analiz için verileri formüle etmek amacıyla iş verilerinin her bir öğesini tanımlamak için etiketler olarak bilinen XBRL öğelerini kullanan [XML](/tr/web/xml/) tabanlı bir dildir. XBRL dosya biçimi belirtimleri, şu anda [XBRL sürüm 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) ile XBRL International, Inc tarafından geliştirilmiş ve yayınlanmıştır. kullanıcıların kullanımına sunulmuştur.

### XBRL Belge Yapısı

[XBRL 2.1 etiketleri] hakkında eksiksiz bilgi(https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) programcılar tarafından bu dosya biçimini çalıştırmak için uygulamalar yazmaya yönlendirilebilir. Bir XBRL, bir XBRL örneğinden ve bir taksonomi koleksiyonundan oluşur.

**`XBRL Örneği`** - XBRL örneği,<xbrl> kök eleman. Büyük bir XML belgesi, içine katıştırılmış birden fazla XBRL örneği içerebilir.

**`XBRL Taksonomisi`** - [XBRL Taksonomisi](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +corrected-errata-2013-02-20.html#_5), XML şema yapıları ve doğrudan başvurulan dış bağlantılar öğesi kümesi olarak tanımlanır. Bağlantı tabanı referanslarını gösteren ölçeklenebilir bir taksonomi şeması aşağıdaki gibidir.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Referanslar ##

* [XBRL - Wikipedia Tarafından](https://en.wikipedia.org/wiki/XBRL)
* [Genişletilebilir İş Raporlama Dili (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- hata-2013-02-20.html)

