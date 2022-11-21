{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PET Dosya Formatı - Puppy Linux Kurulum Paketi Dosyası",
  "description":"PET dosya formatı ve PET dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Linux PET dosyası nedir?

PET dosyası, Linux İşletim Sisteminin PuppyLinux varyantı ile oluşturulan ve kullanılan bir uygulama yükleme paketi dosyasıdır. Sıkıştırılmış arşivin dosya boyutunu azaltan sıkıştırılmış bir [TGZ](/tr/compression/tgz/) dosyası olarak oluşturulur. PET dosya biçiminin bütünlüğü, uzak uçta doğrulama için dosyanın sonuna eklenen md5sum sağlama toplamı ile sağlanır. PET dosyaları, standart TGZ dosya çıkarıcı ve WinRAR kullanılarak çıkarılabilir. PET dosyaları, eski [PUP](/tr/compression/pup/) paket yükleme dosyalarının yerini almıştır.

## PET Dosya Biçimi

PET dosyaları, ikili dosya biçiminde sıkıştırılmış arşivler olarak diske kaydedilir. Ancak, PET dosya formatının dahili dosya formatı detayları bilinmemektedir. [.exe](/tr/executable/exe/) ve [.msi](/tr/executable/msi/) paket kurulum dosyalarına benzer şekilde, PET dosyaları çalıştırıldıklarında bir kurulum başlatırlar.

## Referanslar

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [PuppyLinux PET paketleri dizini](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

