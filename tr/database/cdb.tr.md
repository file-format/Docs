{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "uzantı", "cdb dosyası", "cdb dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "cdb dosyası nedir" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"CDB dosya formatı ve CDB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"CDB - Sabit Veritabanı Dosyası",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## .cdb dosyası nedir?
CDB dosyaları, e-posta gibi görev açısından kritik uygulamalarda kullanılır. CDB, sabit veritabanları oluşturmak veya okumak için hızlı, güvenilir ve basit bir paket olan "sabit veritabanı" anlamına gelir. Veritabanı değişimi, sistem çökmelerine karşı güvenlidir. Kullanıcıların yeniden yazma sırasında duraklaması gerekmez. CDB ilişkisel bir dizi (disk üzerinde) olarak çalışır, anahtarları değerlerle eşler ve birden çok değerin tek bir anahtarda saklanmasını sağlar.

## CDB Dosya Biçimi
CDB dosya formatı sayıları, ofsetleri, uzunlukları ve karma değerleri küçük endian formatında işaretsiz 32 bit tamsayılar olarak saklar. Anahtarların ve verilerin, özel bir işlem gerektirmeyen opak bayt dizileri olduğu düşünülmektedir. Veritabanının başlangıcında, sabit boyutlu başlık, dosya içindeki konumlarını ve yuvalardaki uzunluklarını listeleyerek 256 karma tabloyu temsil eder. Genellikle veriler bir kayıt dizisi olarak saklanır, her kayıt anahtar uzunluğunu, veri uzunluğunu, anahtarı ve verileri depolar. Sıralama veya hizalama kuralları yoktur. Kayıtları, değişen uzunluklarda 256 hash tablosu seti takip eder. Sıfır geçerli bir uzunluk olduğundan, veritabanında fiziksel olarak saklanan 256'dan az karma tablo olabilir, ancak 256 tablo olarak kabul edilen hiçbir şey yoktur. Hash tabloları, her biri bir hash değeri ve bir kayıt ofseti içeren bir dizi yuvadan oluşur. "Boş yuvalar"ın ofseti sıfırdır.

### Yapı
CDB veritabanı, tek bir bilgisayar dosyasındaki tüm veri kümesinden oluşur. Üç bölümden oluşur:
- Sabit boyutlu bir başlık
- Veri
- Bir dizi hash tablosu.

Aramalar yalnızca tam anahtarlar için kullanılabilir. Aramalar aşağıdaki algoritmayı kullanarak hareket eder:

- Anahtarı aç.
- Bu kaydın hangi hash tablosunda ve slotta olması gerektiğini belirleyin.
- Hash tablosunda belirtilen yuvayı test edin.

Birden fazla değere sahip anahtarların aranması için, aramaya bir sonraki yuvada devam edilerek ek değerler bulunabilir.

#### Özellikler

CDB veritabanı yapısı çeşitli özellikler sağlar:

##### Hızlı aramalar
Devasa bir veritabanında başarılı bir arama normalde yalnızca iki disk erişimi gerektirir ve başarısız bir arama yalnızca bir disk erişimi gerektirir.
##### Düşük havai
Bir veritabanı 2048 bayt, kayıt başına 24 bayt ve anahtarlar ile veriler için alan kullanır.
##### Rastgele sınır yok
CDB, 4 gigabayta kadar herhangi bir veritabanını yönetebilir. Başka bir kısıtlama olmadığı için kayıtların belleğe sığması bile gerekmez. Veritabanları, makineden bağımsız bir biçimde saklanır.
##### Hızlı atomik veritabanı değişimi
**cdbmake** komutu, diğer karma paketlerden daha hızlı bir şekilde tüm veritabanını iki büyüklük sırasına göre yeniden yazabilir.
##### Hızlı veritabanı dökümleri
**cdbdump** bir veritabanının içeriğini cdbmake uyumlu biçimde yazdırabilir.


## Referanslar ##

* [cdb (yazılım) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(yazılım))
* [CDB spesifikasyonu](http://cr.yp.to/cdb.html)

