{
  "date": "2019-10-11",
  "keywords": [
"AVI",
"Sıxılmış audio video",
"Fayl",
"Uzatma",
"Fayl Format",
"Multimedia konteyneri",
"XVid",
"DivX",
"Kodeklər",
"Resurs mübadiləsi fayl formatı",
"RIFF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AVI Fayl Format - Audio Video Interleave Fayl",
  "description": "AVI fayl formatı və AVI faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "AVI",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-av-azi"
}
},
  "lastmod": "2021-04-23"
}

## AVI faylı nədir? ##

**AVI** fayl formatı Microsoft tərəfindən təqdim edilmiş Audio Video multimedia konteyner fayl formatıdır. O, **XVid** və **DivX** kimi bir neçə kodeklərdən (Koderlər/Dekoderlər) istifadə etməklə yaradılmış və sıxılmış audio və video məlumatlarını saxlayır. AVI məzmunlarını kodlaşdırmaq üçün müxtəlif kodeklərdən istifadə oluna bildiyindən, axtarış proqramları, yəni AVI pleyerləri, yalnız AVI məzmunlarının yaradıldığı tələb olunan kodeklər quraşdırılıbsa, onları aça bilməlidir. Format defolt olaraq bütün **Microsoft Windows** platformalarında, eləcə də demək olar ki, bütün digər əsas platformalarda dəstəklənir. Bir neçə proqram və API AVI-ni yaratmaq/saxlamaq, oxumaq və MP4, MOV, WMV və s. kimi digər məşhur formatlara çevirmək imkanı verir.

## AVI Fayl Format ##

.avi uzantısı olan fayl AVI faylıdır. Bu, Resurs Mübadiləsi Fayl Formatının (RIFF) alt formatıdır. RIFF məlumatları FourCC teqi ilə müəyyən edilmiş bloklara və ya parçalara təşkil edir. AVI faylı RIFF formatlı faylda sadəcə bir parçadır.

Birinci alt hissədə faylın başlığı hdrl teqi ilə müəyyən edilir; onun məzmununa videonun eni, hündürlüyü və kadr sürəti daxildir. İkinci alt hissədə hərəkət etiketi videonun kadr sürətini təmsil edir. AVI videosu bu hissədəki faktiki audio/vizual məlumatlardan ibarətdir. Həmçinin idx1 teqli üçüncü isteğe bağlı alt hissə də var ki, bu da fayla aid olan fərdi məlumat hissələrinin fayl daxilindəki mövqeyini göstərir.

### Məhdudiyyətlər ###

* Aspekt nisbəti məlumatı orijinal AVI spesifikasiyasında kodlaşdırıla bilməz, baxmayaraq ki, sonrakı OpenDML spesifikasiyası (AVI 2.0) standartlaşdırılmış metod təklif edir.

* AVI faylları film və televiziya post-produksiyasında geniş istifadə olunsa da, onlara vaxt kodu əlavə etmək üçün müxtəlif yanaşmalar rəqabət aparır və bu formatın yararlılığına təsir göstərir.

* AVI-də kodlanmış video faylı kodlaşdırılan çərçivədən (B-çərçivə) kənarda gələcək kadr məlumatlarını tələb edən sıxılma texnikasından istifadə edə bilməz.

* Dəyişən bit sürətləri (VBR) olan AVI fayllarından istifadə etmək problemlidir (məsələn, 32 kHz-dən aşağı nümunə tezliklərində MP3 audio)

* Normal istifadə edilən standart təsviri bədii filmləri kodlayan AVI faylı faylın necə istifadə olunduğundan asılı olaraq saatda təxminən 5 MB yükə səbəb ola bilər.

* AVI faylları şriftlər və altyazılar kimi əlavələri yerləşdirə bilmədiyi halda, altyazılar video axınına sərt kodlaşdırılmalı və ya ayrıca faylda paylanmalıdır.


## Qısa tarix ##

AVI daha möhkəm və təkmil audio və video fayl formatını təmin etmək məqsədi ilə 1992-ci ildə Microsoft tərəfindən təqdim edilmişdir. Bu format internetin istifadəsi ilə tez bir zamanda populyarlaşdı və fərdlərə bulud əsaslı media yaddaşı vasitəsilə birbaşa və dolayı yolla video faylları paylaşmağa imkan verdi.

## İstinadlar ##

* [AVI - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Audio_Video_Interleave)


