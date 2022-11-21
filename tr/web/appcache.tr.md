{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPCACHE Dosyası - HTML5 Cache Manifest Dosya Biçimi",
  "description" :"APPCACHE dosyası nedir ve APPCACHE dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## APPCACHE dosyası nedir?

APPCACHE dosyası, web uygulamalarına çevrimdışı erişim için tarayıcılar tarafından önbelleğe alınacak kaynakların listesini içeren bir metin dosyasıdır. Bu, internet bağlantısı olmadığında kullanışlıdır. Böyle bir durumda tarayıcı, web içeriğine erişim sağlamak için çevrimdışı önbellek kaynaklarını kullanır. APPCACHE dosyası, resimler (örneğin **[PNG](/tr/image/png/)**, **[WEBP](/tr/image/webp/)**, vb.), stil sayfaları **([ CSS])(/tr/web/css/)** ve betik dosyaları (Javascript **[JS](/tr/web/js/)** dosyaları gibi).

**APPCACHE dosyalarını açabilen** uygulamalar arasında Google Chrome, Safari ve Firefox gibi web tarayıcıları bulunur.

## APPCACHE Dosya Biçimi - Daha Fazla Bilgi

APPCACHE dosyaları, internet bağlantısı olmadan çalışmak için web sayfalarına çevrimdışı erişim sağlayan basit metin dosyalarıdır. APPCACHE'nin varlığı, bir sayfayı çevrimdışı kullanılabilir olarak tanımlar.

### Bir APPCACHE dosyasına nasıl başvurulur?

HTML sayfanızda, bir APPCACHE dosyasına aşağıdaki şekilde başvurulmaktadır.

```
<html manifest="example.appcache">
  ...
</html>
```

## APPCACHE Manifest dosyasının yapısı

Basit bir APPCACHE bildirim dosyası aşağıdaki gibi görünür.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Bu en basit örnektir ve daha karmaşık yapılar da mevcut olabilir.

## APPCACHE Manifest'in Avantajları

Önbellek arabiriminin kullanılması web uygulamalarına aşağıdaki avantajları sağlar.

1. Çevrimdışı Tarama - Önbellek arayüzü, son kullanıcıların Çevrimdışı olduklarında tüm sitenize göz atmalarını sağlar.
1. Hız - önbellek, çevrimdışı içeriğe doğrudan diskten yüksek hızlı erişim sağlar
1. Her zaman erişilebilirlik - Sitenizin çökmesi durumunda, kullanıcılar web içeriğine erişmeye devam edecek ve çevrimdışı deneyimi yaşayabilecektir.

## Referanslar

* [AppCache Bildirimi İçin Başlangıç Kılavuzu](https://web.dev/appcache-beginner/)

