
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADS Faylı - Ada Spesifikasiya Fayl Formatı",
  "description":"Nümunə və ADS fayllarını yarada və aça bilən API ilə ADS fayl formatının nə olduğunu öyrənin.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads-az",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## ADS faylı nədir?

ADS faylı Ada proqramlaşdırma layihəsi üçün spesifikasiya faylıdır. Java üçün sinifə və ya C++ vəziyyətində başlıq və tətbiq cütlüyünə bənzəyir. Ada paketinin ictimai və özəl xüsusiyyətləri .ads faylında saxlanılır. .adb faylı, əksinə, icra və ya Ada orqanlarını ehtiva edir. [C++](/programming/cpp/) kimi, Ada da OOP-dən asılı olmayaraq spesifikasiyalar və tətbiqlər arasında ayırma təklif edir.

ADS faylları Microsoft Notepad, Notepad++ və Atom kimi istənilən mətn redaktorunda açıla bilər.

## ADS fayl formatı

ADS faylları sadə düz mətn faylı formatındadır və istənilən mətn redaktoru ilə açıla/redaktə edilə bilər. Ada paketləri iyerarxiyalara bölünə bilər. Uşaq vahidi aşağıdakı şəkildə elan edilə bilər:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## İstinadlar

 * [Ada Paketləri](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

