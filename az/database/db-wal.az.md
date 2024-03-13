{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "DB-WAL fayl formatı və DB-WAL fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title" : "DB-WAL Fayl Format - SQLite Database Write-Ahead Log File",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-az",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## DB-WAL faylı nədir?

.db-wal fayl uzantısı məşhur açıq mənbəli relational verilənlər bazası idarəetmə sistemi olan SQLite ilə əlaqələndirilir. WAL fayl formatı (Write-Ahead Log üçün qısadır) SQLite tərəfindən istifadə edilən ənənəvi geri qaytarma jurnalına alternativdir. O, daha çox paralellik nəzarətini təmin edir, eyni zamanda birdən çox prosesə verilənlər bazasını oxumağa imkan verir, eyni zamanda qəza-bərpa imkanlarını təmin edir. .db-wal faylı verilənlər bazasına edilən və hələ əsas verilənlər bazası faylına (.db uzantısı ilə) daxil edilməmiş dəyişiklikləri saxlamaq üçün istifadə olunur.

## Ümumi WAL Format

WAL (Write-Ahead Log) fayl formatında verilənlər bazasına edilən dəyişikliklər əsas verilənlər bazası faylına daxil edilməzdən əvvəl əvvəlcə WAL faylına yazılır. Bu, verilənlər bazasına daha çox eyni vaxtda daxil olmağa imkan verir, çünki dəyişikliklər edilərkən çoxlu proseslər verilənlər bazasından oxuya bilər. Bundan əlavə, WAL fayl formatı gözlənilməz bağlanma halında verilənlər bazasını əvvəlki vəziyyətinə qaytarmağa imkan verən qəza-bərpa imkanlarını təmin edir.

## DB-WAL və WAL formatı arasındakı fərq

Həm .db-wal, həm də WAL fayl formatları məşhur açıq mənbəli relational verilənlər bazası idarəetmə sistemi olan SQLite ilə əlaqələndirilir. Bununla belə, ikisi arasında incə bir fərq var.

.db-wal faylı mahiyyətcə WAL faylıdır, lakin fərqli fayl uzantısına malikdir. .db-wal faylı verilənlər bazasında edilmiş və hələ də əsas verilənlər bazası faylına (.db uzantısı ilə) daxil edilməmiş dəyişiklikləri saxlamaq üçün istifadə olunur, WAL fayl formatı isə verilənlər bazası dəyişikliklərinin qabaqcadan yazma jurnalını saxlamaq üçün istifadə olunur. .

Başqa sözlə desək, .db-wal faylı SQLite verilənlər bazaları tərəfindən verilənlər bazasında edilmiş və hələ də əsas verilənlər bazası faylına daxil edilməmiş dəyişiklikləri saxlamaq üçün istifadə edilən xüsusi WAL fayl növüdür. WAL fayl formatı bu tip fayl formatı üçün ümumi termindir.

Beləliklə, WAL fayl formatı üçün ümumi termindir, .db-wal SQLite verilənlər bazaları tərəfindən istifadə edilən WAL fayl formatının xüsusi tətbiqidir.

## İstinadlar
* [WAL rejimi fayl formatı](https://www.sqlite.org/walformat.html)

* [İrəlidən yazmaq](https://www.sqlite.org/wal.html)


