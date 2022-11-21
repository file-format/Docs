{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"PCL dosya formatı ve PCL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## PCL dosyası nedir? ##

PCL, Hewlett Packard (HP) tarafından sunulan bir Sayfa Açıklama Dili olan Yazıcı Komut Dili anlamına gelir. HP, birçok farklı yazdırma aygıtında yazıcı özelliklerini kontrol etmenin verimli bir yolunu sağlamak için PCL'yi yarattı. Biçim başlangıçta HP'nin nokta vuruşlu ve Inkjet yazıcıları için geliştirildi, ancak zaman geçtikçe çeşitli termal, matris ve sayfa yazıcılarının bir parçası oldu. Format birkaç farklı revizyondan geçti ve her versiyonun yazıcı kontrol özelliklerine göre zamanın taleplerini karşılayacak şekilde geliştirildiği farklı versiyonlarla sonuçlandı. Bugün PCL, son yazıcı pazarında en yaygın kullanılan yazıcı dilidir.

## PCL Sürümleri ##

PCL sürümleri işlevsellik açısından farklılık gösterir (örneğin, yazı tipi türü desteği: bitmap yazı tipleri, ölçeklenebilir yazı tipleri (Intellifonts, TrueType yazı tipleri), raster grafik sıkıştırma yöntemleri, HP-GL/2 grafik desteği).

**PCL 1:** 1980 civarında - Yazdırma ve Alan işlevi, basit, kullanışlı, tek kullanıcılı iş istasyonu çıktısı için sağlanan temel işlevler kümesidir.

**PCL 2:** 1980 civarında - EDP (Elektronik Veri İşleme)/İşlem işlevi, PCL 1'in bir üst kümesidir. Genel amaçlı, çok kullanıcılı sistem yazdırma için işlevler eklendi.

**PCL 3**: 1984 - Office Kelime İşleme işlevi, PCL 2'nin bir üst kümesidir. Yüksek kaliteli ofis belgesi üretimi ve 300 dpi'ye kadar artan dpi için işlevler eklendi. Sınırlı sayıda bit eşlemli yazı tipi ve grafiğin kullanımına izin verdi ve HP-GL'yi destekledi. PCL 3, diğer yazıcı üreticileri tarafından geniş çapta taklit edildi ve bu şirketler tarafından "LaserJet Plus Öykünmesi" olarak anıldı.
(Yazıcılar: HP DeskJet ailesi, HP LaserJet serisi yazıcı, HP LaserJet Plus serisi yazıcı)

**PCL3+:** DeskJet ve DesignJet yazıcı ailesi tarafından kullanılır.

**PCL3c:** DeskJet ve DesignJet yazıcı ailesi tarafından kullanılır.

**PCL3e**: DeskJet ve DesignJet yazıcı ailesi tarafından kullanılır. Artık PhotoSmart'ta da kullanılıyor.

**PCL3GUI**: RTL kullanır ve DeskJet ve DesignJet yazıcı ailesi tarafından kullanılır.

**PCLSLEEK**: RTL'yi kullanır ve DeskJet ve DesignJet yazıcı ailesi tarafından kullanılır.

**PCL 4**: 1985 - Sayfa biçimlendirme işlevi, PCL 3'ün bir üst kümesidir. Desteklenen makrolar, daha büyük bit eşlemli yazı tipleri ve grafikler. (Yazıcılar: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing işlevi, PCL 4'ün bir üst kümesidir. Yeni yayımlama yetenekleri, yazı tipi ölçeklendirmeyi ve HP-GL/2 (vektör) grafiklerini içerir. (Yazıcılar: HP LaserJet III)

**PCL 5e:** 1994 - Bu, Uyarlanabilir Sıkıştırma Sistemi, 2 bayt karakter kodlama, vektör yazı tipleri desteği ve çift yönlü yapılandırma komutları gibi yeni özellikleri içeren büyük bir revizyondur. Yolları kırpmadan önce Windows desteğini iyileştirmek için Mantıksal İşlemler (GDI ROP'lara karşılık gelir) içerir. (Yazıcılar: HP LaserJet 4)

**PCL 5j:** Japonca yerleşik ölçeklenebilir yazı tipleri, dikey yazı, Japonca kağıt boyutları ve yazı tipi dizileri için 2 baytlık karakter desteği gibi yeni özellikler. (Yazıcılar: HP LaserJet 4PJ)

**PCL 5c:** 1995 - PCL5'e renk desteği ve Mantıksal İşlemler eklendi. PCL5c, PCL5e'den önce gelir. Bazı modeller ayrıca kırpma yollarını da destekler. (Yazıcılar: HP Color LaserJet, HP PaintJet 300 XL (PCL5c içeren ilk yazıcı), HP DeskJet 1200C/1600C (bu model numaraları yeniden kullanılmıştır ve daha yeni modeller PCL 5c değildir)

**PCL 5ce:** Agfa Microtype ölçeklenebilir yazı karakterlerini destekler. (Yazıcılar: HP 2500c Pro Yazıcı)

**PCL 6 / XL:** 1996 - PCL 6 veya PCL XL, 1995'te tanıtılan ve PCL'nin önceki sürümleriyle uyumlu olmayan yeni bir biçimdir. (Yazıcılar: HP LaserJet 5, 5M ve 5N)

## PCL 6'ya Genel Bakış ##

HP, PCL dilinin ve ilgili teknolojilerin bir sonraki evrimi olan PCL 6'yı 1996'da tanıttı. Aşağıdaki bileşenlere sahiptir:

**PCL 6 Enhanced:** MS Windows ve OS/2 gibi grafik kullanıcı arabirimlerinden (GUI'ler) yazdırmak için optimize edilmiş sürüm sağlar

**PCL 6 Standardı:** eski HP LaserJet yazıcılarla tam geriye dönük uyumluluk sağlar

**PCL Yazı Tipi Sentezi:** ölçeklenebilir yazı tipleri, yazı tipi yönetimi ve formlar ile yazı tiplerinin depolanmasını sağlar.

Genişletilmiş sürüm PCL XL, birçok uygulamanın kullandığı GDI'ya daha yakındır. Gelişmiş sürücü tarafından uygulanan kaçışları destekleyen uygulamalarla artan WYSIWYG yetenekleri ve daha iyi performansla sonuçlanan daha az çeviri yapılmasını sağlar. Enhanced (PCL XL) sürücüsünün çıktısı, Standart sürücünün çıktısıyla aynı olmayabilir. Çıktı beklendiği gibi değilse bunun yerine Standart (PCL5e) sürücüyü seçin.

PCL 6 Gelişmiş komutları, GUI tabanlı uygulamalar için grafik yazdırma gereksinimlerini en iyi şekilde karşılayacak şekilde tasarlanmıştır. Çoğu durumda, bir GUI'nin gerçekleştirmek istediği her grafik yazdırma komutu için eşleşen bir PCL 6 Enhanced komutu vardır. Bu, bir grafik sayfasını tanımlamak için gereken komut sayısını azaltır. PCL 6 Enhanced'deki her komut, ana bilgisayardan yazıcıya minimum veri aktarımı gerektirecek şekilde tasarlanmıştır. Bu, bir sayfayı tanımlamak için gereken veri miktarını azaltır.

Çoğu HP LaserJet yazıcı için Windows Yazdırma Sistemi iki ayrı sürücü sağlar: Standart ve Gelişmiş. Standart sürücü, basit metin veya karışık metin ve grafik sayfaları yazdırmak için PCL 6 Standard (PCL5e) komutlarını kullanarak geriye dönük uyumluluk sağlar. Enhanced sürücüsü, karmaşık grafik sayfaları yazdırmak için optimize edilmiş PCL 6 Enhanced komutlarını kullanır.

## PCL 6 Sınıf Revizyonları ##

#### Sınıf 1.1 ####

**Çizim araçları:** Çizim çizgileri, yaylar/elipsler/akorlar, (yuvarlanmış) dikdörtgenler, çokgenler, Bezier yolları, kırpılmış yollar, tarama görüntüleri, tarama çizgileri, tarama işlemleri desteği.
**Renk işleme:** 1/4/8 bit paletleri, RGB/gri renk alanını destekler. Özel noktalı resim desenlerini destekleyin (maksimum 256 desen).
**Sıkıştırma:** RLE'yi destekler.
**Ölçü birimleri:** İnç, milimetre, milimetrenin onda biri.
**Kağıt kullanımı:** Genel Letter, Legal, A4 vb. dahil olmak üzere özel veya önceden tanımlanmış kağıt türü gruplarını destekler. Elle besleme, tepsiler, kasetler arasından kağıt seçebilir. Kağıt yatay veya dikey olarak duplekslenebilir. Kağıt dikey, yatay veya önceki ikisinin 180 derece dönüşünde yönlendirilebilir.
**Yazı Tipi:** Bitmap veya TrueType yazı tiplerini, 8 veya 16 bit kod noktalarını destekler. Karakter setinin seçilmesi, PCL 5'ten farklı sembol seti kodu kullanır. Bitmap yazı tipi kullanıldığında, birçok ölçeklendirme komutu kullanılamaz. TrueType yazı tipi kullanıldığında, değişken uzunluklu tanımlayıcılar, devam blokları desteklenmez. Anahat yazı tipi döndürülebilir, ölçeklenebilir veya kırpılabilir.

#### Sınıf 2.0 ####

**Sıkıştırma:** JetReady adlı tescilli bir JPEG sıkıştırması eklendi.
**Kağıt kullanımı:** Ortam, farklı çıkış bölmelerine (en fazla 256) yönlendirilebilir. A6 ve Japonca B6 ön ayarlı medya boyutları eklendi. Üçüncü kaset ön ayarı, 248 harici tepsi ortam kaynağı eklendi.
**Yazı Tipi:** Metin dikey olarak yazılabilir.

#### Sınıf 2.1 ####

**Renk işleme:** Renk eşleştirme özelliği eklendi.
**Sıkıştırma:** Delta Satırı eklendi.
**Kağıt kullanımı:** Yeni bir sayfa bildirilirken yön ve ortam boyutu isteğe bağlıdır. B5, JIS 8K, JIS 16K, JIS Exec kağıt türleri eklendi.

#### Sınıf 3.0 ####

**Renk işleme:** Vektör veya raster grafikler, metin için farklı yarım ton ayarlarının kullanılmasına izin verin. Uyarlanabilir yarım tonlamayı destekler.
**Protokol:** PCL geçişini destekler ve PCL 5 özelliklerinin PCL 6 akışları tarafından kullanılmasına izin verir. Ancak, bu özellik kullanılırken bazı PCL 6 durumları korunmaz.
**Yazı Tipi:** PCL yazı tiplerini destekler.
**Görüntüleyici/Dönüştürücü:** PCLReader (ücretsiz yazılım), herhangi bir düzeyde PCL 6'yı (JetReady dahil) herhangi bir yazıcıda görüntüleyebilir, dönüştürebilir veya yazdırabilir.

## Referanslar ##

* [PCL - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Printer_Command_Language)

