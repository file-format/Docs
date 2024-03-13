{
  "date" : "2021-10-20",
  "keywords" : [ ".pak", "file format", "what is a pak file", "file", "pak example", "Video Game Package File","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"PAK faylları yarada və aça bilən .pak faylı və API-lər haqqında məlumat əldə edin.",
  "title" : "PAK Fayl Format - Video Oyun Paket Faylı",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak-az",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## PAK faylı nədir?

PAK faylı oyun məlumatlarını arxivləşdirmək üçün müxtəlif video oyunları tərəfindən yaradılmış paket faylıdır. Əslində, bu bir oyun fayl formatıdır. Buraya digər oyun məlumatları ilə yanaşı, qrafika, tekstura, səslər, obyektlər kimi çoxlu oyun elementləri daxil ola bilər. Arxiv əsasən .zip faylı kimi saxlanılır və onu WinZip və WinRAR kimi məşhur dekompressiya proqramı ilə çıxarmaq olar. PAK fayllarından istifadə edən video oyunların nümunələrinə Quake, Hexen, Crysis və Half-Life daxildir.

## PAK Fayl Format - Ətraflı Məlumat

Əksər hallarda PAK faylları [ZIP file format](/compression/zip/)-də saxlanılır. Lakin müxtəlif proqramlar bu faylları saxlamaq üçün fərqli fayl formatından istifadə edə bilər.


## PAK fayllarını necə açmaq olar?

PAK fayllarını [PakExplorer](https://www.quaketerminus.com/tools.shtml) və [SpriteExplorer](http://www.slackiller.com/hlprograms.htm) kimi proqramlarla aça bilərsiniz.

**------------------------------------------------ ------------------------------------------------- ----------------------------------

## PAK Fayl Format - Simutrans Obyekt Faylı

.pak uzantısı olan fayl [Simutrans](https://www.simutrans.com/en/) nəqliyyat simulyasiya oyunu fayl formatıdır. O, istifadəçi tərəfindən hazırlanmış qrafika və məlumat məzmunu kimi simulyasiyada istifadə olunan obyektləri ehtiva edir. O, oyun vasitələri, binalar, ərazi və s. kimi bir neçə fərqli obyektə malik ola bilər. PAK faylları bu simulyasiya obyektlərini yaratmaq üçün .dat faylları və .png şəkillərini tərtib edən MakeObject yardım proqramı ilə yaradılır. Simutrans, oyunçulara sərnişinlər, poçt və mallar üçün quru nəqliyyat sistemləri quraraq və idarə etməklə uğurlu nəqliyyat sistemini idarə etməyə imkan verir.

## PAK faylları necə yaradılır?

Simutrans Windows və Linux OS-də PAK faylları yaratmaq üçün nümunə nümunələri sadaladı.

### Windows əməliyyat sistemi

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## İstinadlar

 * [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

