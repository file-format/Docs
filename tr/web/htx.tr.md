{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX Dosyası - HTML Uzantısı Dosya Biçimi",
  "description" :"HTX dosyasının ne olduğunu ve HTX dosyasını oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## HTX dosyası nedir?

Bir HTX dosyası aslında veritabanı sorgu sonuçlarını bir web sayfası olarak görüntülemek için veri değişkenleri içeren bir HTML dosyasıdır. Çoğunlukla Microsoft FrontPage Web geliştirme yazılımıyla oluşturulan HTX dosyaları, karşılık gelen Internet Database Connector (.IDC) dosyasıyla aynı klasöre kaydedilmek üzere kaydedilir.

HTX dosyaları, Microsoft FrontPage gibi uygulamalarla ve Notepad, TextEdit veya Atom gibi herhangi bir metin düzenleyiciyle açılabilir.

## HTX Dosya Biçimi

HTX dosyaları, bir veritabanından veri almak ve görüntülemek için değişkenlerde kaydetmek için kod içeren düz metin dosyası olarak kaydedilir.


### HTX Dosya Örneği

Sorgu kısıtlamasını görüntülemek için bir sayfa başlığı ve kullanıcıya görüntülemek için sayfada görüntülenen belgeleri tanımlayan bir HTX dosyası örneği aşağıdaki gibidir.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

Bu örnek kodun çıktısı aşağıdaki gibidir.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Görüldüğü gibi HTX dosyası, sonuçların son kullanıcılara nasıl döndürüldüğünü ve görüntülendiğini biçimlendiren bir şablondur. Bazı IIS uzantıları ve Dizin Oluşturma Hizmeti ile HTML biçiminde yazılmıştır. Bu uzantılar, sonuçları işlemek için değişken adlarını ve diğer kodları içerir.

## Referanslar

* [Sonuçları .Htx Dosyasında Biçimlendirme](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

