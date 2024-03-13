{
  "date": "2019-10-11",
  "keywords": [
"vb",
"fayl",
"uzadılması",
"fayl formatı",
"Visual Basic",
"Proqramlaşdırma bələdçisi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VB - Visual Basic kod faylı",
  "description": "VB fayl formatı və VB faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "VB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-v-azb"
}
},
  "lastmod": "2019-09-10"
}

## VB faylı nədir?

VB faylı Microsoft tərəfindən .NET proqramlarının inkişafı üçün yaradılmış Visual Basic dilində yaradılmış mənbə kodu faylıdır. Fərqli sintaksisi olan digər oxşar dil, faylları [.CS](/programming/cs/) fayl uzantısı ilə saxlanılan C# dilidir. Fayl formatı EXE və ya DLL şəklində yekun çıxış faylını yaratmaq üçün tərtib edilən kodu yazmaq üçün aşağı səviyyəli proqramlaşdırma dilini təmin edir. Bunlar Microsoft Visual Studio ilə yaradıla və tərtib edilə bilər. Microsoft Visual Studio Express həmçinin pulsuz IDE olan bu cür faylları yaratmaq və yeniləmək üçün istifadə edilə bilər. VB dili ilə yaradılmış sadə Visual Studio layihəsi [solution](/programming/sln/) bir və ya bir neçə belə fayldan ibarət ola bilər. Kompilyasiyaya daxil edilmək üçün işarələnmiş fayllar layihənin bir hissəsi olan [CSPROJ](/programming/csproj/) faylında sadalanır və tərtibçiyə qeyd olunan fayllardan istifadə etməyi əmr edir.

## VB Fayl Format - Ətraflı Məlumat

VB faylları redaktə üçün istənilən mətn redaktorunda açıla bilən mətn əsaslı fayl formatlarıdır. Bununla belə, düzgün sintaksis vurğulanması ilə dəstəklənən IDE-də açıldıqda kodu oxumaq və tənzimləmək asandır. Sadə bir VB faylı ehtiva edir:

* Ad məkanları bəyannaməsi - Həmin xüsusi ad məkanı ilə müəyyən edilmiş xüsusi funksionallığa istinad üçün

* Dəyişənlərin elanı - Xüsusi tətbiq üçün sinif səviyyəli dəyişənləri elan etmək

* Metodlar Bəyannaməsi - Xüsusi funksionallıq üçün metodlar bəyannaməsini elan etmək


## VB fayl formatı nümunəsi

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



