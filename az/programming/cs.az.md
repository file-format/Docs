{
  "date": "2019-10-11",
  "keywords": [
"cs",
"fayl",
"uzadılması",
"fayl formatı",
"CSharp",
"Proqramlaşdırma dili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CS - CSharp Kod Faylı",
  "description": "CS fayl formatı və CS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c-azs"
}
},
  "lastmod": "2019-09-10"
}

## CS faylı nədir?

.cs uzantılı fayllar C# proqramlaşdırma dili üçün mənbə kodu fayllarıdır. .NET Framework ilə istifadə üçün Microsoft tərəfindən təqdim edilən fayl formatı EXE və ya DLL şəklində yekun çıxış faylını yaratmaq üçün tərtib edilən kodu yazmaq üçün aşağı səviyyəli proqramlaşdırma dilini təmin edir. Bunlar Microsoft Visual Studio ilə yaradıla və tərtib edilə bilər. Microsoft Visual Studio Express həmçinin pulsuz IDE olan bu cür faylları yaratmaq və yeniləmək üçün istifadə edilə bilər. CS faylları sadə iş masası proqramlarından daha mürəkkəb proqramlara qədər dəyişən proqramların inkişafı üçün istifadə olunur. C# dili ilə yaradılmış sadə Visual Studio layihəsi [solution](/programming/sln/) bir və ya bir neçə belə fayldan ibarət ola bilər. Kompilyasiyaya daxil edilmək üçün işarələnmiş fayllar layihənin bir hissəsi olan [CSPROJ](/programming/csproj/) faylında qeyd olunur və tərtibçiyə qeyd olunan fayllardan istifadə etməyi əmr edir.

## CS Fayl Format ##

CS faylları redaktə üçün istənilən mətn redaktorunda açıla bilən mətn əsaslı fayl formatlarıdır. Bununla belə, düzgün sintaksis vurğulanması ilə dəstəklənən IDE-də açıldıqda kodu oxumaq və tənzimləmək asandır. Sadə bir CS faylı ehtiva edir:

* Ad məkanları bəyannaməsi - Həmin xüsusi ad məkanı ilə müəyyən edilmiş xüsusi funksionallığa istinad üçün

* Dəyişənlərin elanı - Xüsusi tətbiq üçün sinif səviyyəli dəyişənləri elan etmək

* Metodlar Bəyannaməsi - Xüsusi funksionallıq üçün metodlar bəyannaməsini elan etmək


### Sintaksis ###

* Nöqtəli vergül ifadənin sonunu bildirmək üçün istifadə olunur.

* Buruq mötərizələr ifadələri qruplaşdırmaq üçün istifadə olunur. İfadələr adətən metodlara (funksiyalara), metodlar siniflərə və siniflər ad fəzalarına qruplaşdırılır.

* Dəyişənlər bərabərlik işarəsi ilə təyin edilir, lakin iki ardıcıl bərabərlik işarəsi ilə müqayisə edilir.

* Kvadrat mötərizələr massivlərlə birlikdə həm onları elan etmək, həm də onlardan birində verilmiş indeksdə qiymət almaq üçün istifadə olunur.


### Nümunə ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

## Digər CS faylları

**.cs** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Məlumat Faylları və Oyun**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Proqramlaşdırma**
- [CS - CSharp Kod Faylı](/programming/cs/)

