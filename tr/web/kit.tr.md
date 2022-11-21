{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"KIT dosya formatı ve KIT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"KIT Dosya Biçimi - CodeKit Dosyası",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## .kit dosyası nedir?

.kit uzantılı bir dosya, [CodeKit](https://codekitapp.com/) programlama dili uygulamasıyla oluşturulan bir HTML dosyasıdır. Mevcut [HTML](/tr/web/html/) dosyalarına ek olarak "içe aktarmalar" ve "değişkenler" içerir, bu da onu statik siteler için ideal kılar. CodeKit, KIT dosyalarını statik web sitesi dosyaları olarak kolayca kullanılabilen HTML'de derler.

## KİT Dosya Biçimi

KIT dosyaları, ek olarak içe aktarmaları ve değişkenleri içeren HTML dosyalarıdır. Bunlar düz metin dosyaları olarak saklanır ve herhangi bir metin düzenleyici veya web dosyası düzenleyici ile açılabilir.

### KIT Dosyası İçe Aktarımı

Hemen hemen her tür dosya bir Kit dosyasına alınabilir. Dosyaları bir .kit dosyasına aktarmak için kullanılan içe aktarma söz dizimi aşağıdadır.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Bir KIT dosyasına bir içe aktarma eklendiğinde ve kaydedildiğinde, içe aktarılmakta olan dosyanın metniyle değiştirilir. @import yerine @include kullanabilirsiniz.

### Bir KIT dosyasında Çoklu İçe Aktarma

Ayrıca, virgülle ayrılmış bir liste kullanarak aynı anda birden fazla dosya içe aktarabilirsiniz:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Referanslar

* [Kit Nedir?](https://codekitapp.com/help/kit/)

