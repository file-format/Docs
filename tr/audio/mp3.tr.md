{
  "date" : "2019-12-13",
  "keywords" :[ "MP3", "dosya", "uzantı", "biçim", "Ses", "MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MP3 dosya formatı ve MP3 dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "title" :"MP3 - Ses Dosyası Biçimi",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2020-09-04"
}

## MP3 dosyası nedir?

.mp3 uzantılı dosyalar, resmi olarak MPEG-1 Ses Katmanı III veya MPEG-2 Ses Katmanı III'ü temel alan ses dosyaları için dijital olarak kodlanmış dosya biçimleridir. Layer 3 ses sıkıştırmasını kullanan Hareketli Resim Uzmanları Grubu (MPEG) tarafından geliştirilmiştir. MP3 dosya biçimiyle elde edilen sıkıştırma, .WAV veya .AIF dosyalarının boyutunun 1/10'u kadardır. Biçim, ses dosyalarının büyük dosya boyutları nedeniyle daha önce mümkün olmayan, çevrimiçi dinlemek için bu tür ses dosyalarının internet üzerinden akışının avantajlarını sağlar. Bir MP3 ses dosyasının ses kalitesi, bit hızı, örnekleme hızı, birleşik veya normal stereo gibi parametre ayarlarıyla kontrol edilebilir.

## MP3 Dosya Formatının Kısa Tarihi

MP3 formatı bir Alman Şirketi olan Fraunhofer-Gesellshart tarafından icat edildi ve geliştirildi. Algoritma, kullandığı sıkıştırma teknolojisi için lisanslı patentlere sahiptir. İşte kullanışlı bir MP3 zaman çizelgesi:

• **1987** - Almanya'daki Fraunhofer Enstitüsü, yüksek kaliteli, düşük bit hızlı ses kodlamasını araştırmaya başladı. EUREKA projesi EU147, Dijital Ses Yayını olarak adlandırıldı.

• **Ocak 1988** - Hareketli Görüntü Uzmanları Grubu veya MPEG kuruldu.

• **Nisan 1989** - Fraunhofer, MP3 için Almanya'da bir patent aldı.

• **1992** - Araştırmasında Fraunhofer'a yardımcı olan Dieter Seitzer, ses kodlamasını MPEG-1 ile entegre etti.

• **1993** - MPEG-1 standardı yayınlandı.

• **1994** - MPEG-2 standardı geliştirildi ve bir yıl sonra yayınlandı.

• **Kasım 26, 1996** - MP3 için ABD patenti verildi.

• **Eylül 1998** - Fraunhofer patent haklarını uygulamaya başladı. MP3 ses kodlamasını kim kullandıysa, Fraunhofer'a bir lisans ücreti ödedi.

• **Şubat 1999** - Bir kayıt şirketi olan SubPop, müziği MP3 formatında dağıttı ve bunu yapan ilk şirket oldu.

• **1999** - İlk taşınabilir MP3 oynatıcılar ortaya çıktı.

## MP3 Dosya Biçimi

Bir MP3 dosyası, her çerçevenin bir başlık ve bir veri bloğundan oluştuğu MP3 çerçevelerinden oluşur. Çerçeveler bağımsız değildir ve genellikle keyfi çerçeve sınırlarında çıkarılamaz. Dosyanın veri blokları, frekanslar ve genlikler açısından ses hakkında bilgi içerir. Başlıktaki senkronizasyon sözcüğü, geçerli bir çerçevenin başlangıcını tanımlar. Bunu 3 bit takip eder, burada ilk bit bunun bir MPEG standardı olduğunu gösterir ve kalan 2 bit katman 3'ün kullanıldığını gösterir; dolayısıyla MPEG-1 Ses Katmanı 3 veya MP3. Bundan sonra, MP3 dosyasına bağlı olarak değerler değişecektir.

[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3, belgenin her bölümü için değer aralığını tanımlar. başlığın özelliği ile birlikte başlık. Günümüzde çoğu MP3 dosyası, MP3 çerçevelerinden önce veya sonra gelen [ID3](https://en.wikipedia.org/wiki/ID3) [metadata](https://en.wikipedia.org/wiki/Metadata) içerir, diyagramda belirtildiği gibi. Veri akışı isteğe bağlı bir sağlama toplamı içerebilir.

## Referanslar ##

* [MP3 - Wikipedia'dan](https://en.wikipedia.org/wiki/MP3)

