{
  "date": "2019-12-10",
  "keywords": [
"CSV",
"fayl",
"uzadılması",
"fayl formatı",
"Vergüllə Ayrılmış Dəyərlər",
"Elektron cədvəl"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "CSV faylları yarada və aça bilən CSV fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "CSV fayl formatı",
  "linktitle": "CSV",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-cs-azv"
}
},
  "lastmod": "2019-12-10"
}

## CSV faylı nədir?

.csv (Virgüllə Ayrılmış Dəyərlər) uzantısı olan fayllar vergüllə ayrılmış dəyərləri olan məlumatların qeydlərini ehtiva edən düz mətn fayllarını təmsil edir. CSV faylındakı hər bir sətir faylda olan qeydlər dəstindən yeni qeyddir. Belə fayllar məlumatların bir saxlama sistemindən digərinə ötürülməsi nəzərdə tutulduqda yaradılır. Bütün proqramlar vergüllə ayrılmış qeydləri tanıya bildiyi üçün belə məlumat fayllarının verilənlər bazasına idxalı çox rahat şəkildə həyata keçirilir. Microsoft Excel və ya OpenOffice Calc kimi demək olar ki, bütün cədvəl proqramları çox səy göstərmədən CSV-ni idxal edə bilər. Bu cür fayllardan idxal edilən məlumatlar istifadəçiyə təqdim etmək üçün elektron cədvəlin xanalarında yerləşdirilir.

## Qısa tarix ##

Aşağıda CSV fayl formatının mənşəyi və tarixi ilə bağlı bəzi sürətli faktlar verilmişdir.

* 1972 - IBM Fortran (səviyyə H uzadılmış) kompilyator onları OS/360 altında dəstəklədi


* 1978 - Siyahıya yönəldilmiş giriş/çıxış ayırıcılar üçün vergül və boşluqlardan istifadə edən FORTRAN 77 tərəfindən dəstəklənir


* 2005 - CSV MIME Məzmun Növü kimi [RFC4180](https://tools.ietf.org/html/rfc4180) ilə standartlaşdırılıb.


* 2013 - RFC4180 çatışmazlıqları W3C tövsiyəsi ilə həll edildi


* 2015 - W3C 2015-ci ilin dekabrında tövsiyə kimi başlayan CSV-metadata standartları üçün tövsiyələrin ilk layihələrini hazırladı.


## CSV fayllarını çevirin ##

CSV faylları bu faylları aça bilən proqramlardan istifadə edərək bir neçə fərqli fayl formatına çevrilə bilər. Məsələn, Microsoft Excel məlumatları CSV fayl formatından idxal edə və onu XLS, [XLSX](/spreadsheet/xlsx/), [PDF](/pdf/), [TXT](/word-processing/txt/), XML və [HTML](/web/html/) fayl formatlarında saxlaya bilər. Eynilə, digər masaüstü və onlayn xidmətlər CSV fayllarını HTML, ODS və [RTF](/word-processing/rtf/) formatına ixrac etmək imkanı verir.

## CSV fayl formatı ##

CSV fayl formatının [RFC4180](https://tools.ietf.org/html/rfc4180) altında göstərildiyi məlumdur. O, hər hansı bir faylın CSV uyğunluğunu müəyyən edir, əgər:

* Hər bir qeyd sətir sonu (CRLF) ilə ayrılmış ayrıca sətirdə yerləşir. Misal üçün:

  * aaa, bbb, ccc CRLF
  * zzz,yyy,xxx CRLF
* Fayldakı son qeyddə son sətir fasiləsi ola bilər və ya olmaya da bilər. Misal üçün:

  * aaa, bbb, ccc CRLF
  * zzz,yyy,xxx
* Normal qeyd sətirləri ilə eyni formatda faylın ilk sətri kimi görünən isteğe bağlı başlıq xətti ola bilər. Bu başlıq fayldakı sahələrə uyğun adlardan ibarət olacaq və faylın qalan hissəsindəki qeydlərlə eyni sayda sahəni ehtiva etməlidir (başlıq xəttinin mövcudluğu və ya olmaması bunun isteğe bağlı "başlıq" parametri vasitəsilə göstərilməlidir. MIME növü). Misal üçün:

  * sahə_adı, sahə_adı, sahə_adı CRLF
  * aaa, bbb, ccc CRLF
  * zzz,yyy,xxx CRLF
* ﻿Başlıqda və hər bir qeyddə vergüllə ayrılmış bir və ya daha çox sahə ola bilər. Hər bir sətirdə fayl boyu eyni sayda sahə olmalıdır. Boşluqlar sahənin bir hissəsi hesab olunur və nəzərə alınmamalıdır. Qeydin sonuncu sahəsindən sonra vergül qoyulmamalıdır. Misal üçün:

  * aaa, bbb, ccc
* Hər bir sahə qoşa dırnaqlar içərisində ola bilər və ya olmaya da bilər (lakin bəzi proqramlar, məsələn, Microsoft Excel, ümumiyyətlə qoşa dırnaqlardan istifadə etmir). Əgər sahələr qoşa dırnaqlarla əhatə olunmayıbsa, o zaman sahələr içərisində qoşa dırnaqlar görünməyə bilər. Misal üçün:\

  * aaa, bbb, ccc CRLF
  * zzz,yyy,xxx
* Sətir sonu (CRLF), qoşa dırnaq və vergüldən ibarət sahələr qoşa dırnaq içərisinə daxil edilməlidir. Misal üçün:

  * aaa,b CRLF
  * bb,ccc CRLF
  * zzz,yyy,xxx
* Əgər sahələri əhatə etmək üçün qoşa dırnaq işarələrindən istifadə edilirsə, onda sahənin içərisində görünən qoşa dırnaq işarəsi ondan əvvəl başqa bir cüt dırnaq işarəsi qoyaraq qaçmalıdır. Misal üçün:

  * aaa,bbb,ccc

Bununla belə, müasir istifadə işığında, ayırıcı yalnız vergüllə məhdudlaşmır və nöqtəli vergül, nişan və ya boşluq da ola bilər. Microsoft Excel kimi proqramlar CSV faylından qeydləri idxal etmək üçün ayırıcı simvolu təyin etmək seçimini təmin edir.

## İstinadlar

* [RFC 4180](https://tools.ietf.org/html/rfc4180)

* [RFC 2048](https://tools.ietf.org/html/rfc2048)

* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Virgüllə ayrılmış_values)


