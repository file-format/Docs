{
  "date": "2020-01-10",
  "keywords": [
"c",
".c",
"ac faylı nədir",
"c faylını necə açmaq olar",
"uzadılması",
"fayl",
"c faylı",
"c fayl formatı",
"c fayl uzantısı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "C - C Dil Proqramlaşdırma Faylı",
  "description": "C faylları yarada və aça bilən C fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "C",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--azc"
}
},
  "lastmod": "2020-01-10"
}

## C faylı nədir?

c fayl uzantısı ilə saxlanılan fayl C proqramlaşdırma dilində yazılmış mənbə kodu faylıdır. **C faylı** mənbə kodu şəklində tətbiqin funksionallığının bütün həyata keçirilməsini ehtiva edir. Mənbə kodunun bəyanı [.h](/programming/h/) uzantısı ilə saxlanılan başlıq fayllarında yazılır. C++ C dilinin müasir formasıdır və bu gün proqram təminatının əksəriyyətini hazırlamaq üçün istifadə olunur.

## Qısa tarix

C dili UNIX əməliyyat sistemi üçün müxtəlif utilitlərin yaradılması nəticəsində yaranmışdır. Denis Ritchie, bu proqramlaşdırma dilinin yaradılmasının arxasında duran adam, iş ilk olaraq 1960-cı illərdə və 1970-ci illərin əvvəllərində başlamışdır.

## C Fayl Format

C faylları proqramlaşdırma dilinin sintaksisinə uyğun olaraq düz mətn faylı formatında yazılır. Tipik bir C faylı olacaq:

 * hər hansı başlıq Fayllarını idxal etmək üçün faylın yuxarısındakı idxal bəyanatı
 * İstənilən funksionallığı həyata keçirmək üçün bir və ya bir neçə üsul

### Başlıqların idxalı

.h uzantılı başlıq faylları layihəyə digər funksionallıq fayllarını daxil etmək üçün lazımi ifadələri ehtiva edir. Bundan əlavə, bunlar icra faylında müəyyən edilmiş metodların bəyannamələrini ehtiva edir. Başlıq faylları aşağıda göstərildiyi kimi daxil ifadəsindən istifadə etməklə daxil edilir.

```
#include <filename.h>
```

### Mənbə kodunun icrası

Funksional tələblərin faktiki icrası C faylında metodlar kimi kodlanır. C faylındakı hər bir metodun qaytarma növü, metod adı var və bəzi giriş parametrləri ola bilər. Qayıdış növü etibarsız deyilsə, üsul bəzi dəyəri qaytara bilər.

### C kodu nümunəsi
Budur AC nümunə proqramı:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **İstinadlar** ##

* [Sinif Tətbiqi - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Class_implementation_file)


