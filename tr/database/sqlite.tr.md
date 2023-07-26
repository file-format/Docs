{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SQLITE dosya formatı ve SQLITE dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"SQLite Dosya Biçimi",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## SQLite Dosyası Nedir?

.sqlite uzantılı bir dosya, [SQLite](https://www.sqlite.org/index.html) yazılımıyla oluşturulan basit bir SQL veritabanı dosyasıdır. Kendi başına bir dosyadaki bir veritabanıdır ve bağımsız, tam özellikli, yüksek düzeyde güvenilir bir [SQL](/tr/database/sql/) veritabanı motorunu uygular. SQLite veritabanı dosyaları, bu dosyaları ağ üzerinden basit bir şekilde değiştirerek sistemler arasında zengin içerikleri paylaşmak için kullanılabilir. Hemen hemen tüm cep telefonları ve bilgisayarlar veri depolamak ve paylaşmak için SQLite kullanır ve platformlar arası uygulamalar için tercih edilen dosya formatıdır. Kompakt kullanımı ve kolay kullanılabilirliği nedeniyle, diğer uygulamaların içinde paketlenmiş olarak gelir. C, [C#](/tr/programming/cs/), [C++](/tr/programming/cpp), [Java](/tr/programming/java/), [PHP](/tr/programming/php/) gibi programlama dilleri için SQLite bağlamaları mevcuttur. ), Ve bircok digerleri.

## SQLite Dosya Biçimi

Gerçekte SQLite, SQLite dosya biçimini kullanarak SQLite RDBMS'yi uygulayan bir C-Dil kitaplığıdır. Her gün yeni cihazların gelişmesiyle, dosya formatı eski cihazlara uyum sağlamak için geriye dönük olarak uyumlu tutuldu. SQLite dosya formatı, veriler için uzun vadeli arşiv formatı olarak görülmektedir.

### Veritabanı Dosyası

Bir SQLite veritabanı tamamen iki dosya aracılığıyla korunur.
* Ana veritabanı Dosyası - SQLite veritabanının tam durumunu içerir
* Geri Alma Günlüğü - Ek bilgileri ikinci bir dosyada saklar ve işlemlerin gerçekleştirilmesi sırasında kullanılır. SQLite'ın WAL modunda olması durumunda, bir yazma kafası günlük dosyası tutulur.

#### Günlük Dosyası

Bu dosya, bilgisayar çökmesi gibi durumlarda son işlemin tamamlanamaması durumunda tüm bilgilerin saklanması için tasarlanmıştır. Bu dosya, veritabanı dosyasını tutarlı bir duruma geri yüklemek için kullanılır.

#### Sayfa

Ana SQLite veritabanı dosyası bir veya daha fazla sayfadan oluşur. Herhangi bir zamanda, ana veritabanındaki her sayfanın aşağıdakilerden biri olan tek bir kullanımı vardır:

* Kilit baytı sayfası
* Serbest liste sayfası
* Bir serbest liste ana sayfa
* Bir serbest liste yaprak sayfası
* Bir b-ağacı sayfası
* Bir tablo b-ağacı iç sayfası
* Bir tablo b-ağacı yaprak sayfası
* Bir dizin b-ağacı iç sayfası
* Bir dizin b-ağacı yaprak sayfası
* Bir yük taşma sayfası
* Bir işaretçi harita sayfası

SQLite veritabanı dosyalarının boyutu birkaç kilobayttan birkaç gigabayta kadar değişebilir.

### SQLite Başlığı

SQLite veritabanı başlığı, veritabanı dosyasının ilk 100 baytında bulunur. Geçerli her SQLite veritabanı dosyası 16 bayt (onaltılık olarak) ile başlar:53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Başlık alanlarının detayları aşağıdaki tablodaki gibidir.

|Ofset|Boyut|Açıklama|
---|---|---|
|0|16|Başlık dizesi: "SQLite biçimi 3\000"|
|16|2|Bayt olarak veritabanı sayfa boyutu. 512 ile 32768 (dahil) arasında ikinin katı veya 65536 sayfa boyutunu temsil eden 1 değeri olmalıdır.|
|18|1|Dosya biçimi yazma sürümü. miras için 1; WAL için 2.|
|19|1|Dosya biçimi okunan sürüm. miras için 1; WAL için 2.|
|20|1|Her sayfanın sonunda baytlık kullanılmayan "ayrılmış" alan. Genellikle 0.|
|21|1|Maksimum yerleşik yük oranı. 64 olmalı.|
|22|1|Minimum yerleşik yük oranı. 32 olmalı.|
|23|1|Yaprak yük oranı. 32 olmalı.|
|24|4|Dosya değişiklik sayacı.|
|28|4|Veritabanı dosyasının sayfa cinsinden boyutu. "Başlık içi veritabanı boyutu".|
|32|4|İlk serbest liste ana sayfasının sayfa numarası.|
|36|4|Serbest listedeki toplam sayfa sayısı.|
|40|4|Şema çerezi.|
|44|4|Şema biçim numarası. Desteklenen şema biçimleri 1, 2, 3 ve 4'tür.|
|48|4|Varsayılan sayfa önbelleği boyutu.|
|52|4|Otomatik vakum veya artımlı vakum modlarındayken en büyük kök b-ağacı sayfasının sayfa numarası, aksi halde sıfır.|
|56|4|Veritabanı metin kodlaması. 1 değeri UTF-8 anlamına gelir. 2 değeri UTF-16le anlamına gelir. 3 değeri UTF-16be anlamına gelir.|
|60|4|Kullanıcı_sürüm pragması tarafından okunan ve ayarlanan "kullanıcı sürümü".|
|64|4|Artırımlı vakum modu için doğru (sıfır değil). Aksi takdirde yanlış (sıfır).|
|68|4|PRAGMA application_id tarafından ayarlanan "Uygulama Kimliği".|
|72|20|Genişletme için ayrıldı. Sıfır olmalı.|
|92|4|Geçerli sürüm numarası.|
|96|4|SQLITE_VERSION_NUMBER|

## Referanslar ##

* [SQLite Dosya Biçimi - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - C Dil Özellikleri](https://www.sqlite.org/c3ref/intro.html)

