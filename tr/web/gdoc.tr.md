{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC Dosyası - Google Dokümanlar Kısayolu",
  "description":"GDOC dosyasının ne olduğu ve GDOC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## GDOC dosyası nedir?

GDOC dosyası, bulut tabanlı bir belge depolama hizmeti olan Google Drive'da bulunan bir dosyaya işaret eden bir kısayol dosyasıdır. Google Drive istemcisi bir bilgisayara yüklendiğinde ve içinde bir belge oluşturulduğunda, sürücü çevrimiçi bulut depolama alanında bir belge oluşturur ve bu belgenin [URL](/tr/web/url/) adresini yerel Google'daki GDOC dosyasına yazar. Sürücü klasörü. Bu kısayol dosyası çift tıklandığında, varsayılan web tarayıcısı belgeyi [URL](/tr/web/url/) konumundan açar. Bu kısayol dosyası bu klasörün dışına taşınırsa, çevrimiçi belgeye olan bağlantı bozulur.

## GDOC Dosya Biçimi - Daha Fazla Bilgi

GDOC dosyası, [JSON](/tr/web/json/) dosya biçiminde yazılmış çevrimiçi belgeye kısayol içerir. GDOC dosyalarını açan tarayıcı, URL bilgisini okur ve kullanıcının belgenin depolandığı bu Google hesabında oturum açmış olması koşuluyla bağlantılı belgeyi görüntülenmek üzere açar. GDOC dosyaları, belgenin içeriğini içermez.

### GDOC Dosya Örneği

GDOC dosyası bir metin düzenleyicide açılabilir ve içeriği aşağıdaki gibi görünür.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Görülebileceği gibi içerikler, bir belgenin URL'sine ve ilgili belge kimliğine sahip olan JSON'da biçimlendirilmiştir.

## Referanslar

* [Google Dokümanlar gdoc veya docx dosyalarını açmıyor](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en )

