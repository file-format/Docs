{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DTSX dosyalarını oluşturabilen ve açabilen DXL dosya formatı ve API'ler hakkında bilgi edinin.",
  "title" :"DXL Dosya Formatı - Domino XML Dil Dosya Formatı",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## .DXL dosyası nedir?

DXL dosyası, kurumsal düzeyde iş işbirliği yazılımı Lotus Domino için oluşturulmuş XML tabanlı bir veri depolama dosyasıdır. Şemalar, tasarım öğeleri, görünüm, formlar, belgeler ve veritabanı verilerinin kendisi gibi Lotus Domino veritabanıyla ilgili verileri içerir. [XML](/tr/web/xml/), herhangi bir programlama dilinde yazılmış yazılım uygulamaları tarafından okunabilen evrensel bir dosya formatıdır. Ayrıca insan tarafından okunabilir ve herhangi bir metin düzenleyiciyle açılabilir. Bu nedenle DXL dosyaları, verileri değiştirilebilir dosya formatında dışa aktarma olanağı sağlar.

## DXL Dosya Formatı

DXL dosyaları XML dosya formatında kaydedilir ve herhangi bir programlama dilinde yazılmış uygulamalar tarafından kolayca okunabilir. Bu dosyalar, verileri ve ayarları, verileri kategorilere ayıran ve uygun bir sıraya göre düzenleyen XML etiketlerinde saklar.

### DXL Çıkış Örneği

Aşağıda Notes belgesinin çıktı metni alıntı çıktısı verilmiştir.

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## Referanslar

* [DXL Formatı - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

