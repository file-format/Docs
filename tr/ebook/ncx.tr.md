{
  "date" : "2021-03-23",
  "keywords" :[ "NCX", "EPUB Gezinme Kontrolü XML Dosyası", "uzantı", "biçim", "E-Kitap", "TOC", "DAISY Konsorsiyumu"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"EPUB Navigation Control XML Dosyası (NCX) dosya formatı ve NCX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"NCX - EPUB Gezinme Kontrolü XML Dosyası",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Bir NCX dosyası nedir? ##

XML için Gezinme Denetimi dosyası olarak kısaltılan NCX dosyası, genellikle toc.ncx olarak adlandırılır. Bu dosya, bir EPUB dosyası için hiyerarşik içindekiler tablosundan oluşur. NCX spesifikasyonu Digital Talking Book (DTB) için geliştirilmiştir ve bu dosya formatı **DAISY Consortium** tarafından sağlanmaktadır ve EPUB spesifikasyonunun bir parçası değildir. NCX dosyası, içinde bir mime türü **application/x-dtbncx+xml** içerir.

## NCX Spesifikasyonu ##

NCX dosyası, çeşitli XML etiketleri içerir. Kimlikten bahsetmek için `meta name="dtb:uid"` gibi meta etiketler kullanılır. "meta name="dtb:rought"" öğesi, "navMap" etiket öğesinin derinliğine eşit olarak ayarlanır. "navPoint" öğeleri, hiyerarşik bir içindekiler tablosu oluşturmak için iç içe yerleştirilebilir. "navLabel" içeriği, .ncx kullanan okuma sistemleri tarafından oluşturulan içindekiler tablosunda görünen metindir. "navPoint" öğesinin içeriği, bildirimde listelenen bir içerik belgesine işaret eder ve ayrıca bir öğe tanımlayıcısı içerebilir

EPUB'da kullanıldığı şekliyle NCX spesifikasyonundaki belirli istisnaların açıklaması. Burada bir NCX dosyası örneğini görebilirsiniz:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## Referanslar ##

* [Wikipedia'dan EPUB](https://en.wikipedia.org/wiki/EPUB)
* [toc.ncx'e dahil edilecek dosyalar](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

