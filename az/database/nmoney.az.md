{
  "date": "2023-05-17",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "NMONEY fayl formatı və NMONEY faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "NMONEY Faylı - Denaro Hesab Fayl Formatı",
  "linktitle": "NMONEY",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nmone-azy"
}
},
  "lastmod": "2023-05-17"
}

## NMONEY faylı nədir?

NMONEY faylı maliyyə əməliyyatlarının izlərini ehtiva edən maliyyə məlumatlarının saxlanması verilənlər bazası faylıdır. O, Nickvision tərəfindən hazırlanmışdır və şəxsi maliyyə proqram təminatı olan Nickvision Denaro proqramında istifadə edilmişdir. NOMONEY faylında saxlanılan data hesaba kredit və debet əməliyyatları haqqında məlumat daxildir.

NOMONEY faylları [Github](https://github.com/NickvisionApps/Denaro) tətbiqi ilə açıla bilər.

## Denaro Proqram təminatı haqqında

Denaro was initially developed by [Nickvision](https://nickvision.org/) as a product that was later converted to an open-source software app hosted on [Github](https://github.com/NickvisionApps/Denaro). Since then app has been modified and updated on Github only. The app is developed in C# in Windows UI with Windows App SDK (WinUI 3 as at this time).

### Denaro tərəfindən təklif olunan xüsusiyyətlər

 * Ən populyar və tanış tab interfeysi ilə eyni vaxtda birdən çox hesabı idarə edin
 * Əməliyyatları növə, qrupa və ya tarixə görə süzün
 * Hər ay baş verən hesablar kimi əməliyyatları təkrarlayın
 * Bir hesabdan digərinə pul köçürmək
 * Hesabdan məlumatları CSV faylı kimi ixrac edin və hesaba əməliyyatlar əlavə etmək üçün CSV, OFX və ya QIF faylını idxal edin

## Denaro Fayl Format - Ətraflı Məlumat

Denaro faylları ikili fayl formatında diskdə saxlanılır. Maliyyə məlumatları **.SQLITE3** fayl formatında verilənlər bazası faylı kimi saxlanılır. SQLITE, SQLite proqramı ilə yaradılmış yüngül SQL verilənlər bazası faylıdır. Bu, tam xüsusiyyətli və yüksək etibarlı verilənlər bazası təmin etməyə qadir olan müstəqil verilənlər bazası mühərrikini təmin edir. SQLite verilənlər bazası faylları bu faylları şəbəkə üzərindən sadəcə mübadilə etməklə sistemlər arasında zəngin məzmunu paylaşmaq üçün istifadə edilə bilər. SQLite bağlamaları C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) və bir çox başqaları kimi proqramlaşdırma dilləri üçün mövcuddur.

## İstinadlar

 * [Nickvision](https://nickvision.org/)
 * [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

