{
  "date": "2019-12-12",
  "keywords": [
"SQLite",
"uzadılması",
"fayl",
"fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"Verilənlər Bazasının Faylları"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "SQLITE faylları yarada və aça bilən SQLITE fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "SQLite fayl formatı",
  "linktitle": "SQLITE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sqlit-aze"
}
},
  "lastmod": "2020-11-09"
}

## SQLite faylı nədir?

.sqlite genişləndirilməsi olan fayl [SQLite](https://www.sqlite.org/index.html) proqramı ilə yaradılmış yüngül SQL verilənlər bazası faylıdır. O, faylın özündə verilənlər bazasıdır və müstəqil, tam funksiyalı, yüksək etibarlı [SQL](/database/sql/) verilənlər bazası mühərrikini həyata keçirir. SQLite verilənlər bazası faylları bu faylları şəbəkə üzərindən sadə mübadilə etməklə sistemlər arasında zəngin məzmunu bölüşmək üçün istifadə edilə bilər. Demək olar ki, bütün mobil telefonlar və kompüterlər məlumatların saxlanması və paylaşılması üçün SQLite-dən istifadə edir və platformalararası proqramlar üçün fayl formatının seçimidir. Yığcam istifadəsi və asan istifadəsi sayəsində o, digər proqramlar içərisində yığılır. SQLite bağlamaları C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) və bir çox başqaları kimi proqramlaşdırma dilləri üçün mövcuddur.

## SQLite fayl formatı

SQLite əslində SQLite fayl formatından istifadə edərək SQLite RDBMS-ni həyata keçirən C-Dil kitabxanasıdır. Hər gün yeni cihazların təkamülü ilə onun fayl formatı köhnə cihazları yerləşdirmək üçün geriyə uyğun saxlanılıb. SQLite fayl formatı məlumat üçün uzunmüddətli arxiv formatı kimi görünür.

### Verilənlər Bazası Faylı

SQLite verilənlər bazası iki fayl vasitəsilə tam saxlanılır.
 * Əsas verilənlər bazası faylı - SQLite verilənlər bazasının tam vəziyyətini ehtiva edir
 * Rollback Journal - Əlavə məlumatı ikinci faylda saxlayır və əməliyyatların icrası zamanı istifadə olunur. SQLite WAL rejimində olduqda, yazma başlığı jurnalı faylı saxlanılır.

#### Jurnal faylı

Bu fayl kompüter qəzası kimi hallarda sonuncu əməliyyatın tamamlana bilməyəcəyi halda saxlanılan bütün məlumatları saxlamaq üçün nəzərdə tutulub. Bu fayl verilənlər bazası faylını ardıcıl vəziyyətə qaytarmaq üçün istifadə olunur.

#### Səhifələr

Əsas SQLite verilənlər bazası faylı bir və ya bir neçə səhifədən ibarətdir. İstənilən vaxtda, əsas verilənlər bazasındakı hər bir səhifə aşağıdakılardan biri olan tək istifadəyə malikdir:

 * Kilid bayt səhifəsi
 * Sərbəst siyahı səhifəsi
   * Sərbəst siyahının əsas səhifəsi
   * Sərbəst siyahı yarpaq səhifəsi
 * b-ağac səhifəsi
   * Masa b-ağacının daxili səhifəsi
   * Cədvəl b-ağac yarpağı səhifəsi
   * İndeks b-ağacının daxili səhifəsi
   * İndeks b-ağac yarpağı səhifəsi
 * Yük daşıma səhifəsi
 * Göstərici xəritə səhifəsi

SQLite verilənlər bazası fayllarının ölçüsü bir neçə kilobaytdan bir neçə giqabayta qədər dəyişə bilər.

### SQLite Başlığı

The SQLite database header is located in the first 100 bytes of the database file. Every valid SQLite database file starts with 16 bytes (in hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Başlıq sahələrinin təfərrüatları aşağıdakı cədvəldəki kimidir.

|Ofset|Ölçü|Təsvir|
---|---|---|
|0|16|Başlıq sətri: SQLite formatı 3\000|
|16|2|Bayta verilənlər bazası səhifəsinin ölçüsü. 512 və 32768 daxil olmaqla ikinin gücü və ya 65536 səhifə ölçüsünü təmsil edən 1 dəyəri olmalıdır.|
|18|1|Fayl formatının yazma versiyası. miras üçün 1; WAL üçün 2.|
|19|1|Fayl formatının oxunmuş versiyası. miras üçün 1; WAL üçün 2.|
|20|1|Hər səhifənin sonunda istifadə olunmamış ehtiyat boşluğunun baytları. Adətən 0.|
|21|1|Maksimum daxil edilmiş faydalı yük hissəsi. 64 olmalıdır.|
|22|1|Minimum daxil edilmiş faydalı yük hissəsi. 32 olmalıdır.|
|23|1|Yarpağın faydalı yük hissəsi. 32 olmalıdır.|
|24|4|Fayl dəyişikliyi sayğacı.|
|28|4|Verilənlər bazası faylının səhifələrdə ölçüsü. Başlıqdaxili verilənlər bazası ölçüsü.|
|32|4|İlk sərbəst siyahının əsas səhifəsinin səhifə nömrəsi.|
|36|4|Sərbəst siyahı səhifələrinin ümumi sayı.|
|40|4|Sxem kukisi.|
|44|4|Sxem formatının nömrəsi. Dəstəklənən sxem formatları 1, 2, 3 və 4-dür.|
|48|4|Defolt səhifə keş ölçüsü.|
|52|4|Avtomatik vakuum və ya artımlı-vakuum rejimlərində olduqda ən böyük kök b-ağac səhifəsinin səhifə nömrəsi və ya başqa halda sıfır.|
|56|4|The database text encoding. A value of 1 means UTF-8. 2 dəyəri UTF-16le deməkdir. 3 dəyəri UTF-16be deməkdir.|
|60|4|User_version praqması tərəfindən oxunan və təyin edilən istifadəçi versiyası.|
|64|4|Artıq-vakuum rejimi üçün doğru (sıfırdan fərqli). Yanlış (sıfır) əks halda.|
|68|4|PRAGMA application_id.| tərəfindən təyin edilmiş Tətbiq IDsi
|72|20|Genişləndirmə üçün qorunur. Sıfır olmalıdır.|
|92|4|Nömrə üçün etibarlı versiya.|
|96|4|SQLITE_VERSION_NUMBER|

## İstinadlar ##

* [SQLite Fayl Format - SQLite](https://www.sqlite.org/fileformat2.html)

* [SQLite - Vikipediya](https://en.wikipedia.org/wiki/SQLite)

* [SQLite - C Dil Xüsusiyyətləri](https://www.sqlite.org/c3ref/intro.html)


