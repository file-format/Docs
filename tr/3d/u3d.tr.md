{
  "date" : "2019-10-11",
  "keywords" :[ "u3d dosyası", "u3d dosya biçimi", "u3d dosyası nedir", "dosya", "u3d örneği", "u3d dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Evrensel 3D Dosya Formatı",
  "description":"U3D dosya formatı ve U3D dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## U3D dosyası nedir?

**U3D** (Universal 3D), 3D bilgisayar grafikleri için sıkıştırılmış bir dosya formatı ve veri yapısıdır. Üçgen kafesler, aydınlatma, gölgeleme, hareket verileri, çizgiler ve noktalar gibi renk ve yapıya sahip 3B model bilgilerini içerir. Biçim, Ağustos 2005'te [ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) standardı olarak kabul edildi. 3D [PDF](/tr/pdf/) belgeleri U3D'yi destekler nesneler gömülür ve Adobe Reader'da (sürüm 7 ve sonrası) görüntülenebilir.

U3D formatı, üç boyutlu veri depolama ve alışverişi için evrensel bir standart oluşturma amacı göz önünde bulundurularak geliştirilmiştir. Bununla birlikte, format, bir değişim formatı olarak kullanılmaktansa, asıl kullanımını 3D PDF için kodlamada bulur. Acrobat 3D, desteklenen bir 3D dosya türünü PDF'ye dönüştürdükten sonra U3D'ye veya PRC'ye dönüştürür.

## U3D Dosya Biçimi

U3D dosyaları, [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) referans belgesinde açıklandığı gibi dört sürümden geçen ikili dosya biçimindedir ve bu, teknik özelliklerin güncellenmesine neden olur her sürümde. PDF dosya standardı ISO-32000, izin verilen açıklama ve multimedya türü olarak U3D'yi kabul eder.

U3D'nin ilk sürümü, geometri, renk, dokular, aydınlatma, eklemler ve dönüşüm tabanlı animasyon gibi 3B grafik özelliklerinin temel temsillerine odaklanmıştı. İkinci ve üçüncü baskılar, ilk baskıdaki bazı hataları düzeltti ve üçüncü versiyon, endüstri yazılımında en yaygın kullanılan türdü. Dördüncü baskı, üst düzey ilkel öğeler (eğri yüzeyler) için tanımlar sağlar. [U3D belirtimleri](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/), ECMA web sitesinde kullanıcı referansı için çevrimiçi olarak mevcuttur.

### U3D dosyalarındaki Veri Türleri

İkili dosya şu türleri içerecektir: U8, U16, U32, U64, I16, I32, F32, F64 ve String.

* U8 : İşaretsiz 8 bitlik bir tamsayı
* U16 : İşaretsiz 16 bit tamsayı
* U32 : İşaretsiz 32 bit tamsayı
* U64 : İşaretsiz 64 bit tamsayı
* I16 : İşaretli 16 bit tamsayı
* F32: Bir IEEE tek duyarlıklı kayan nokta.
* F64: Bir IEEE çift duyarlıklı kayan nokta.
* Dize: Bir U3D dosyasındaki dizeler, dizideki karakterlerin toplam uzunluğunu tanımlayan işaretsiz 16 bitlik bir tamsayı ile başlar. Dizeler her zaman büyük/küçük harfe duyarlı olarak işlenir.

## U3D Dosya Yapısı

Bir U3D dosyası bir dizi blok içerir. Her U3D dosyasında 3 farklı blok türü vardır.

* Dosya Başlığı Bloğu
* Beyanname Bloğu
* Devam Bloğu

Yükleyici, o bloktaki veri gerekli değilse veya o blok türü için bir kod çözücü yoksa, bir bloğun sonunu belirler.

{{< figure src="../u3d.png" alt="U3D Dosya Biçimi" >}}

### Dosya Başlığı bloğu
Bir dosya başlık bloğu, dosyanın nasıl okunacağını belirlemek için yüklenen tarafından kullanılan dosya bilgilerini içerir.

### Beyan Bloğu

Bildirim blokları, dosyadaki nesneler hakkında bilgi içerir. Bir bildirim bloğundaki nesneler tanımlanmalıdır.

### Devam Bloğu

Bir Bildirim bloğunda bildirilen nesneler için ek bilgiler, devam bloğunda sağlanır. Her Devam Bloğu bir Bildirim Bloğu ile ilişkilendirilmelidir.


## Referanslar ##

* [U3D Dosya Biçimi - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [ECMA U3D Dosya Biçimi Özellikleri](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

