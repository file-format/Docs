{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "dosya", "uzantı", "format", "cda dosyası nedir", "müzik", "cda dosya formatı", "cda dosya formatı belirtimi"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"CDA dosya formatı ve CDA dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"CDA - CD Audio Parça Kısayol Dosyası",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## CDA dosyası nedir?

.cda uzantılı bir dosya, bir ses CD'sindeki her bir ses parçası için Microsoft Windows tarafından oluşturulan küçük bir saplama dosyasıdır. Bu dosyalar, parça süreleri gibi tipik bilgiler ve kullanıcıların belirli ses parçalarına erişmesini sağlayan bir Windows kısayolu içerir. CDA dosyaları müzik değildir, ancak depoda bir yerde bulunan bir müzik dosyasına işaret ederler. Bir CD'de yer alan bir ses dosyasının kısayolu diyebiliriz.

## CDA Dosya Biçimi

CDA dosya formatı, bir bilgisayara bir CD'de hangi ses dosyasının çalınacağını söylemek için kullanılır. Böylece, CDA dosyaları temsil ettikleri bir CD'den ayrıldıklarında işe yaramaz hale gelirler. CDA dosyaları genellikle RIFF kaynakları olarak kabul edilir. .cda dosyasının geçerli sürümünde "CDDA" adlı ve "FMT" adlı yalnızca bir veri bloğu içeren yalnızca bir yığın vardır. Bu blok 24 bayt uzunluğundadır. Windows tarafından oluşturulan tanımlayıcı, Windows 95 ve Windows 98 ile ilgili CD sürücüsü tarafından kullanılır ve oynatıcısı FreeDB veya CDDB'ye bağlanamaz. Şarkı adını ve sanatçı adını görüntüleyebilmesi için bu bilgileri cdplayer.ini dosyasına manuel olarak girmeniz gerekir.

### Bir CDA dosyasının organizasyonu

Aşağıdaki tablo, tipik ofsetlerle ilgili bilgileri gösterir:
| ofset | uzunluk | içerik |
---|---|---|
| 0x00 | 4 | 4 ASCII karakteri "RIFF" |
| 0x04 | 4 | aşağıdaki öbeğin boyutu: her zaman 36 (44 - 8), 4 baytta (Intel siparişi) |
| 0x08 | 4 | öbek tanımlayıcısı: 4 ASCII karakteri "CDDA" |
| 0x0C | 4 | 3 ASCII karakteri "fmt" ve ardından bir boşluk |
| 0x10 | 4 | yığın uzunluğu: her zaman 24, 4 baytta (Intel siparişi) |
| 0x14 | 2 | CD formatının versiyonu, 2 bayt (Intel siparişi). Mayıs 2006'da her zaman 1'e eşittir. |
| 0x016 | 2 | aralığın numarası, 2 bayt (Intel siparişi). İlk parçanın numarası 1'dir. |
| 0x18 | 4 | cdplayer.exe için Windows tarafından hesaplanan tanımlayıcı. |
| 0x1c | 4 | çerçeve sayısı olarak aralık ofseti (Intel siparişi) |
| 0x20 | 4 | parçanın süresi, toplam çerçeve sayısı (Intel siparişi) |
| 0x24 | 1 | aralık konumu: çerçeveler |
| 0x25 | 1 | aralık konumu: saniye |
| 0x26 | 1 | aralık konumu: dakika |
| 0x27 | 1 | boş bayt (ikili değer 0) |
| 0x28 | 1 | parkurun süresi: çerçeveler |
| 0x29 | 1 | parçanın süresi: saniye |
| 0x2a | 1 | parkurun süresi: dakika |
| 0x2b | 1 | boş bayt (ikili değer 0) |

## Referanslar

* [.cda dosyası - Wikipedia tarafından](https://en.wikipedia.org/wiki/.cda_file)

