{
  "date" : "2021-08-30",
  "keywords" :[ "ipa dosyası", "ipa dosya biçimi", "ipa dosyası nedir", "dosya", "ipa örneği", "ipa dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"IPA dosya formatı ve IPA dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"IPA - iOS Uygulama Paket Dosyası",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## IPA dosyası nedir?
.ipa uzantılı bir dosya, iOS'a aittir ve uygulama paket dosyası olarak bilinir. Bu, bir iOS uygulamasını depolayan bir arşiv ([ZIP](/tr/compression/zip/) sıkıştırması kullanılarak sıkıştırılmış) dosyasıdır, ancak bu uygulama yalnızca iPad, iPhone veya iPad, iPhone gibi bir iOS veya ARM tabanlı MacOS cihazlarına yüklenebilir. ipod touch. Temel olarak, IPA dosyalarını yüklemek için iTunes, Apple Configurator 2 veya herhangi bir üçüncü taraf yazılımı kullanılabilir.

## IPA dosya biçimi
Apple Xcode'u kullanarak uygulamaları geliştiren IOS geliştiricileri, IPA dosyalarına aşinadır çünkü gelişmiş uygulamalarını, uygulama mağazası dağıtım amaçlarının test edilmesi için IPA dosyaları olarak paketlemeleri gerekir. IPA dosyalarının iOS uygulamaları olarak yüklendiği bilinmesine rağmen, içerdiği uygulama verilerini görüntülemek için bunları da açabilirsiniz. Bir IPA dosyası, cep telefonlarının ARM mimarisi için yalnızca bir ikili dosya içerdiğinden ve x86 mimarisi için bir ikili dosya içermediğinden, birçok .ipa dosyası iPhone Simülatörüne yüklenemez.
### Bir .ipa dosyasının yapısı
Aşağıdaki örnek, bir IPA'nın yapısını göstermektedir:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Yukarıdaki, iTunes ve App Store'un tanıması için yerleşik bir yapıdır. Bu yapıya göre:
- Yük dizini tüm uygulama verilerini içerir.
- iTunes Artwork dosyası, iTunes'da ve iPad'deki App Store uygulamasında gösterilmek üzere uygulamanın simgesini içeren 512×512 piksellik bir PNG görüntüsüdür.
- iTunesMetadata.plist, geliştiricinin adı ve kimliği, telif hakkı bilgileri, paket tanımlayıcısı, uygulamanın adı, tür, çıkış tarihi, satın alma tarihi vb. gibi çeşitli bilgi parçalarını içerir.
- META-INF klasörü, yalnızca IPA'yı oluşturmak için hangi programın kullanıldığına ilişkin meta verileri içerir.


## Referanslar

* [.ipa - Wikipedia'dan](https://en.wikipedia.org/wiki/.ipa)


