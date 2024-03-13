{
  "date": "2022-04-25",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "AHK fayl formatı və AHK fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "AHK Fayl Format - AutoHotkey Skript Faylı",
  "linktitle": "AHK",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ah-azk"
}
},
  "lastmod": "2022-04-25"
}

## AHK faylı nədir?

AHK faylı Microsoft Windows-da tapşırıqların avtomatlaşdırılması üçün istifadə olunan AutoHotkey proqram təminatı ilə yaradılan skript faylıdır. Bu, ani hərəkətləri yerinə yetirmək üçün istifadə edilə bilən qısa yol düymələrindən istifadə edərək tapşırıqların avtomatlaşdırılması üçün təlimatları ehtiva edir. Fayl AutoHotkey tərəfindən icra edilir və bütün hərəkətlər ardıcıl olaraq yerinə yetirilir. AHK faylları isti düymələrdən istifadə edərək müəyyən edilmiş isti düymələrdən istifadə edərək mürəkkəb tapşırıqları yerinə yetirmək üçün kifayət qədər güclüdür. AHK faylları Microsoft Notepad və Notepad++ kimi mətn redaktorları ilə açıla bilər.

## AHK fayl formatı

AHK faylları diskdə düz mətn faylları kimi saxlanılır və AutoHotkey tərəfindən icra edilə bilən kod sətirlərini ehtiva edir. AutoHotkey pulsuz, açıq mənbəli skript dilidir və istifadəçilərə forma doldurucular, avtomatik klikləmə, makroların icrası və s. kimi hərəkətləri yerinə yetirmək üçün sadədən mürəkkəbə qədər skriptlər yaratmağa imkan verir. Minimum AHK faylı bir hərəkəti yerinə yetirib sonra çıxa bilər. .

AHK-nı [Exe](/executable/exe/) fayllarına çevirmək üçün istifadə edilə bilən alətlər mövcuddur.

### AHK Nümunəsi

Aşağıdakı nümunə Microsoft Notepad-i işə salmaq və ya artıq işləyirsə, onu önünə gətirmək üçün Win+Z düymələrindən istifadə edir.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## AHK faylını necə yarada bilərəm?

AHK faylı yaratmaq üçün aşağıdakı addımlardan istifadə edilə bilər. Bunlar hesab edir ki, AutoHotkey artıq maşında quraşdırılıb.

* Masaüstünüzdə sağ klikləyin.

* Menyuda "Yeni" tapın.

* "Yeni" menyusunda "AutoHotkey Skripti" üzərinə klikləyin.

* Ssenariyə yeni ad verin.

* İş masanızda yeni yaradılmış faylı tapın və üzərinə sağ klikləyin.

* "Skripti redaktə et" düyməsini basın.

* Bir pəncərə açılmalı idi, yəqin ki, Notepad.

* Faylı saxla.


## İstinadlar

* [AutoHotkey](https://www.autohotkey.com/)

* [Paket faylı - Wikipewdia tərəfindən](https://en.wikipedia.org/wiki/Batch_file)


