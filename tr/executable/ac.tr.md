{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "AC dosya formatı ve ACCDB dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" : "AC Dosya Formatı - Autoconf Komut Dosyası",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-tr",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## AC dosyası nedir?

AC dosyası Autoconf komut dosyasıdır. **Autoconf**, yazılım kaynak kodu paketlerini otomatik olarak yapılandırmak için kabuk komut dosyaları üreten, genişletilebilir bir M4 makro paketidir. Bu betikler, manuel kullanıcı müdahalesine gerek kalmadan paketleri birçok UNIX benzeri sistem türüne uyarlayabilir. Autoconf, paketin kullanabileceği işletim sistemi özelliklerini M4 makro çağrıları biçiminde listeleyen bir şablon dosyasından bir paket için bir yapılandırma komut dosyası oluşturur.

Producing configuration scripts using Autoconf requires GNU M4. Autoconf'u yapılandırmadan önce GNU M4'ü (en az sürüm 1.4.6, ancak 1.4.13 veya üstü önerilir) yüklemelisiniz, böylece Autoconf'un yapılandırma betiği onu bulabilir. Autoconf tarafından üretilen yapılandırma komut dosyaları bağımsızdır, dolayısıyla kullanıcılarının Autoconf'a (veya GNU M4) sahip olması gerekmez.

## AC dosyası nasıl açılır?

AC, Otomatik Yapılandırma anlamına gelir. Paketteki gerekli özellikleri test ederek yazılım kaynak kodunun çeşitli Posix benzeri sistemlere uyarlanmasını sağlayan, GNU Autoconf tarafından oluşturulan bir komut dosyasıdır. Komut dosyasına AC dosyası denir.

## Başlıca Autotools Bileşenleri

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools, birlikte kullanıldığında taşınabilir yazılım oluşturmanın getirdiği zorlukların çoğunu ortadan kaldıran ilgili paketlerin bir koleksiyonudur. Bu araçlar, nispeten basit, yukarı yönde sağlanan birkaç girdi dosyasıyla birlikte, bir paket için derleme sistemi oluşturmak için kullanılır.

**Ana otomatik aletler bileşenlerinin birbirine nasıl uyduğuna dair temel bir genel bakış.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Basit bir kurulumda:

- 'autoconf' programı, 'configure.in' veya 'configure.ac'dan bir yapılandırma komut dosyası üretir.
- 'automake' programı Makefile.am dosyasından Makefile.in dosyasını üretir.
- 'configure' betiği, Makefile.in dosyalarından bir veya daha fazla Makefile dosyası oluşturmak için çalıştırılır.
- 'Make' programı, programı derlemek için Makefile dosyasını kullanır.

## Referanslar
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Autotools'un Temelleri](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



