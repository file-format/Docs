{
  "date": "2020-11-11",
  "keywords": [
"NDF",
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
  "description": "MDF fayl formatı və NDF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "NDF Fayl Format - SQL Server Master Database Faylı",
  "linktitle": "NDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nd-azf"
}
},
  "lastmod": "2020-08-12"
}

## NDF faylı nədir?

.ndf uzantılı fayl istifadəçi məlumatlarını saxlamaq üçün [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) tərəfindən istifadə edilən ikincil verilənlər bazası faylıdır. NDF ikinci yaddaş faylıdır, çünki SQL server istifadəçi tərəfindən müəyyən edilmiş məlumatları [MDF](/database/mdf/) kimi tanınan əsas yaddaş faylında saxlayır. NDF məlumat faylı isteğe bağlıdır və əsas MDF faylı bütün ayrılmış yerdən istifadə etdiyi halda məlumat saxlama yerini idarə etmək üçün istifadəçi tərəfindən müəyyən edilir. O, adətən ayrı diskdə saxlanılır və bir çox saxlama qurğusuna yayıla bilər. NDF fayllarını açmaq üçün MDF fayllarının olması lazımdır.

## NDF fayl formatı

NDF fayl formatı [MDF](/database/mdf/) formatından fərqlənmir və məlumatların saxlanmasının əsas vahidi kimi səhifələrdən istifadə edir. hər bir səhifə 96 baytlıq başlıq ilə başlayır, o cümlədən:

 * Səhifə ID
 * Struktur növü
 * Səhifələrdəki qeydlərin sayı
 * Əvvəlki və sonrakı səhifələrə işarələr

### NDF Fayl Strukturu

MDF faylı aşağıdakı məlumat strukturuna malikdir.

 * Səhifə 0: Başlıq
 * Səhifə 1: İlk PFS
 * Səhifə 2: İlk GAM
 * Səhifə 3: İlk SGAM
 * Səhifə 4: İstifadə olunmayıb
 * Səhifə 5: İstifadə olunmayıb
 * Səhifə 6: İlk DCM
 * Səhifə 7: İlk BCM

#### NDF Fayl Başlığı

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

## Məlumat faylı səhifəsi

SQL Server məlumat faylındakı səhifələr sıfırdan (0) başlayır və ardıcıl olaraq artır. Hər bir fayl unikal fayl ID nömrəsi ilə tanınır. Fayl identifikatoru və səhifə nömrəsi cütü verilənlər bazasındakı səhifəni unikal şəkildə müəyyənləşdirir. Verilənlər bazasında səhifə nömrələrini göstərən nümunə aşağıdakı şəkildəki kimidir.

{{< figure src="../ndf.png" alt="NDF verilənlər bazası fayl formatı" >}}

Bu nümunə 4 MB əsas məlumat faylı və 1 MB ikincil məlumat faylı olan verilənlər bazasında səhifə nömrələrini göstərir.

## İstinadlar

 * [Verilənlər Bazası Faylları və Fayl Qrupları](https://learn.microsoft.com/en-us/sql/relational-databases/database/database-files-and-filegroups?view=sql-server-ver16)
 * [Verilənlər Bazasının Ayrılması və Qoşulması - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- versiya 15)
 * [SQL Server Data Fayl Anatomiyasının Təhlili](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

