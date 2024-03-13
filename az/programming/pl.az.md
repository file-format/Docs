{
  "date": "2021-07-23",
  "keywords": [
"PL",
"fayl",
"uzadılması",
"format",
"Perl",
"Perl dili",
"PL faylları",
"proqramlaşdırma"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "PL fayl formatı və PL fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "PL Faylı - Perl Skripti Fayl Formatı",
  "linktitle": "PL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-p-azl"
}
},
  "lastmod": "2021-07-23"
}

## PL faylı nədir?

.pl uzantılı fayl skript dili olan Perl Script faylıdır. Bunlar Perl Tərcüməçi proqramından istifadə etməklə tərtib edilir və işləyir. PL skript faylı kod sətirlərini, dəyişənləri və şərhləri ehtiva edir. Skript dilləri nisbətən çətindir
[PHP](/programming/php/) kimi digər proqramlaşdırma fayl formatlarını başa düşmək. PL faylları yaradıla bilər və Windows, macOS və Linux ilə uyğun gəlir.

## Perl Skript Dilinin Qısa Tarixi

Bu dil ilk dəfə 1987-ci ildə istifadəyə verildi, buna görə də bu fayllar öz mənşəyini həmin il aldı. 1989-cu ildə Perl 2 buraxıldı. Daha sonra o, yeniləndi və 5.35 versiyasına qədər dəyişdirildi və növbəti versiyanın gələn il buraxılması nəzərdə tutulur.

Hər yeniləmədə dilin və faylların funksionallığı, performansı və görünüşü ilə bağlı alətlər əlavə edilmişdir. Bu illərdə versiyalar haqqında çoxlu təftişlər olub. Əvvəlcə əsas skript dili idi, lakin indi bir çox başqa modulları da əhatə edir. Əvvəlcə bu çox sadə dil idi, lakin bu dilin yazıları yığcam olduğundan başa düşmək olduqca çətin idi.

## Perl Fayl Formatının Genişləndirilməsi Xüsusiyyətləri

Bu proqramlaşdırma fayllarının bəzi xüsusiyyətləri və ya spesifikasiyası var, onlardan bəziləri aşağıdakılardır:

* Bu fayllara daxil olan kod düz mətn formatındadır və skriptin inkişafı üçün istifadə olunur
* Serverin skripti, mətnin təhlili və serverin idarə edilməsi bu dilin skriptinin əhatə etdiyi əsas cəhətlərdir.
* Bu dillə əlaqəli bir çox məşhur proqramlar Active state Active Perl və Bare Bones BBEdit (Mac OS ilə uyğundur)
* Bu dil yüksək səviyyəli dil hesab olunur
* Win32 üçün istifadəçi dilin yerli ikili paylanmasını quraşdırmalı ola bilər
* Müxtəlif Windows Resurs Dəstlərində icra edilə bilən olmaq üçün bəzi skript alətləri tələb olunur
* Visual Studio .NET proqramlaşdırma dillərinin inkişafı üçün məşhur çərçivədir. Visual Perl kimi tanınan Active State aləti Perl-i Visual studio-ya əlavə etmək üçün istifadə olunur
* Fayllarda mənbə kodunun birinci sətri istifadə olunan tərcüməçinin məlumatını təsvir edir. PL faylları adətən **#!/usr/bin/perl** xətti ilə başlayır və bu xətt kompüterinizə bu skripti kompüterdə quraşdırılmış Perl tərcüməçisindən istifadə edərək işlətməyi əmr edir.


## PL Skript Nümunələri

```
#!/usr/bin/perl
print "Hello, world\n";
```

Bu çap edəcək

```
Hello, World
```

### Tək sətir şərh ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Çox sətirli şərh ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Dəyişən təyinatı ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skalyar dəyişən təyinatı ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Sadə skalyar əməliyyatlar ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## İstinadlar ##

- [Python (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

