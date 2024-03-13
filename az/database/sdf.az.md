{
  "date": "2021-05-03",
  "keywords": [
"SDF",
"sdf faylı",
"sdf faylı nədir",
"sdf faylı necə açmaq olar",
"uzadılması",
"fayl",
"sdf fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"Verilənlər Bazasının Faylları"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "SDF fayl formatı və SDF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "SDF - SQL Server yığcam verilənlər bazası faylı",
  "linktitle": "SDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sd-azf"
}
},
  "lastmod": "2021-05-03"
}

## SDF faylı nədir?
.sdf uzantılı faylda kompakt relyasiya verilənlər bazası kimi tanınan Microsoft SQL Server Compact (SQL CE) verilənlər bazası var; Microsoft tərəfindən mobil qurğular və masaüstü kompüterlər üçün hazırlanmış proqramlar üçün hazırlanmışdır. O, həm 32, həm də 64 bit əməliyyat sistemini dəstəkləyir və verilənlər bazasının tam məzmunu bir SDF faylına daxil edilir və 4 GB-dan çox disk sahəsi tuta bilər. Təhlükəsizlik məqsədi ilə .sdf faylı 128 bit şifrələmə ilə şifrələnə bilər. SQL CE işləmə müddəti .sdf faylına paralel çox istifadəçi girişini təmin edir. SDF faylı **QuickOnce** vasitəsilə kopyalana bilər və ya sadəcə olaraq sistemin yerləşdirilməsi üçün təyinat yerinə kopyalana bilər.

## SDF fayl formatı
SDF faylında adətən kompakt relyasiya verilənlər bazası adlanan verilənlər bazası var. SDF faylı verilənlər bazası ilə əlaqəli bütün məlumatları ehtiva edir və SQL Server Compact .sdf fayllarını idarə etmək üçün istifadə edilən yüngül və pulsuz verilənlər bazası mühərrikidir. .sdf faylının ölçüsü 4 GB ölçüsündən çox olmamalıdır. SDF faylları saxlanılan prosedurlar, tetikleyiciler və ya görünüşlər haqqında məlumatları saxlamır. SQL CE verilənlər bazasından istifadə edən proqramlar ADO.NET əlaqə sətirində SDF faylına gedən yolu göstərməli deyil, bunun əvəzinə o, proqram üçün montaj manifestində müəyyən edilən məlumat qovluğunu müəyyən edən |DataDirectory|\database_name.sdf kimi qeyd edilə bilər.
.sdf adlandırma konvensiyası isteğe bağlıdır və faylı saxlamaq üçün istənilən genişləndirmə istifadə edilə bilər. Verilənlər bazası faylı üçün parolun qurulması isteğe bağlı bir addımdır. Verilənlər bazasını sıxışdırmaq və ya təmir etmək üçün fayl **sıxlaşdırılmış/təmir edilmiş verilənlər bazası** seçimi ilə yadda saxlanılmalıdır.

## İstinadlar

 * [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
 * [ASP.NET Veb Tətbiqləri üçün SQL Server Kompaktdan istifadə](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


