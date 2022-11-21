{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","jhtml dosyası", "jhtml dosya biçimi", "jhtml dosya türü", "dosya", "tür", "jhtml dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - Java HTML Dosyası",
  "description":"JHTML dosya formatı ve JHTML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## JHTML dosyası nedir?

.jhtml uzantılı bir dosya, bir istemci tarayıcıda bu sayfayı istediğinde sunucuda yürütülen [Java](/tr/programming/java/) kodlu bir [HTML](/tr/web/html/) dosyasıdır. Sunucu istekleri işler, işlevde bulunan Java işlevlerini yürütür ve sayfayı istemcinin tarayıcısına döndürür. JHTML sayfalarına katıştırılmış Java nesneleri, bu tür sayfalara yönelik istekleri işlemek için sunucuda çalışır. JHTML dosyaları, JDBC (Java [Veritabanı](/tr/veritabanı/) Bağlantı) bağlantısını kullanarak veritabanındaki bilgilere de erişebilir. JHTML dosyaları herhangi bir metin düzenleyicide açılabilir ve Google Chrome, Firefox ve Safari gibi web tarayıcılarında görüntülenebilir.

## JHTML Dosya Biçimi

JHTML, ATG'nin tescilli bir teknolojisidir ve ATG (Art Technology Group) Dynamo Document Editor kullanılarak oluşturulabilir. JHTML dosyaları, standart HTML ve Java kodu kullanılarak düz metin dosyası biçiminde yazılır. Bunlar, Java nesnelerine başvuran özel etiketlere ek olarak standart HTML etiketlerini içerir. Kullanıcı tarafından böyle bir sayfa talep edildiğinde, HTTP sunucusu talebi bir Java uygulama sunucusuna iletir. JHTML sayfası önce .java dosyasına dönüştürülür ve sunucu uygulaması olarak yürütülen bir [.class](/tr/programming/class/) dosyası oluşturmak için derlenir. Bu, kullanıcıya görüntülenmek üzere istekte bulunan tarayıcıya geri döndürülen bir standart HTTP ve HTML verileri akışı oluşturur. Bu, sunucuda veritabanıyla ilgili sorguları çalıştırmak ve nihai birikmiş sonucu müşterinin tarayıcısına döndürmek için yararlıdır.

## Referanslar

* [HTML belgesinin Global Yapısı](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

