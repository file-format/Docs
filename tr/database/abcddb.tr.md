{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "ABCDDB dosya formatı ve ABCDDB dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "title" : "ABCDDB Dosya Formatı - Apple Adres Defteri Kişi Listesi Veritabanı Dosyası",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-tr",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## ABCDDB dosyası nedir?

**.ABCDDB** uzantılı dosya, Apple Adres Defteri Kişi Listesi Veritabanı anlamına gelir. Yaygın olarak **Kişiler** olarak da bilinen **Adres Defteri** uygulamasına aittir. Yerleşik bir uygulamadır ve iOS ve macOS işletim sistemlerine dahildir. Kişiler uygulaması, kullanıcıların kişiler, işletmeler ve kuruluşlar da dahil olmak üzere kişileriyle ilgili bilgileri kaydetmesine ve düzenlemesine olanak tanır. Bu uygulama, kullanıcıların adlar, adresler, telefon numaraları ve e-posta adresleri gibi ayrıntıları takip etmesine ve kişilerini gruplara ayırmasına olanak tanır.

## SQLite ve Tipik Yol ile İlişkisi

Apple'ın Adres Defteri (Kişiler olarak da bilinir), kişi bilgilerini meta veri klasöründe vCard'lar olarak saklar. **_ABCDDB_ dosyası aslında _SQLite 3 veri dosyasıdır_**.

SQLite, hafif ve kendi kendine yetecek şekilde tasarlanmış popüler bir veritabanı yönetim sistemidir. Birçok farklı türde yazılım ve cihazda kullanılır. SQLite bir tür RDBMS'dir, yani verileri anahtarlar aracılığıyla birbiriyle ilişkili tablolarda saklar. Tamsayılar, kayan noktalı sayılar, dizeler ve ikili veriler dahil olmak üzere bir dizi veri türünü işleyebilir. Ayrıca SQLite, kullanıcıların birden fazla veritabanı işlemini tek bir iş birimi olarak birlikte gerçekleştirmesine olanak tanıyan işlemleri destekler.

ABCDDB uzantılı dosya genellikle burada saklanır

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Bozuk Kişiler veritabanını düzeltme

Lütfen bunu yapmadan önce yedeklemeyi alın. O zaman lütfen şuraya gidin:

`~/Kütüphane/Uygulama Desteği/Adres Defteri`

Bu dizinde .abcddb uzantılı dosya da dahil olmak üzere üç dosya bulacaksınız.

- 'adres defteri-v22.abcddb
- 'adres defteri-v22.abcddb-wal
- 'adres defteri-v22.abcddb-shm

Tüm bu dosyaları silin ve Kişileri yeniden açın, yeniden çalışmaya başlayacaktır.

## Adres Defteri veritabanını Yedeklemeden geri yükleme

Adres Defteri veritabanı kişilerinizin 'addressbook-v22.abcddb'de saklandığını varsayalım.

- Öncelikle Adres Defteri verilerinizi yedekleyin ve tüm uygulamalardan çıkın.
- Veritabanı dosyanızı `~/Library/Application Support/AddressBook` alt dizinine taşıyın
- **Adres Defteri.app**'i başlatın.

## ABCDDB dosya verilerini Microsoft Access'e aktarın

Dosya SQLite 3 veri dosyası olduğundan, abcddb dosyası içindeki verileri ODBC bağlayıcıyı kullanarak Microsoft Access'e aktarabilirsiniz.

SQLite ODBC bağlayıcısı, ODBC arayüzünü destekleyen uygulamaların SQLite veritabanına bağlanmasını sağlayan bir yazılım kitaplığı ve sürücüsüdür. ODBC arayüzünü tanımlayan bir kitaplık ve bu arayüzü SQLite API çağrılarına çeviren bir sürücü içerir. SQLite ODBC bağlayıcıyı kullanmak için önce onu yüklemeli, ardından bilgisayarınıza bir ODBC veri kaynağı kurmalısınız. Bu adımları tamamladıktan sonra ODBC desteğine sahip herhangi bir uygulama, veri kaynağına bağlanıp SQLite veritabanından veri alabilecektir.

## Referanslar
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Mac için Veritabanına Başvurun](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Bir abcddb dosyasını Windows 7 Excel'de nasıl açabilirim veya dışa aktarabilirim?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

