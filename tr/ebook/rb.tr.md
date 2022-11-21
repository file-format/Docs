{
  "date" : "2021-03-08",
  "keywords" :["RB", "Nuvo Media's Rocket eKitap cihazı", "dosya", "uzantı", "biçim", "eKitap"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Nuvo Media'nın Rocket eBook cihazı için RB dosya formatı ve RB dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"RB - Rocket eKitap Dosyası",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Bir RB dosyası nedir?

.rb uzantılı dosya, Rocket e-Kitap içeriğini tutar. Rocket e-Kitabı aslında Nuvo Media tarafından yapılmış bir cihazdır; bu cihazı 1998'de piyasaya sürdüler. Rocket eBook görüntüleri gösterebilse de, yalnızca siyah beyaz ekranda. 4,5 x 3 inç dokunmatik ekranda 106 dpi veya 480 x 320 piksel ekrana sahiptir. Rocket e-Kitabı, e-Kitapları RB dosya formatında indirmek için bir seri port bağlantısı aracılığıyla bir bilgisayara bağlanır. RB dosyaları DRM'yi kullanabilir ancak bu teknoloji modern e-Kitaplarda kullanılmamaktadır. RB dosyası geleneksel olarak görüntüleri içeren bir HTML dosyası ve tüm meta verileri (.info) içeren bir sözde OPF dosyası içerir.

## RB Dosya Formatının Teknik Özellikleri ##

Dosyanın ilk 4 baytında sihirli bir sayı (onaltılık olarak) görünür: B0 0C B0 0C.

Sonraki iki baytın, ana sürüm 2 ve küçük sürüm 0'ı temsil eden "02 00" gibi bir sürüm numarası olduğu anlaşılıyor.

Sonraki dört bayt "NUVO" metnini ve ardından 4 bayt 00h içerir.

Sonraki 4 bayt, kitabın oluşturulduğu tarihtir ve int16 olarak kodlanmıştır. Bu bizi 0Eh ofsetine koyar. ORocketLibrary'nin eski versiyonu yılın tam değerini kodluyordu (yani 1999 "CF 07", 2000 "D0 07" idi). Son sürümde, tm_year kelimesi kelimesine depolanır, yani 2000 yılı için 100 ("64 00"). Yıldan sonra 1-bağlı ay sayısını temsil eden bir int8 ve ayın gününü temsil eden bir int8 gelir.

Sonraki 6 bayt 00h'dir. Zaman ayarı için bunlar rezerve edilebilir.

"İçindekiler Tablosu"nun mutlak ofseti, 18h ofsetinde bir int32'de bulunur.

Bundan sonra .rb dosyasının uzunluğunu içeren bir int32 gelir. Bu, dosyaların eksiksiz olup olmadığını belirlemek için kullanılır.

Tüm bu bayt yığınına (20h ila 128h) yalnızca şifrelenmiş bir başlık için ihtiyaç duyuluyor gibi görünüyor. Şifrelenmemiş başlıklarda her zaman sıfırdır.

Çoğu durumda, içindekiler tablosu bunu takip eder (128'den sapmayla). İçindekiler'deki "sayfa" girişlerinin (.rb dosyası bölümleri) int32 sayısıyla başlar. Her giriş bir addan (32 bayta sıfırla doldurulmuş), ardından 3 int32'den oluşur: veri bölümünün uzunluğu, .rb dosyasındaki konum ve bu girdi için bir işaret. Bugün itibariyle bilinen değerler: 1 (şifreli), 2 (bilgi sayfası) ve 8 (sönük). Adların tümü, benzersiz olmalarını sağlamak için gerektiği gibi uyarlanmıştır.

## Referanslar

* [E-Okuyucu - MobileRead Tarafından](https://en.wikipedia.org/wiki/E-reader)

