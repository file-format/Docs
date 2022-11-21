{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "uzantı", "dosya", "dosya biçimi", "Veritabanı Dosya Türü", "Veritabanı Dosya Biçimi", "Veritabanı Dosyaları" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DDL dosya formatı ve DDL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"DDL Dosya Biçimi - Bir Veri Tanımlama Dili Dosyası",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## DDL dosyası nedir?

.ddl uzantılı bir dosya, bir veritabanının şemasını tanımlamak için kullanılan bir Veri Tanımlama Dili dosyasıdır. Tablolar, sütunlar, kayıtlar ve diğer alanlar gibi veritabanı yapılarıyla çalışmak için ifadeler/komutlar içerir. Bir DDL dosyasındaki komutlar [SQL](/tr/database/sql/) dilinde yazılır ve veritabanında tablo oluşturma, bırakma ve güncelleme gibi işlemleri gerçekleştirebilir. Oluşturulan veritabanı şemasına aittir ve tüm CRUD işlemleri bu şema üzerinde gerçekleştirilebilir. DDL dosyaları oluşturabilen ve açabilen popüler uygulamalar Windows Metin Düzenleyici, Jetbrains Intellij Idea ve EclipseLink'tir.

## DDL komutları

Tek bir DDL dosyası, doğru sözdizimi sayesinde sırayla yürütülecek ve şemada karakter kümeleri ve tabloları oluşturma, tabloları bırakma, tabloları yeniden adlandırma ve değiştirme gibi değişiklikler yapacak birkaç komut içerebilir. Aşağıdaki DDL komutları, veritabanı şemasıyla çalışırken yaygın olarak kullanılır.

`CREATE` - Veritabanını veya nesnelerini (tablo, dizin, işlev, görünümler, saklama prosedürü ve tetikleyiciler gibi) oluşturmak için kullanılır.

`DROP` – Veritabanından nesneleri silmek için kullanılır.

`ALTER` - Veritabanının yapısını değiştirmek için kullanılır.

`TRUNCATE` – Kayıtlar için ayrılan tüm boşluklar da dahil olmak üzere bir tablodan tüm kayıtları kaldırmak için kullanılır.

"YORUM" – Veri sözlüğüne yorumlar ekler.

`RENAME` – Veritabanındaki mevcut bir nesneyi yeniden adlandırır.

## DDL Örneği

Aşağıdaki örnek, bir tablo oluşturan ve alanlarını tanımlayan CREATE komutu için DDL ifadesini göstermektedir.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referanslar ##

* [Wikipedia'dan DDL](https://en.wikipedia.org/wiki/Data_definition_language)

