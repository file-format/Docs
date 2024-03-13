{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR Fayl - dBASE Struktur Siyahısı Obyekt Faylı - .str faylı nədir və onu necə açmaq olar?",
  "description" : "STR dBASE Struktur Siyahısı Obyekt Faylı və onun necə açılacağını öyrənin.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-az",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## STR faylı nədir?

STR fayl formatı adətən verilənlər bazası idarəetmə sistemi olan dBASE ilə əlaqələndirilir. dBASE-də .str faylı adətən struktur siyahısı obyekt faylını təmsil edir. Bu fayl verilənlər bazası cədvəlinin strukturunu, o cümlədən sahələr (sütunlar) və onların xassələri haqqında məlumatları ehtiva edir.

Struktur siyahısı obyekt faylı (.str) sahə adları, məlumat növləri, sahə uzunluqları və verilənlər bazası cədvəlindəki hər bir sahə ilə əlaqəli hər hansı digər xüsusiyyətlər kimi metaməlumatlardan ibarətdir. O, faktiki məlumat qeydlərini ehtiva etmədən verilənlər bazası cədvəlinin strukturunu müəyyən etmək üçün istifadə olunur.

dBASE və ya digər verilənlər bazası idarəetmə alətləri kimi proqramlar verilənlər bazası cədvəlinin tərtibatını başa düşmək və bu struktur əsasında sorğu, yeniləmə və ya yeni qeydlər yaratmaq kimi əməliyyatları yerinə yetirmək üçün bu fayldan istifadə edə bilər.

STR faylının nəyi ehtiva edə biləcəyinin əsas nümunəsi:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Bu nümunə dörd sahədən ibarət cədvəli təsvir edir: ID, Ad, Yaş və DOB, onların müvafiq məlumat növləri və uzunluqları.

## STR faylını necə açmaq olar?

.str fayllarını açmağın əsas yolu dBASE-in özündən, xüsusən də Windows əməliyyat sistemlərində istifadə etməkdir. dBASE bu faylların məzmununu oxumağa və şərh etməyə qadirdir, istifadəçilərə verilənlər bazası strukturuna baxmaq və işləmək imkanı verir.

.str faylları verilənlər bazası strukturu haqqında məlumatları ehtiva edən sadə mətn faylları olduğundan, siz onları mətn redaktorundan istifadə etməklə də aça bilərsiniz. Mətn redaktorlarına misal olaraq Windows-da Microsoft Notepad və Mac-də Apple TextEdit proqramlarını göstərmək olar. Mətn redaktorunda açdığınız zaman siz faylın məzmununu, o cümlədən sahə adlarını, məlumat növlərini və digər struktur məlumatları insanların oxuya biləcəyi formatda görə biləcəksiniz.

## İstinadlar
* [dBase](https://en.wikipedia.org/wiki/DBase)


