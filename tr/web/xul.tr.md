{
  "date" : "2021-05-24",
  "keywords" :["xul", "Dosya", "Uzantı", "Dosya Biçimi", "Dosya Uzantısı", "XML Kullanıcı Arayüzü Dili"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML Kullanıcı Arayüzü Dil Dosyası",
  "description":"XUL dosya formatı ve XUL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## XUL dosyası nedir?

.xul uzantılı bir dosya ([XUL](https://wiki.mozilla.org/XUL:Home_Page), XML Kullanıcı Arayüzü Dili anlamına gelir), [XML](/tr/web/xml/) tabanlı bir biçimlendirme dili dosyasıdır. kullanıcı arayüzleri oluşturmak. Mozilla tarafından, geliştiricilerin web sayfaları oluşturmak için kullanılan diğer biçimlendirme dillerine benzer grafik kullanıcı arabirimi öğeleri oluşturması için geliştirilmiştir. XUL, Mozilla tarafından Mozilla kod tabanını kullandığı Firefox tarayıcısında yaygın olarak kullanılmaktadır. XUL oluşturma, kullanılarak gerçekleştirilir
[Gecko motoru](https://en.wikipedia.org/wiki/Gecko_(software)). Pale Moon, Basilisk ve Waterfox gibi Firefox çatalları, XUL eklentileri için desteği koruyor. XUL dosyaları MIME türüyle tanımlanır: application/vnd.mozilla.xul+xml.

## XUL Dosya Biçimi

XUL dosyaları, XML dosya biçimine dayalı olarak düz metin olarak yazılır ve Gecko motoru kullanılarak oluşturulur. Bir XUL yapısının üç ana bölümü şunlardır:

* `İçerik` - Bu, pencere bildirimlerini ve bunların içerdiği kullanıcı arabirimi öğelerini içerir.
* `Dış Görünüm` - Stil sayfalarını, resimleri ve temayla ilgili diğer dosyaları içerir. Bir pencerenin görünümü, stil sayfalarında açıklanmıştır.
* `Yerel Ayar` - Bir pencerede görüntülenen metin ayrı olarak saklanır ve kullanıcılar tarafından birden fazla dil dosyası seti kullanılabilir.

### XUL Örneği

Aşağıdaki örnek, dikey yönde üst üste istiflenmiş üç düğme oluşturur.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Referanslar

* [XUL - Wikipedia'dan](https://en.wikipedia.org/wiki/XUL)
* [XUL Arşivlenmiş Belgeler - Mozilla Tarafından](https://wiki.mozilla.org/XUL:Home_Page)

