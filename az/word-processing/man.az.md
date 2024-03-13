{
  "date": "2021-07-25",
  "keywords": [
"adam",
"fayl",
"uzadılması",
"növü",
"format",
"Unix təlimatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MAN - Unix Təlimatı",
  "description": "MAN fayllarını yarada və aça bilən FODT fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "MAN",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ma-azn"
}
},
  "lastmod": "2021-07-25"
}

## MAN faylı nədir?

.man uzantısı olan fayl proqram sənədləri formasında Unix proqramlaşdırma istifadəçi təlimatı olan man səhifəsini ifadə edir. Sənədlərə baxmaq üçün istifadə edilən Unix-ə daxil olan Man” yardım proqramı tərəfindən istifadə olunur. Proqram sənədləri bölmələr və səhifələrdəki məlumatları ehtiva edir ki, onları əmrlər verməklə komanda terminalından Man yardım proqramından istifadə etməklə əldə etmək olar. Kompüterdə sənədlərin yumşaq nüsxəsi kimi mövcud olduğundan, ona daxil olmaq üçün heç bir çap surəti və ya internet bağlantısı tələb olunmur.

## Unix Manual Man File Format - Ətraflı Məlumat

Man səhifələri düz mətn formatında saxlanılır və baxmaq və ya redaktə etmək üçün istənilən mətn redaktorunda yaradıla və açıla bilər. UNIX-də Man səhifələrindən məlumat təlimatdakı bölmə və səhifə nömrələrinə istinad daxil olmaqla terminaldan əmrlər verməklə əldə edilir.

### Bölmələr və Səhifələr

Unix man sistemin təlimatıdır, burada komandanın hər bir səhifə arqumenti proqramın, köməkçi proqramın və ya funksiyanın adına istinad edir. komanda, bölmə məlumatı ilə təmin olunarsa, həmin xüsusi bölmədə səhifəni axtaracaq. Bununla belə, standart davranış bütün bölmələrdə səhifəni axtarmaq və birdən çox bölmədə olub-olmamasından asılı olmayaraq ilk səhifəni göstərməkdir.

### Bölmə Nömrələri

Aşağıda təlimatın bölmə nömrələri və onların ehtiva etdiyi səhifələrin növləri haqqında məlumat verilir.

|Bölmə nömrəsi|səhifələrin növü|
---|---|
|1|İcra edilə bilən proqramlar və ya qabıq əmrləri|
|2|Sistem çağırışları (kernel tərəfindən təmin edilən funksiyalar)|
|3|Kitabxana çağırışları (proqram kitabxanaları daxilində funksiyalar)|
|4|Xüsusi fayllar (adətən /dev-də tapılır)|
|5|Fayl formatları və konvensiyalar, məsələn /etc/passwd|
|6|Oyunlar|
|7|Müxtəlif (makrospaketlər və konvensiyalar daxil olmaqla), məsələn, man(7), groff(7)|
|8|Sistem idarəetmə əmrləri (adətən yalnız kök üçün)|
|9|Kernel rutinləri [Qeyri-standart]|

## Nümunə - MAN Səhifələrini Necə Oxumaq olar?

Budur, Man əmrindən istifadə edərək MkDir əmri haqqında məlumat əldə etmək üçün bir nümunə.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## İstinadlar

* [OpenDocument Texniki Xüsusiyyətləri - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)

* [man(1) — Linux təlimat səhifəsi](https://man7.org/linux/man-pages/man1/man.1.html)


