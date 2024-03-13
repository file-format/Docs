
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "4-cü fayl - dördüncü dil fayl formatı",
  "description":"4-cü faylları yarada və aça bilən nümunə və API ilə .4-cü fayl formatının nə olduğunu öyrənin.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th-az",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## 4-cü fayl nədir?

.4-cü fayl uzantısı olan fayl **Dördüncü Proqramlaşdırma Dili** üçün yaradılmış proqramlaşdırma faylıdır. O, dördüncü proqramlaşdırma dilində yazılmış proqramlar üçün mənbə kodunu ehtiva edir və proqram icra edildikdə çıxışı yaradır. Bu, [C](/programming/c/) və [C++](/programming/cpp/) mənbə faylına bənzər başqa bir proqramlaşdırma dili faylıdır.

## 4-cü Fayl Format - Ətraflı Məlumat


### 4-cü Proqramlaşdırma Dili Kod Nümunəsi

Verilmiş ədədin faktorialını hesablayan Forth dilində yazılmış sadə proqram nümunəsi:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * yığının üstündəki iki dəyəri çoxaldır. if və start/until konstruksiyaları proqramın hərəkətinə nəzarət edir.

Bu proqramdan istifadə etmək üçün siz dördüncü tərcüməçiyə tərifi daxil etməli və sonra faktorial sözü tapmaq istədiyiniz nömrəyə zəng etməlisiniz:

```
10 factorial .
```
Bu, 10-un faktorialı olan 3628800 çıxışı ilə nəticələnəcəkdir.

## İstinadlar

 * [Forth Programming Language](https://en.wikipedia.org/wiki/Forth_(programming_language))

