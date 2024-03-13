{
  "date": "2019-10-11",
  "keywords": [
"asmx",
"asmx faylı",
"asmx fayl formatı",
"asmx fayl növü",
"fayl",
"növü",
"asmx faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASMX - ASP.NET Veb Xidmət Faylı",
  "description": "ASMX faylı və ASMX fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "ASMX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asm-azx"
}
},
  "lastmod": "2021-06-10"
}

## ASMX faylı nədir?

.asmx uzantıları olan fayl Sadə Obyekt Giriş Protokolundan (SOAP) istifadə edərək internet üzərindən iki obyekt arasında əlaqəni təmin edən ASP.NET Veb Xidmət faylıdır. O, daxil olan sorğunu emal etmək və cavabı qaytarmaq üçün Windows əsaslı Veb Serverdə xidmət kimi yerləşdirilir. ASP.NET veb-səhifələrinin vizual nümayişi üçün kodu ehtiva edən [ASPX](/web/aspx/) fayllarından fərqli olaraq, ASMX faylları serverdə arxa fonda işləyir və verilənlər bazasına qoşulmaq, məlumatların əldə edilməsi və onu hansı formatda geri qaytarmaq kimi müxtəlif tapşırıqları yerinə yetirir. tələb edilib. Bunlar xüsusi olaraq XML şəbəkə xidmətləri üçün istifadə olunur.

## ASMX fayl formatı

ASMX faylları düz mətn formatındadır və Microsoft Visual Studio və ya mətn redaktorları kimi proqramlarda açıla və ya redaktə edilə bilər. Bu, Microsoft-un xüsusi fayl formatıdır və veb xidmətlərinin yaradılması üçün yaxşı müəyyən edilmiş sintaksisə malikdir. SOAP XML şəklində ASMX faylının cavabı aşağıdakı elementlərə malikdir.

 * `Zərf` - XML sənədini SOAP mesajı kimi müəyyən edən kök element.
 * `Başlıq` - Autentifikasiya məlumatları kimi proqrama aid məlumatları ehtiva edən əlavə element. Başlıq elementi varsa, o, Zərf elementinin ilk uşaq elementi olmalıdır.
 * `Body` - Alıcı üçün nəzərdə tutulmuş SOAP mesajını ehtiva edir.
 * `Fault` - Səhv mesajlarını göstərmək üçün istifadə edilən isteğe bağlı element. Səhv elementi varsa, o, Bədən elementinin uşaq elementi olmalıdır.

ASMX faylları [C#](/programming/cs/), [Visual Basic](/programming/vb/) və ya JScript kimi .NET dillərində yazıla bilər.

## ASMX ASPX və ASCX-dən nə ilə fərqlənir?

ASMX faylları ASPX və ASCX fayllarından fərqlidir.

 * ASPX, Active Server Pages, fayllar veb serverlərdə işləyən Microsoft ASP.NET çərçivəsi ilə yaradılan proqramlaşdırma fayllarıdır. İstifadəçi belə bir səhifəyə daxil olmaq üçün müraciət etdikdə bunlar müştərinin veb brauzerində göstərilir.
 * ASCX, Active Server User Control, ASP.NET veb səhifələrində və ya bütün vebsaytda təkrar istifadə edilə bilən idarəetmələri müəyyən etmək üçün istifadə olunan istifadəçi nəzarətlərini müəyyən edir.

## İstinadlar

 * [ASMX Xidmətindən istifadə](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
 * [ASCX İstifadəçi Nəzarəti](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

