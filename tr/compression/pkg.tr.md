{
  "date" : "2021-04-08",
  "keywords" :[ "pkg dosyası", "pkg dosya biçimi", "pkg dosyası nedir", "dosya", "pkg örneği", "pkg dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Genişletilebilir Arşiv Dosyası Formatı",
  "description":"PKG dosya formatı ve PKG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## PKG dosyası nedir?

.pkg uzantılı bir dosya, macOS'ta yazılım yüklemek için kullanılan bir yükleyici paket dosyasıdır. Macintosh bilgisayarların yanı sıra iPhone'da da kullanılmaktadır. Yerleşik Apple yükleyici uygulaması, bir PKG dosyasının içeriğini yüklemek için kullanılabilir. Bir PKG dosyası, yazılımın yüklenmesi için Windows İşletim Sisteminde kullanılan bir MSI dosyasına benzer. Yükleme sırasında, bu paket dosyaları, bu paket tarafından yüklenen ekstra şeyler hakkında size bir fikir veren mesajları günlüğe kaydedebilir.

## PKG Dosya Biçimi

PKR, genel dosya boyutunu azaltmak için sıkıştırılan ikili dosyalardır. OSX 10.5'ten bu yana, Apple tarafından tek yükleyici dosyalarına sahip düz paketler tanıtıldı. Bunlar, tek dosyalar yerine paketler halinde gelen önceki paketleme biçimlerinden farklıdır. Bu paketlenmiş paketler, dosyaları bazı dizin dosyaları yoluyla alınmalarını kolaylaştıracak şekilde depolayan yapılandırılmış bir dizin hiyerarşisi içeriyordu. Düz PKG dosya formatı aslında aşağıdakileri içeren bir [XAR](/tr/compression/xar/) arşividir:

* Başlık - Boyut, sağlama toplamı ve sürüm bilgilerini tanımlar
* İçindekiler - UTF-8 olarak kodlanmış (ve olması gereken) ve dosyanın başında saklanan bir XML belgesi, tek tek dosyaları ayıklamak için arşivi taramayı kolaylaştırır
* Yığın - TOC tarafından başvurulan yapılandırılmamış veri yığını

## Referanslar

* [Düz Paket Dosya Biçimi](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

