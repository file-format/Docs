{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","mhtml dosyası", "mhtml dosya biçimi", "mhtml dosya türü", "dosya", "tür", "mhtml dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML Dosyası",
  "description":"MHTML dosya formatı ve MHTML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## MHTML dosyası nedir?

MHTML uzantılı dosyalar, bir dizi farklı uygulama tarafından oluşturulabilen bir web sayfası arşiv biçimini temsil eder. Biçim, web **[HTML](/tr/web/html/)** kodunu ve ilişkili kaynakları tek bir dosyaya kaydettiği için arşiv biçimi olarak bilinir. Bu kaynaklar, resimler, uygulamalar, animasyonlar, ses dosyaları vb. gibi web sayfasına bağlı her şeyi içerir. MHTML dosyaları, Internet Explorer ve Microsoft Word gibi çeşitli uygulamalarda açılabilir. Microsoft Windows, Windows'ta sorun çıkaran herhangi bir uygulamanın kullanımı sırasında gözlemlenen sorunların senaryolarını kaydetmek için MHTML dosya biçimini kullanır. MHTML dosya formatı, sayfa içeriklerini düz metin e-posta ile ilgili spesifikasyonlar olan message/rfc822'de tanımlanan spesifikasyonlara benzer şekilde kodlar. Biçimin asıl özellikleri, [RFC 2557](https://tools.ietf.org/html/rfc2557) ile ayrıntılı olarak verilmiştir.

## MHTML Dosya Biçimi

MHTML, kaynaklarıyla birlikte tek bir web arşivinde HTML web sayfalarını kodlama yeteneği nedeniyle Toplu HTML belgelerinin MIME Kapsüllemesi olarak da bilinir. RFC 2557 spesifikasyonuna göre, toplu belge, bir kök kaynağı (nesne) ve URI'ler aracılığıyla ona bağlı diğer kaynakları içeren MIME kodlu bir mesajdır. Bu tür diğer kaynaklar, satır içi resimlerin, stil sayfalarının, apletlerin vs. temsili olabilir. Ayrıca bunlar, diğer multimedya belgelerinin kökü olabilir. MHTML dosya formatı için tam belge özellikleri [RFC 2557](https://tools.ietf.org/html/rfc2557)'de ayrıntılı olarak verilmiştir ve bu dosya formatının okunması/yazılması için her türlü uygulama geliştirme için başvurulmalıdır. Standart, başvurulacak vücut bölümlerinin bir Content-ID veya bir Content-Location tarafından tanımlanabileceğini belirtir.

### MIME İçerik Başlıkları

Diğer gövde bölümlerindeki kaynaklara URI başvurularını çözümlemek için bir MIME içerik başlığı olan Content-Location tanımlanır. Bu başlık, herhangi bir mesaj veya içerik başlığında bulunabilir.

### İçerik-Konum Başlığı

İçerik-Konum, yerleştirildiği bir vücut bölümünün içeriğini etiketleyen bir URI'nin temsilidir. Değeri, mutlak veya göreli bir URI olabilir. Bir mesajın bazı veya tüm alıcıları tarafından alınamayan bir kaynağı etiketlemek için kullanılabilir. Tek bir iletinin yalnızca tek bir Content-Location başlığına sahip olmasına izin verilir. Hem Content-Location hem de Content-ID etiketlerine sahip vücut kısımlarını içeren çok parçalı/ilgili yapı örneği:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### MHTML Toplamalarının URI'leri

MHTML toplamının URI'si, kök URI'sinden farklıdır. İçerik-Konum başlık alanı, çok parçalı/ilgili bir başlığın başlığında kullanılıyorsa tüm topluluğa uygulanmalıdır. Benzer şekilde, alınan kaynaklar kümesi, bu kümeyi almak için MHTML topluluğuna atıfta bulunan URI kullanıldığında, parçalarının İçerik Konumları kullanılarak alınan kaynaklar kümesinden farklı olabilir. Örneğin, bir MHTML toplamının alınması eski bir sürümü döndürürken, kök URI'nin ve onun satır içi bağlantılı nesnelerinin alınması daha yeni bir sürüm döndürebilir.

## Referanslar

* [Toplu Belgelerin MIME Kapsüllemesi - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML Dosya Biçimi - Wikipedia Tarafından](https://en.wikipedia.org/wiki/MHTML)

