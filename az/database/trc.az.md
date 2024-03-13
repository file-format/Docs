{
  "date": "2021-08-24",
  "keywords": [
"trc faylı",
"trc fayl formatı",
"trc faylı nədir",
"fayl",
"trc nümunəsi",
"trc fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "TRC faylları yarada və aça bilən TRC fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "TRC - SQL Server İz Faylı",
  "linktitle": "TRC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-tr-azc"
}
},
  "lastmod": "2021-08-24"
}

## TRC faylı nədir?
.trc uzantısı olan fayl Microsoft SQL server verilənlər bazası fəaliyyətinin iz nəticələrini ehtiva edir. Bu fayllar SQL Server Profiler proqramı tərəfindən yaradılmışdır; adətən Microsoft SQL Server proqramı ilə paketlənir. Verilənlər bazası inzibatçıları verilənlər bazası bəyanatlarının ardıcıllığını təhlil edə bilər və bir növ səhv və ya xəbərdarlıqdan şübhələnildikdə izləmə jurnalını nəzərdən keçirə bilər. Bu fayllar adətən Windows əməliyyat sistemində Proqram Faylları qovluğunda MSSQL-in tipik LOG qovluğunda yerləşir.

## TRC fayl formatı
TRC fayl formatı SQL Server Profiler tərəfindən avtomatik olaraq MS SQL serveri tərəfindən bu yaxınlarda yerinə yetirilən ifadələrin yeni izini yaratmaq üçün istifadə olunur. SQL Server Profiler hər hansı yeni iz üçün standart şablondan istifadə edir. Bununla belə, proqram müəyyən hadisələrin monitorinqi üçün bir neçə əvvəlcədən təyin edilmiş şablonları ehtiva edir. Həmçinin SQL Server Profiler, izlərə daxil ediləcək hadisə siniflərini və məlumat sütunlarını təyin edən şablonlar yaratmaq üçün istifadə edilə bilər.

### Əvvəlcədən təyin edilmiş şablonlar
SQL Server Profiler-ə daxil edilmiş bəzi əvvəlcədən təyin edilmiş şablonların siyahısı budur:
- **SP_Counts**: Zamanla saxlanan prosedurun icrası davranışını ələ keçirir.
- **Standart**: İz yaratmaq üçün ümumi başlanğıc nöqtəsi.
- **TSQL**: Müştərilər tərəfindən SQL Serverə təqdim edilən bütün Transact-SQL ifadələrini və buraxılış vaxtını çəkir.
- **TSQL_Duration**: Müştərilər tərəfindən SQL Serverə təqdim edilən bütün Transact-SQL ifadələrini, onların icra müddətini çəkir və müddətə görə qruplaşdırır.
- **TSQL_Grouped**: Müəyyən müştəri və ya istifadəçinin sorğularını araşdırmaq üçün istifadə edin.
- **TSQL_Locks**: Kilidlərin problemlərini həll etmək, fasilələri kilidləmək və eskalasiya hadisələrini kilidləmək üçün istifadə edin.
- **TSQL_Replay**: Benchmark testi kimi təkrarlanan tənzimləməni yerinə yetirmək üçün istifadə edin.
- **TSQL_SPs**: Saxlanılan prosedurların komponent addımlarını təhlil etmək üçün istifadə edin.
- **Tunning**: Database Engine Tuning Advisor-un verilənlər bazalarını tənzimləmək üçün iş yükü kimi istifadə edə biləcəyi iz çıxışı yaratmaq üçün istifadə edin.
### İzi Windows Performans Qeydiyyatı məlumatları ilə əlaqələndirin
SQL Server Profiler, Microsoft Windows performans jurnalını açmaq, izlə əlaqələndirmək üçün sayğacları seçmək və MS SQL Server Profiler GUI-də iz ilə yanaşı seçilmiş performans sayğaclarını göstərmək üçün istifadə edilə bilər. Seçilmiş iz hadisəsi ilə əlaqəli performans jurnalı məlumatlarını göstərmək üçün SQL Server Profiler-in Sistem Monitoru məlumat pəncərəsi panelində şaquli qırmızı çubuq.


## İstinadlar ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)


