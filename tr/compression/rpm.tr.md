{
  "date" : "2021-04-08",
  "keywords" :[ "rpm dosyası", "rpm dosya biçimi", "rpm dosyası nedir", "dosya", "rpm örneği", "rpm dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Red Hat Paket Yöneticisi Dosyası",
  "description":"RPM dosya formatı ve RPM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## .rpm dosyası nedir?

.rpm uzantılı bir dosya, Linux sistemlerde programların kurulumu için bir Red Hat Linux işletim sistemi paketidir. Red Hat Paket Yöneticisi, RPM dosya formatını kullanır ve ücretsiz ve açık kaynaklı bir paket yönetim sistemidir. RPM dosyaları, programların kurulumu için olduğu gibi kullanılabilse de, bunlar Alien adlı Debian programı kullanılarak [DEB](/tr/compression/deb/) gibi diğer paket biçimlerine dönüştürülebilir.

## RPM Dosya Biçimi

Bir RPM dosyası, bir dizi dosya içerebilen bir ikili dosyadır. Çoğu zaman, RPM dosyaları, yazılımın derlenmiş yürütülebilir dosyaları olan "ikili RPM'lerdir". RPM dosyası, paketi kaynak koddan oluşturmak için kullanılabilecek kaynak RPM'leri (SRPM'ler) içerebilir. RPM dosya formatı dört bölümden oluşur.

* Kurşun - Dosyayı bir RPM dosyası olarak tanımlar
* İmza - Bütünlük ve/veya orijinalliği sağlamak için kullanılabilir
* Başlık - Paket adı, sürüm, mimari, dosya listesi vb. dahil olmak üzere meta verileri içerir.
* Dosya Arşivi - Yük olarak da bilinir ve genellikle [GZIP](/tr/compression/gz/) ile sıkıştırılmış cpio biçimindedir.

## Referanslar

* [RPM - Wikipedia](https://rpm.org)
* [RPM Belgeleri](https://rpm.org/documentation.html)

