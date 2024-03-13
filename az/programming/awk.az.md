{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AWK Fayl Format - AWK Skript Faylı",
  "description":"AWK fayl formatı və AWK fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk-az",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## AWK faylı nədir?

AWK faylı Unix və Linux əməliyyat sistemləri ilə birlikdə gələn **AWK** mətn emal proqramı üçün yaradılmış skript faylıdır. O, mətn və ya faylın məzmunu üzərində mətnin uyğunlaşdırılması, dəyişdirilməsi və çap edilməsi kimi hərəkətləri yerinə yetirmək üçün məntiqi təlimatları ehtiva edir. Bu, giriş faylından hesabatlar və formatlanmış mətn yaratmağa kömək edir. Awk yardım proqramı adətən əksər linux/unix paylamalarında /usr/bin/awk-da yerləşir.

## AWK skriptini necə yaratmaq olar?

AWK faylı Linux/Unix ƏS-də istənilən mətn redaktorunda yaradıla və ya açıla bilər. Yeni AWK skript faylı aşağıdakı kimi yaradıla bilər.

```
$ vi script.awk
```

Bu, AWK faylını mətn redaktorunda açacaq. Mətn redaktoruna bəzi ifadələri aşağıdakı kimi daxil edin.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Bu mətn məzmununun birinci sətri aşağıdakı kimi izah olunur.

 * \#! – skriptdəki təlimatlar üçün tərcüməçini təyin edən Shebang” kimi istinad edilir
 * /usr/bin/awk – tərcüməçidir
 * -f – proqram faylını oxumaq üçün istifadə edilən tərcüməçi seçimi

## AWK skriptini necə icra etmək olar?

Aşağıdakı əmri verməklə faylı yadda saxlayın və skripti icra edilə bilən hala gətirin:
```
$ chmod +x script.awk
```

Bundan sonra skript aşağıdakı kimi işlədilə bilər.

```
$ ./script.awk
```

bu, aşağıdakı çıxışla nəticələnir.

```
Writing my first Awk executable script!
```

## İstinad ##

* [Awk Proqramlaşdırma Dilindən istifadə edərək Skriptlər Yazın](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)


