{
  "date": "2022-05-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "PYC faylları yarada və aça bilən PYC fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "PYC Fayl Format - Python tərəfindən tərtib edilmiş fayl",
  "linktitle": "PYC",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-py-azc"
}
},
  "lastmod": "2022-05-09"
}

## PYC faylı nədir?

PYC faylı Python proqramlaşdırma dilində yazılmış mənbə kodundan yaradılan tərtib edilmiş çıxış faylıdır. PY faylı Python tərcüməçisi ilə işlədildikdə, icra üçün bayt koduna çevrilir. Eyni zamanda, tərtib edilmiş baytkod da .pyc faylı kimi saxlanılır ki, mümkün olduqda daha sonra keşdən yenidən istifadə olunsun.

## PYC Fayl Formatının Strukturu

PYC faylları bayt kodundadır və onların fayl formatı spesifikasiyası ictimaiyyətə açıq deyil. Bununla belə, bəzi mənbələrin araşdırması göstərir ki, [structure of a PYC file](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) aşağıdakılardan ibarətdir:

 * `Dörd baytlıq sehrli nömrə` - Sıralama koduna hər dəyişikliklə dəyişən sadəcə iki bayt və sonra iki bayt 0d0a.
 * `Dörd baytlıq modifikasiya vaxt damğası` - .pyc-ni yaradan mənbə faylının Unix modifikasiya vaxt damğası, beləliklə, mənbə dəyişdikdə onu yenidən tərtib etmək olar.
 * `Bir sıralanmış kod obyekti` - mənbə faylının kompilyasiyasının nəticəsi olan kod obyektinin marshal.dump çıxışı.

## Tez-tez verilən suallar

1. **PYC faylı necə yaradılır?** Python mənbə kodu Python tərcüməçisindən istifadə etməklə tərtib edildikdə PYC faylı yaradılır. Sonra tərtib edilmiş kod PYC faylında saxlanılır.

1. **PYC py-dən daha sürətlidir?** PYC faylları python mənbə kodu tərtib edildikdən sonra saxlanılır. Bunlar artıq şərh edildiyi üçün bu fayllar .py fayllarından daha sürətlidir.

1. **py və pyc faylı arasında fərq nədir?** PY fayllarında proqram üçün Python mənbə kodu faylı, .pyc fayllarında isə tətbiqin şərh edilmiş bayt kodu var.

1. **PYC ikili fayldırmı?** Bəli, PYC faylı 4 baytlıq sehrli nömrə, 4 baytlıq modifikasiya vaxt damğası və sıralanmış kod obyektindən ibarət ikili fayldır.

1. **Biz .pyc-ni .py-ə çevirə bilərik?** Bəli, pyc fayllarını py-yə çevirmək mümkündür. Decompyle++ kimi dekompilyatorlar tərtib edilmiş Python bayt kodunu yenidən etibarlı və insan tərəfindən oxuna bilən Python mənbə koduna tərcümə etmək üçün istifadə edilə bilər.

## İstinadlar

* [.pyc fayllarının strukturu](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)


