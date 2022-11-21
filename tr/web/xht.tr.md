{
  "date" : "2021-05-24",
  "keywords" :["xht", "Dosya", "Uzantı", "Dosya Biçimi", "Dosya Uzantısı", "genişletilmiş köprü metni biçimlendirme dili"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHT",
  "description":"XHT dosya formatı ve XHT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## XHT dosyası nedir?

.xht uzantılı bir dosya, kendisi [XML](/tr/web/xml/) tabanlı bir biçimlendirme dosyası olan [XHTML](/tr/web/xhtml/) (Genişletilmiş Köprü Metni İşaretleme Dili) dosya türüyle ilişkili bir web dosyasıdır. Bu dosyaların her ikisi de HTML'ye benzer, ancak daha katı bir XML benzeri sözdizimine sahiptir. XHT dosyaları daha yapılandırılmış olacak şekilde tasarlanmıştır, daha az komut dosyası içerir ve XML'in mevcut olanaklarını kullanmanın yanı sıra geneldir.

## XHT Dosya Biçimi

Bir XHT dosyası, varsayılan olarak UTF-8 kodlamasıyla düz metin dosyası olarak oluşturulur ve saklanır. Unicode kodlamayı destekleyen herhangi bir metin düzenleyiciyle açılıp düzenlenebilen bir XHTML belgesinin tüm kaynak kodunu içerir. Metin editörlerine ek olarak, XHT dosya formatı çoğu modern web tarayıcısı tarafından anlaşılabilir ve bunlar kullanılarak açılabilir.

## XHT Örneği

Aşağıdaki bir XHT belgesi örneği, XML bildirimlerini tanımlar.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## Referanslar ##

* [XHTML Tarihi: 1990'lardan Günümüze](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

