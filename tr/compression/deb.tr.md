{
  "date" : "2021-04-08",
  "keywords" :[ "deb dosyası", "deb dosyası biçimi", "deb dosyası nedir", "dosya", "deb örneği", "deb dosyası uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip Sıkıştırılmış Tar Arşivi",
  "description":"DEB dosya formatı ve DEB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## DEB dosyası nedir?

.deb uzantılı bir dosya, Linux işletim sisteminde yazılım paketlerinin dağıtımı için kullanılabilen bir Debian ikili paket dosyası biçimidir. İki [TAR](/tr/compression/tar/) arşiv dosyasından oluşur. DPKG, DEB paketlerini okuma ve kurma mekanizmasını sağlar. DEB paketleri, APT paketi yazılım yönetimi arabirimi kullanılarak kurulabilir. DEB dosyalarının İnternet Medya Türü "application/vnd.debian.binary-package" şeklindedir.

## DEB Dosya Biçimi

Bir DEB dosyası iki [TAR](/tr/compression/tar/) arşiv dosyasından oluşur. Bir arşiv kontrol bilgisini tutarken diğeri yüklenebilir verileri içerir.

### Paket Organizasyonu

DEB dosyası, `! sihirli değerine sahip bir **ar** arşiv dosyasıdır.<arch> `. Debian 0.93'ten bu yana, DEB dosyalarının arşivleme mekanizması belirli bir sırada üç dosya içerir.

1. `Debian Binary` - Yeni satırlarla ayrılmış bir dizi satıra sahip olmaya mahkumdur. Şu anda, sürüm numarasını açıklayan yalnızca tek bir satır mevcuttur. Geçerli sürüm numarası 2.0'dır.
1. `Kontrol Arşivi` - Paket adı, sürüm, bağımlılıklar ve bakımcı gibi paket hakkında bakım betikleri ve meta bilgileri içeren bir control.tar arşivi içerir.
1. `Veri Arşivi` - Bu, data.tar adlı bir tar arşividir ve gerçek kurulabilir medya dosyalarını içerir. Arşiv gz, bz2, lzma veya xz ile sıkıştırılabilir ve veri arşivinin dosya uzantısı buna göre değişir.

### Denetim Arşivi

Kontrol arşivi aşağıdaki içerikleri içerebilir.

* `kontrol` - Paketin kısa bir açıklamasını ve bağımlılıkları gibi diğer bilgileri içerir.
* `md5sums` - Bozuk veya eksik dosyaları tespit etmek için paketteki tüm dosyaların MD5 sağlama toplamlarını içerir.
* `conffiles` - Yapılandırma dosyaları olarak değerlendirilmesi gereken paketin dosyalarını listeler. Belirtilmediği sürece bir güncelleme sırasında yapılandırma dosyalarının üzerine yazılmaz.
* `preinst`, postinst, prerm ve postrm - Paketi yüklemeden veya kaldırmadan önce veya sonra yürütülen isteğe bağlı komut dosyaları
* `config`, debconf yapılandırma mekanizmasını destekleyen isteğe bağlı bir komut dosyasıdır.
* `shlibs` - Paylaşılan kütüphane bağımlılıklarının bir listesidir.

## Referanslar

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Debian ikili paket formatı](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

