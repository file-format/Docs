{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AGI Fayl - Asterisk Gateway Interface Fayl Format",
  "description":"AGI faylları yarada və aça bilən nümunə və API-lərlə AGI fayl formatının nə olduğunu öyrənin.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi-az",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## What is an AGI file?

AGI faylı açıq mənbəli telefoniya sistemi Asterisk tərəfindən istifadə edilən skript faylıdır. O, prosesləri avtomatlaşdırmaq üçün istifadə edilə bilən məlumatları və Ulduz dialplanını ehtiva edir. AGI skript fayllarından istifadə edərək PostgreSQL və ya MySQL kimi əlaqəli verilənlər bazaları ilə əlaqələr qurmaq olar. Bundan əlavə, AGI skriptləri digər xarici resurslara daxil olmaq üçün də istifadə edilə bilər. AGI skriptləri dialplana nəzarəti xarici AGI skriptinə təhvil verə bilər və Asterisk-ə mürəkkəb tapşırıqları yerinə yetirməyə imkan verir.

## AGI Fayl Format - Ətraflı Məlumat

AGI skript faylları mətn faylları kimi saxlanılır və dəyişiklik etmək üçün istənilən mətn redaktorunda açıla bilər.

### AGI Rabitə Standart Modeli

AGI skripti Asterisk tərəfindən ona göndərilən dəyişənləri və onların dəyərlərini yükləyir. Bu dəyişənlərin ümumi görünüşü aşağıdakı kimidir.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Bu dəyişənlərdən sonra Asterisk tərəfindən göndərilən boş sətir AGI skriptinin indi dialplana nəzarət edə biləcəyini göstərir.

### AGI Skript Faylları üçün proqramlaşdırma dili

AGI skriptləri adətən Perl, [PHP](/programming/php/), [C](/programming/c/), Pascal və ya Bourne Shell dillərində yazıla bilər.

## İstinadlar

 * [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

