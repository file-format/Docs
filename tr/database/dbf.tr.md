{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "uzantı", "dbf dosyası", "dbf dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "dbf dosyası nedir", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DBF dosya formatı ve DBF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"DBF - dBase Veritabanı Dosyası",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## DBF dosyası nedir?
.dbf uzantılı dosya **dBASE** adlı bir veritabanı yönetim sistemi uygulaması tarafından kullanılan bir veritabanı dosyasıdır. Başlangıçta, dBASE veritabanı Project Vulcan olarak adlandırıldı; **Wayne Ratliff** tarafından 1978'de başlatıldı. DBF dosya türü, 1983'te dBASE II ile tanıtıldı. Array türü alanlarla birden çok veri kaydını düzenler. Çok çeşitli dosya formatlarıyla uyumluluğu nedeniyle popüler olan **xBase** veri tabanı yazılımı; DBF dosyalarını da destekler.

## DBF Dosya Biçimi
DBF dosya formatı, dBASE veri tabanı yönetim sistemine aittir ancak xBase veya diğer DBMS yazılımları ile uyumlu olabilir. Dbf dosyasının ilk sürümü, ASCII karakter seti kullanılarak verilerin eklenebileceği, değiştirilebileceği, silinebileceği veya yazdırılabileceği basit bir tablodan oluşuyordu. Zamanla .dbf geliştirildi ve veritabanı sisteminin özelliklerini ve yeteneklerini artırmak için ek dosyalar eklendi.

Modern dBASE'de bir DBF dosyası bir başlıktan, veri kayıtlarından ve EOF (Dosya Sonu) işaretçisinden oluşur.

- Başlık, kayıt sayısı ve kayıtlarda kullanılan alan türlerinin sayısı gibi dosya hakkında bilgiler içerir.
- Kayıtlar gerçek verileri içerir.
- Dosyanın sonu, 0x1A değerinde tek bir bayt ile işaretlenir.

### Dosya başlığı
dBase'deki dosya başlığının düzeni aşağıdaki tabloda verilmiştir:

| Bayt | içindekiler | Anlamı |
---|---|---|
| 0 | 1 bayt | DOS dosyası için geçerli dBASE; 0–2 bitleri sürüm numarasını, bit 3, DOS not dosyası için bir dBASE'nin varlığını, 4–6 bitleri bir SQL tablosunun varlığını, bit 7, herhangi bir not dosyasının (dBASE m PLUS veya dBASE için dBASE) varlığını gösterir. DOS) |
| 1–3 | 3 bayt | Son güncelleme tarihi; YYAAGG olarak biçimlendirildi |
| 4–7 | 32 bitlik sayı | Veritabanı dosyasındaki kayıt sayısı |
| 8–9 | 16 bitlik sayı | Başlıktaki bayt sayısı |
| 10–11 | 16 bitlik sayı | Kayıttaki bayt sayısı |
| 12–13 | 2 bayt | Rezerve; 0 ile doldur |
| 14 | 1 bayt | Tamamlanmamış işlemi gösteren bayrak[not 1] |
| 15 | 1 bayt | Şifreleme bayrağı[not 2] |
| 16–27 | 12 bayt | Çok kullanıcılı bir ortamda DOS için dBASE için ayrılmıştır |
| 28 | 1 bayt | Üretim .mdx dosyası bayrağı; Üretim .mdx dosyası varsa 1, yoksa 0 |
| 29 | 1 bayt | Dil sürücüsü kimliği |
| 30–31 | 2 bayt | Rezerve; 0 ile doldur |
| 32–n [not 3][not 4] | Her biri 32 bayt | alan tanımlayıcıları dizisi (tanımlayıcıların düzeni için aşağıya bakın) |
| sayı + 1 | 1 bayt | alan tanımlayıcısı olarak 0x0D dizi sonlandırıcı |

- ISMARKEDO işlevi bu bayrağı kontrol eder (İŞLEMİ BAŞLAT bunu 1'e ayarlar, İŞLEMİ SONLANDIR ve GERİ DÖNÜŞ onu 0'a sıfırlar).
- Bu bayrak 1 olarak ayarlanırsa Veritabanı şifrelendi mesajı görünür.
- Maksimum alan sayısı 255'tir.
- n, alan tanımlayıcı dizisindeki son bayt anlamına gelir.

### Alan tanımlayıcı dizisi
dBASE'de alan tanımlayıcılarının düzeni:

| Bayt | içindekiler | Anlamı |
---|---|---|
| 0–10 | 11 bayt | ASCII'de alan adı (sıfır dolu) |
| 11 | 1 bayt | Alan türü. İzin verilen değerler: C, D, F, L, M veya N (anlamlar için sonraki tabloya bakın) |
| 12–15 | 4 bayt | Ayrılmış |
| 16 | 1 bayt | İkili olarak alan uzunluğu (maksimum 254 (0xFE)). |
| 17 | 1 bayt | İkili alan ondalık sayısı |
| 18–19 | 2 bayt | Çalışma alanı kimliği |
| 20 | 1 bayt | Örnek |
| 21–30 | 10 bayt | Ayrılmış |
| 31 | 1 bayt | Üretim MDX alan bayrağı; Alanın üretim MDX dosyasında bir dizin etiketi varsa 1, yoksa 0 |

### Veritabanı kayıtları
Her kayıt bir silme (1 baytlık) bayrağıyla başlar. Alanlar, alan ayırıcılar olmadan kayıtlara sarılır. Tüm alan verileri ASCII'dir. Alanın türüne bağlı olarak, uygulama daha fazla kısıtlama getirir. İşte dBase'deki alan türleri:

| Alan türü | anımsatıcı | Neleri kabul eder |
-------|-----|----|
| Ç | Karakter | Herhangi bir ASCII metni (alanın uzunluğuna kadar boşluklarla doldurulmuş) |
| D | Tarih | Ay, gün ve yılı ayırmak için sayılar ve bir karakter (dahili olarak YYYYAAGG biçiminde 8 basamak olarak depolanır) |
| F | Kayan nokta | -, ., 0–9 (sağa yaslanmış, boşluklarla doldurulmuş) |
| L | Mantıksal | Y, y, N, n, T, t, F, f veya ? (başlatılmamışken) |
| M | not | Herhangi bir ASCII metni (bir .dbt blok numarasını temsil eden 10 basamak olarak dahili olarak depolanır, sağa yaslanmış, boşluklarla doldurulmuş) |
| N | Sayısal | -, ., 0–9 (sağa yaslanmış, boşluklarla doldurulmuş) |









## Referanslar ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

