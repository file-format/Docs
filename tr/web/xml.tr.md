{
  "date" : "2019-10-11",
  "keywords" :["xml", "Dosya", "Uzantı", "Dosya Biçimi", "Dosya Uzantısı", "genişletilebilir biçimlendirme dili"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XML Dosya Biçimi",
  "description":"XML dosya formatı ve XML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## XML dosyası nedir?

XML, **[HTML](/tr/web/html/)**'ye benzeyen, ancak nesneleri tanımlamak için etiketleri kullanma açısından farklı olan Genişletilebilir İşaretleme Dili anlamına gelir. XML dosya formatının oluşturulmasının ardındaki tüm fikir, yazılım veya donanım araçlarına bağımlı olmadan verileri depolamak ve taşımaktı. Popülaritesi, hem insan hem de makine tarafından okunabilir olmasından kaynaklanmaktadır. Bu, World Wide Web (WWW) gibi ağ üzerinden depolanacak ve paylaşılacak nesneler şeklinde ortak veri protokolleri oluşturmasını sağlar. XML'deki "X", dilin kullanıcı gereksinimlerine göre herhangi bir sayıda sembole genişletilebileceğini ima eden genişletilebilir içindir. Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/tr/web/xhtml/)** ve **[SVG](/tr/page-description-language) gibi birçok standart dosya formatının kullandığı özellikler bu özelliklerdir. /svg/)**.

## XML Dosya Biçimi

XML dosya biçimi, HTML ve XML belgeleri için bir programlama API'si olan XML Belge Nesne Modeli'ne (DOM) dayalıdır. XML DOM, XML belge öğelerine erişmek ve bunları değiştirmek için standart bir yöntem tanımlar. DOM ağacı aracılığıyla tüm öğelere erişmek için kullanılabilecek bir XML belgesinin ağaç yapısı görünümünü oluşturur. Mevcut öğeler değiştirilebilir/silinebilir ve ayrıca XML ağacında yeni öğeler oluşturulabilir. Bir XML belgesinin her elemanına düğüm denir. XML DOM aşağıdaki görseldeki gibidir.

{{< figure src="../XML DOM.png" alt="XML DOM'u" >}}

### Evrensel XML yaklaşımı

XML'in gücü, veri aktarımını ve platform değişikliklerini basitleştirerek onu ağ üzerinden veri iletişimi için evrensel bir dil haline getirir. Bu aynı zamanda verileri düz metin biçiminde depolayarak uyumsuz sistemler arasında veri alışverişini mümkün kılar. HTML, web üzerinden veri temsili içindir, XML ise veri alışverişi içindir. XML içinde kullanılan biçimlendirme etiketi çiftleri, okuma uygulamaları tarafından kullanılacak yapının temel öğelerini tanımlar.

## XML Örneği

Aşağıda, her kaydın CD'ler hakkında sanatçı, ülke, şirket, fiyat ve üretim yılı gibi bilgiler içerdiği basitleştirilmiş bir CD kataloğu örneği verilmiştir.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Referanslar

* [XML - Wikipedia Tarafından](https://en.wikipedia.org/wiki/XML)

