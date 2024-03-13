{
  "date": "2020-11-11",
  "keywords": [
"MDF",
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
  "description": "MDF fayl formatı və MDF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "MDF Fayl Format - SQL Server Master Database Faylı",
  "linktitle": "MDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-azf"
}
},
  "lastmod": "2020-08-12"
}

## MDF faylı nədir?

.mdf uzantılı fayl istifadəçi məlumatlarını saxlamaq üçün [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) tərəfindən istifadə edilən Əsas Məlumat Bazasıdır. Bütün məlumatlar bu faylda saxlandığı üçün bu çox vacibdir. MDF faylı istifadəçilərin məlumatlarını əlaqəli verilənlər bazalarında forma sütunlarında, sətirlərdə, sahələrdə, indekslərdə, görünüşlərdə və cədvəllərdə saxlayır. SQL Server verilənlər bazasının işinə müsbət təsir göstərmək üçün avtomatik böyümə və avtomatik kiçilmə parametrlərini təyin etməyə imkan verir. MDF faylları yüklənə və Microsoft SQL Server istifadə edərək verilənlər bazasına əlavə edilə bilər. MDF faylları Application/octet-stream mime növünə malikdir.

## MDF fayl formatı

SQL Serverdə verilənlərin saxlanmasının əsas vahidi səhifədir. Verilənlər bazasına təyin edilmiş saxlama səhifəsi 0-dan n-ə qədər nömrələnən məntiqi səhifələrə bölünür. Tək bir səhifə Səhifə ID-sindən, səhifənin aid olduğu strukturun növündən, səhifədəki qeydlərin sayından və əvvəlki və sonrakı səhifələrin göstəricilərindən ibarət 96 baytlıq başlıq ilə başlayır.

### Fayl strukturu

MDF faylı aşağıdakı məlumat strukturuna malikdir.

 * Səhifə 0: Başlıq
 * Səhifə 1: İlk PFS
 * Səhifə 2: İlk GAM
 * Səhifə 3: İlk SGAM
 * Səhifə 4: İstifadə olunmayıb
 * Səhifə 5: İstifadə olunmayıb
 * Səhifə 6: İlk DCM
 * Səhifə 7: İlk BCM

#### Fayl başlığı

Bütün faylların 0 nömrəli səhifəsi fayl haqqında metadata saxlayan başlıqdan ibarətdir.

#### Səhifə Boş Yeri (PFS)
PFS ayırma statusunu müəyyənləşdirir və boş yerin miqdarını müəyyən edir.

 * Bit 1: Səhifənin ayrılıb-açılmadığını göstərir.
 * Bit 2: Səhifənin qarışıq dərəcədə olub olmadığını göstərir.
 * Bit 3: Bu səhifənin IAM səhifəsi olduğunu göstərir.
 * Bit 4: Bu səhifədə xəyal qeydləri olduğunu göstərir
 * 5-dən 7-dək bitlər: Səhifənin dolğunluğunu aşağıdakı kimi göstərən birləşdirilmiş üç bitlik dəyər:
   * 0: Səhifə boşdur
   * 1: Səhifə 1-50% doludur
   * 2: Səhifə 51-80% doludur
   * 3: Səhifə 81-95% doludur
   * 4: Səhifə 96-100% doludur

## İstinadlar

 * [Database Files and Filegroups](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Database Detach and Attach - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
 * [Analyzing SQL Server Data File Anatomy](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

