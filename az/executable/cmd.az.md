{
  "date": "2021-07-12",
  "keywords": [
"cmd faylı",
"cmd faylı nədir",
"fayl",
"cmd nümunəsi",
"cmd fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "CMD faylları yarada və aça bilən CMD fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "CMD - Windows əmr faylı formatı",
  "linktitle": "CMD",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cm-azd"
}
},
  "lastmod": "2021-07-12"
}

## CMD faylı nədir?
CMD faylı müxtəlif tapşırıqları yerinə yetirmək üçün icra edilən düz mətn şəklində bir və ya bir neçə əmrdən ibarət skriptdən ibarətdir. O, adətən icra edilə bilən əmrlər toplusunu saxlamaq üçün istifadə edilən [BAT](/executable/bat/) faylına bənzəyir. CMD faylları Microsoft Windows əməliyyat sistemində geniş istifadə olunur. Bu fayllar demək olar ki, 90-cı illərdə təqdim edildi, lakin hələ də ən son Windows əməliyyat sistemində istifadə olunur. Bu fayllar ümumiyyətlə ardıcıllıqla birdən çox əmri yerinə yetirmək üçün yazılır.

## CMD fayl formatı
CMD CP/M tipli icra edilə bilən proqramlar tərəfindən istifadə olunan fayl formatıdır. O, ümumiyyətlə CP/M-80-də [COM](/executable/com/) və DOS-da [EXE](/executable/exe/) ilə müqayisə edilir. CMD faylı 1-8 qrup kod və ya məlumat və 128 bayt başlıqdan ibarətdir. Hər qrupun ölçüsü 1 mb-ə qədər ola bilər. CMD faylları həmçinin onun sonrakı versiyalarında yerdəyişmə məlumatlarını və Rezident Sistem Genişləndirmələrini (RSXs) ehtiva edə bilər. CMD [BAT](/executable/bat/) faylı ilə müqayisədə yenidir; MS-DOS-da pəncərələrin buraxılmasından əvvəl MS-DOS üçün istifadə edilmişdir. Baxmayaraq ki, siz hələ də .bat uzantılı faylları saxlaya bilsəniz, bir çox insanlar icra olunan skriptlərini saxlamaq üçün .cmd uzantısından istifadə edirlər.

### CMD formatının spesifikasiyası

Başlığın başlanğıcı faylda mövcud qrupların siyahısını və növlərini ehtiva edir. Hər növ ən çox bir dəfə istifadə edilə bilər. Bu növlər bunlardır:

- Kod
- Məlumat
- Əlavə
- Yığın
- İstifadəçi 1
- İstifadəçi 2
- İstifadəçi 3
- İstifadəçi 4
- Paylaşılan Kod

Eynilə DOS-da Proqram Seqmenti Prefiksi, verilənlər qrupunun ilk 256 baytı sıfırdır. Onlar CP/M-86 tərəfindən sıfır səhifə ilə doldurulacaq. Əgər məlumat qrupu yoxdursa, onun əvəzinə kod qrupunun ilk 256 baytı istifadə olunacaq.
## CMD fayl nümunəsi
Aşağıda sistem məlumatlarını göstərmək üçün CMD skriptinin nümunəsi verilmişdir.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## İstinadlar 

* [CMD Skriptini Necə Yazmaq olar](https://smallbusiness.chron.com/write-cmd-script-53226.html)

* [CMD faylı (CP/M) - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/CMD_file_(CP/M))


