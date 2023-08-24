{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion İşaretleme Dili Dosyası",
  "description" :"CFML dosyasının ne olduğu ve CFML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## CFML dosyası nedir?

.cfml uzantılı bir dosya, web sayfası oluşturmak için kullanılan bir ColdFusion İşaretleme Dili dosyasıdır. ColdFusion uygulamasının programcı tarafından nasıl geliştirileceğini tanımlamak için kullanılan bir dizi kuralı ifade eder. ColdFusion, [ASP](/tr/web/asp/), [PHP](/tr/programming/php/), vb. gibi diğer teknolojilerden daha azıyla ve hızlı bir şekilde sunucu tarafı web uygulamaları oluşturmak için kullanılan bir programlama dilidir. CML dosyalarını açabilen uygulamalardan bazıları Adobe ColdFusion 2018, Adobe ColdFusion Builder ve Adobe Dreamweaver'dır.

## CFML Dosya Biçimi - Daha Fazla Bilgi

CFML dosyaları biçimlendirme dosyalarıdır ve etiketler biçiminde web öğeleri içerir. Bunlar, herhangi bir metin düzenleyicide açılıp düzenlenebilen metin dosyalarıdır. CFML dosyaları, [HTML](/tr/web/html/) dosyasına benzer birkaç etiketten oluşur ve genellikle bir açılış ve bir kapanış etiketinden oluşur. Bu etiketler ayrıca bir veya daha fazla özellik içerebilir.

### Etiketler Sözdizimi

Aşağıda, CFML etiketlerinin genelleştirilmiş sözdizimi verilmiştir.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Çoğu etiket nitelikleri kabul eder ve aşağıdaki gibi tanımlanır.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Bu etiketlerin bazıları, aşağıdaki sözdizimine sahip birden çok özelliği de kabul eder.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML Kodu Örneği

İşte gerçek bir CFML etiketi - "cfoutput" etiketi kullanan bir örnek:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Referanslar

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

