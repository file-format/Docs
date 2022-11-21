{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Btrieve Veritabanı" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"BTR dosya formatı ve BTR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"BTR - Btrieve Veritabanı Dosyası",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## BTR dosyası nedir?

.btr uzantılı bir dosya, [Btrieve](https://www.actian.com/) işlem veritabanı uygulaması tarafından oluşturulan bir veritabanı dosyasıdır. İlişkisel veri tabanı yönetim sistemlerinden (RBMS) farklı olarak Btrieve, hızlı erişim için veri depolamanın bir yolu olan Dizinlenmiş Sıralı Erişim Yöntemine (ISAM) dayalıdır. BTR dosyası, bir kayıt koleksiyonunu saklar ve gereksinimlere göre raporlar oluşturmak için kullanılır. BTR dosyaları, Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility ve Legend Software BTRIEVE Viewer kullanılarak açılabilir.

## BTR Dosya Yapısı - Daha Fazla Bilgi

Bir BTR dosyasının yapısındaki her baytın dahili veri yapısı ve hizalaması halka açık değildir. Ancak, Btrieve
BTR dosyalarından bilgi okumak için kullanılabilen [Btrieve API'sini](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) sağlar. Aşağıdaki programlama dilleri ve geliştirme ortamları ile uyumludur.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Mikro Odak COBOL
*Microsoft Visual Basic
*Microsoft Visual C++
* Watcom C/C++

Bir BTR dosyasından veri alma, onunla ilişkili DDF dosyasına bağlıdır. DDF olmadan, böyle bir dosyadan bilgi almak kolay olmayacaktır.

## Referanslar

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Btreive API'lerine Giriş](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

