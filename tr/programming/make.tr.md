{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Dosya Yap - Xcode Makefile Komut Dosyası",
  "description":"XCode MakeFile Biçimi ve MakeFile dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## .MAK dosyası nedir?

Bir MAKE dosyası, kod derlemesini düzenleyen bir XCode betik dosyasıdır. Birden fazla kaynak kod dosyasından programları derlemek ve bağlamak için kullanılır. Bu, uygulamanın güncellenmesi gerektiğinde büyük bir uygulamanın hangi bölümlerinin yeniden derlenmesi gerektiğine karar verilmesine yardımcı olur. Dosyaların, hangi dosyaların değiştiğine bağlı olarak çalıştırmak için bir dizi talimat kullanmasını sağlayın.

## MAKE Dosya Biçimi Örneği

Aşağıdaki içerikler Make programı kullanılarak yürütülür ve çıktılar aşağıdaki gibidir.

```
hello:
	echo "hello world"
```
**Çıktı Yap**

```
$ make
echo "hello world"
hello world
```

## Referanslar
* [XCode ve Make - Apple Forumları](https://developer.apple.com/forums/thread/657458)
* [Object-C Kılavuzu](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

