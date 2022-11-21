{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON Dosyası - Konsept Uygulama Kaynak Dosya Formatı",
  "description" :"CON dosyası nedir ve CON dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## CON dosyası nedir?

Bir CON dosyası, **Konsept Uygulama Sunucusu** için geliştirilen uygulama için bir kaynak kod dosyasıdır. Sunucu ve kullanıcı arasında veri alışverişi için uygulama yazmak için kullanılır. Kullanıcı tarafında Concept Client kurulu olması koşuluyla, sunucuda barındırılan CON dosyalarına bir Web tarayıcısı ile erişilebilir. Konsept Uygulama sunucusu, bir [SQL](/tr/database/sql/) altküme veritabanı motoruna (TinDB) sahip olabilecek küçük ölçekli programlama diline sahip bir web sunucusudur.

CON dosyaları RadGs Concept Application Server ile açılabilir/çalışabilir.

## CON Dosya Biçimi - Daha Fazla Bilgi

CON dosyaları sunucuda barındırılır ve kullanıcı makinesindeki web tarayıcısı kullanılarak erişilir. Konsept [URL'ler](/tr/web/url/) normal HTTP url'lerinden farklıdır ve **concept://** ile başlar.

### CON Dosyası URL Örneği

Konsept Uygulama Sunucusunda barındırılan bir CON dosyasına aşağıdaki gibi URL'ler kullanılarak web tarayıcısı aracılığıyla erişilebilir:

```
concept://domain.server.com/web_application/main.con.
```
## Referanslar

* [Konsept Uygulama Sunucusu](https://github.com/Devronium/ConceptApplicationServer)

