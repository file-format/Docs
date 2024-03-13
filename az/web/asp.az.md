{
  "date": "2019-10-11",
  "keywords": [
"asp",
"asp faylı",
"asp fayl formatı",
"asp fayl növü",
"fayl",
"növü",
"asp faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASP - Active Server Pages File Format",
  "description": "ASP faylı və onları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "ASP",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-azp"
}
},
  "lastmod": "2019-09-10"
}

## ASP faylı nədir?

ASP veb səhifələr yaratmaq üçün inkişaf çərçivəsi olan Active Server Pages deməkdir. Veb sorğularına xidmət etmək üçün kompüter kodunun daxili server tərəfindən icrasına imkan verir. Veb-brauzer tərəfindən ASP faylı üçün sorğu yaradıldıqda, server faylı oxuyur və **[HTML](/web/html/)** nəticəsini yaratmaq üçün onun daxilində istənilən kodu/skripti icra edir və nəticə brauzerə nümayiş etdirilmək üçün qaytarılır.

Server tərəfindən xidmət edilən statik səhifələr olan HTML səhifələrindən fərqli olaraq, ASP faylları verilənlər bazasından verilənlərə sorğular daxil ola bilən iş vaxtında dinamik məzmunlar yaradır. ASP səhifələri adətən .html deyil, .asp uzantısından istifadə edir. ASP faylı daxilində kod/skript server tərəfində icra olunduğundan, sorğu göndərən brauzer təqdim olunan səhifəni yaratmaq üçün istifadə olunan kodu görə bilmir. Bütün müasir brauzerlər nəticədə yaradılan səhifələri göstərməyə qadirdir. Microsoft texnologiyası əsasında qurulan ASP ilə qurulmuş səhifələr Microsoft Internet Information Services (IIS) serverlərində yerləşdirilir.

## ASP Fayl Formatının Qısa Tarixi
ASP server yan səhifələrini inkişaf etdirmək və idarə etmək üçün daha müasir və daha səmərəli bir üsul olan ASP.NET ilə əvəzlənənə qədər yalnız bir neçə düzəlişdən keçmişdir. ASP dəstəyi standart olaraq İnternet İnformasiya Xidmətləri (IIS) ilə birlikdə daxil edilir. ASP hər birində təkmilləşdirmələrlə üç fərqli versiyada nəşr olundu.

* ASP 1.0 1996-cı ilin dekabrında IIS 3.0-ın bir hissəsi kimi buraxılmışdır

* ASP 2.0 1997-ci ilin sentyabrında IIS 4.0-ın bir hissəsi kimi buraxılmışdır

* ASP 3.0 2000-ci ilin noyabrında IIS 5.0-ın bir hissəsi kimi buraxılmışdır


## ASP funksional obyektləri

ASP faylları istifadəçi sorğularını emal etmək və istifadəçilərə xidmət göstərmək üçün çıxış səhifələri yaratmaq üçün server tərəfindəki obyektlərdən istifadə edir. Hər bir obyekt sorğuların və cavabların işlənməsi üçün bir sıra kolleksiyalar, xüsusiyyətlər və üsullara malikdir. Bu obyektlərə aşağıdakılar daxildir:

### Sorğu Obyekti

Brauzer serverdən səhifə tələb etdikdə ona sorğu deyilir. Sorğu obyekti ziyarətçidən məlumat almaq üçün istifadə olunur.

### Cavab obyekti

ASP Response obyekti serverdən istifadəçiyə çıxış göndərmək üçün istifadə olunur.

### Server obyekti

ASP Server obyekti serverdə xassələrə və metodlara daxil olmaq üçün istifadə olunur. O, verilənlər bazası (ADO), fayl sistemi ilə əlaqə yaratmağa və serverdə quraşdırılmış komponentlərdən istifadə etməyə imkan verir.

### Sessiya obyekti

Sessiya obyekti istifadəçinin serverdən səhifə tələb edən brauzeri ilə serverin özü arasında əlaqə kimidir. Buna ASP tərəfindən yaradılan və istifadəçinin kompüterinə göndərilən kuki vasitəsilə nail olunur. Sessiya obyekti istifadəçi sessiyası haqqında məlumat saxlayır və ya onun parametrlərini dəyişdirir. Session obyektində saxlanılan məlumatlar proqramın bütün səhifələrində paylaşılır. Sessiya dəyişənlərində saxlanılan ümumi məlumat ad, id və üstünlüklərdir. Server hər yeni istifadəçi üçün yeni Session obyekti yaradır və sessiyanın müddəti bitdikdə Session obyektini məhv edir.

### Tətbiq obyekti

Tətbiq obyekti proqramdakı bir çox səhifələr tərəfindən istifadə ediləcək məlumatları (verilənlər bazası əlaqə məlumatı kimi) saxlayır. Məlumata istənilən səhifədən daxil olmaq olar. Məlumat bir yerdə də dəyişdirilə bilər və dəyişikliklər avtomatik olaraq bütün səhifələrdə əks olunacaq. Proqram obyekti Session obyekti kimi istənilən səhifədən dəyişənləri saxlamaq və onlara daxil olmaq üçün istifadə olunur.

### ASPERrror obyekti

ASPError obyekti ASP 3.0-da həyata keçirilib və IIS5 və sonrakı versiyalarda mövcuddur. ASPError obyekti ASP səhifəsində skriptlərdə baş verən hər hansı xətanın ətraflı məlumatını göstərmək üçün istifadə olunur.

**Qeyd:** ASPError obyekti Server.GetLastError çağırıldıqda yaradılır, ona görə də xəta haqqında məlumatı yalnız Server.GetLastError metodundan istifadə etməklə əldə etmək olar.

## İstinadlar

* [ASP - W3C tərəfindən](https://www.w3schools.com/asp/default.asp)

* [Sadə ASP Səhifələrinin Yaradılması](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))


