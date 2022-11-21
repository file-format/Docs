{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SQL dosya formatı ve SQL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"SQL Dosya Formatı - Yapılandırılmış Sorgu Dili Veri Dosyası",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## SQL dosyası nedir?

.sql uzantılı bir dosya, ilişkisel veritabanlarıyla çalışmak için kod içeren bir Yapılandırılmış Sorgu Dili (SQL) dosyasıdır. Veritabanları üzerinde CRUD (Create, Read, Update, and Delete) işlemleri için SQL deyimleri yazmak için kullanılır. SQL dosyaları, masaüstü ve web tabanlı veritabanlarıyla çalışırken yaygındır. Java Kalıcılık Sorgu Dili (JPQL), LINQ, HTSQL, 4D QL ve diğerleri gibi SQL'in birkaç alternatifi vardır. SQL dosyaları, Microsoft SQL Server, MySQL'in sorgu düzenleyicileri ve Windows işletim sistemindeki Notepad gibi diğer düz metin düzenleyicileri tarafından açılabilir.

## Kısa Tarihçe

* 1970'lerin başında IBM'de Donal D. Chamberlin ve Raymond F. Boyce tarafından geliştirilmiş ve tanıtılmıştır.
* IBM'in orijinal yarı ilişkisel veritabanı yönetim sistemi System R'den veri depolamak ve almak için kullanılır
* Sırasıyla 1979, 1981 ve 1983'te ticari olarak mevcut olan System/38, SQL/DS ve DB2 dahil olmak üzere System R prototiplerini temel alan ticari ürünlerde kullanılmaya başlandı.
* 1986 yılına kadar ANSI ve ISO standart grupları tarafından ilişkisel veritabanı yönetim sistemleri (RDBMS) için standart "Veritabanı Dili SQL" olarak resmen kabul edilmiştir.

## SQL Dosya Biçimi

SQL dosyaları düz metin biçimindedir ve birkaç dil öğesinden oluşabilir. Birbirine bağlı olmadan çalıştırılmaları mümkünse, tek bir SQL dosyasına birden fazla ifade eklenebilir. Bu SQL komutları, CRUD işlemlerini gerçekleştirmek için sorgu düzenleyicileri tarafından yürütülebilir.

### SQL Dili öğeleri

SQL dili elemanları aşağıda listelendiği gibidir.

|Öğe|Açıklama|
---|---|
|Maddeler| İfadelerin ve sorguların kurucu bileşenleri.|
|İfadeler| Sayısal değerler veya veri sütunlarından ve satırlarından oluşan tablolar üretebilir|
|Yüklemler| SQL üç değerli mantık (3VL) (doğru/yanlış/bilinmeyen) veya Boolean doğruluk değerleri olarak değerlendirilebilecek ve ifadelerin ve sorguların etkilerini sınırlamak veya program akışını değiştirmek için kullanılan koşulları belirtin.|
|Sorgular| Verileri belirli kriterlere göre alın. Bu, SQL'in önemli bir öğesidir.|
|Açıklamalar| Şema ve veriler üzerinde kalıcı bir etkisi olabilir veya işlemleri, program akışını, bağlantıları, oturumları veya tanılamayı kontrol edebilir.|

### SQL Örneği
Aşağıdaki SQL deyimi, **DATA** adlı bir tablo ve ardından bu tabloya kayıt eklemek için ek 'INSERT' komutları oluşturur.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Referanslar ##

* [Wikipedia'dan SQL](https://en.wikipedia.org/wiki/SQL)
* [SQL Sözdizimi](https://en.wikipedia.org/wiki/SQL_syntax)

