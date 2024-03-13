{
  "date": "2021-07-08",
  "keywords": [
"SYS",
"uzadılması",
"fayl",
"format",
"sistemi",
"Sürücü",
"Sistem faylı",
"proqramlar",
"kompüter",
"tətbiq"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "SYS - Sistem Fayl Formatı",
  "description": "SYS fayl formatı və SYS fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "SYS",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sy-azs"
}
},
  "lastmod": "2021-07-08"
}

## SYS faylı nədir? ##

SYS faylları Windows OS və MS-DOS proqramlarında istifadə olunan Sistem fayllarıdır. Bu fayllar birbaşa açıla bilməz və sürücüdən və cihazın konfiqurasiyasından ibarətdir. SYS faylları əməliyyat sisteminin əsas funksiyalarının fayllarını ehtiva etməkdən məsuldur. Bunlar cihaz sürücüsünün kritik faylları hesab olunur və yarış sürücüsü ilə bağlı hər hansı bir məsələnin həlli lazım olduqda istifadə edilə bilər. Bunlar kompüter sisteminin düzgün işləməsinə cavabdehdir və .sys faylları düzgün və tam olmalıdır.


## Texniki Spesifikasiya ##

.sys faylları əslində [BMP](/image/bmp/) formatının alt çoxluğudur, çünki o, yalnız xüsusi birləşmələrə icazə verir. Bu faylların adi formatı LOGOS.SYS, LOGOW.SYS və LOGO.SYS kimidir. Hər hansı digər faylda bu format yoxdur.

Bu fayllar quraşdırma zamanı əsasən Windows-un *C* kataloqunda istifadə olunur. Cihaz drayverləri ətrafında fırlanan problemlərin əksəriyyəti Windows əməliyyat sisteminin yenilənməsi ilə həll olunur. Bu faylların təfərrüatlarına və məlumatlarına Windows OS-nin daxili proqramlarından istifadə etməklə baxmaq olar. Bunlar həm də əməliyyat sistemindəki müxtəlif modullara istinadlardan ibarətdir.
Sistem fayllarının bəzi nümunələri bunlardır:

* IO.SYS (Bu disk əməliyyat sisteminin cihaz drayverlərini saxlayır)

* MSDOS.SYS (Bunlarda kernel və ya əməliyyat sisteminin əsas kodu var)

* CONFIG.SYS (Bunlarda müxtəlif konfiqurasiya seçimləri var)

* KEYBOARD.SYS (Bunlarda klaviatura düzümü ilə bağlı məlumatlar var) 

* COUNTRY.SYS (Bu, ölkə və kod səhifəsi ilə əlaqəli məlumat)


## SYS Fayl Format ##

Microsoft faylları .sys uzantıları ilə hazırlayıb. Dəyişənlər və funksiyalar SYS fayllarına daxil edilir. Bunlar əsasən Microsoft əməliyyat sistemi tərəfindən istifadə olunur. Bu fayllar əsasən diskin kök kataloqunda yerləşir:

* C: \ Windows \ system32 \ sürücülər

* C:\Windows\WinSxS


SYS faylları ilə bağlı bəzi ümumi xəbərdarlıqlar aşağıdakılardır:

* Bu faylların adları dəyişdirilməməlidir, çünki bu fayllar əməliyyat sisteminin əsas funksiyaları və dəyişənləri üçün cavabdehdir.
* Bu fayllar silinməməlidir, çünki onların bu faylların olmaması xətalara səbəb ola bilər
* Mənbənin qanuniliyinə əmin olana qədər .sys faylları internetdən endirilməməlidir.
* Bu fayllarla qarışmaq olmaz, çünki onları dəyişdirmək və ya bunlarla qarışmaq ciddi sistem xətalarına səbəb olur
* Əgər bu fayllar bəzi virus və ya zərərli proqram tərəfindən zədələnirsə, onlar yenidən quraşdırılmalıdır

## SYS Nümunəsi ##

Aşağıdakı sadə SYS sistem konfiqurasiya faylının nümunəsidir:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
