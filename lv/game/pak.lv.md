{
  "date" : "2021-10-20",
  "keywords" : [ ".pak", "file format", "what is a pak file", "file", "pak example", "Video Game Package File","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Uzziniet par .pak failu un API, kas var izveidot un atvērt PAK failus.",
  "title" : "PAK faila formāts - videospēļu pakotnes fails",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak-lv",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Kas ir PAK fails?

PAK fails ir pakotnes fails, ko izveido dažādas videospēles, lai arhivētu spēļu datus. Būtībā tas ir spēles faila formāts. Tas var ietvert vairākus spēles elementus, piemēram, grafiku, faktūras, skaņas, objektus, kā arī citus spēles datus. Arhīvs galvenokārt tiek saglabāts kā .zip fails, un to var izvilkt ar populāru dekompresijas programmatūru, piemēram, WinZip un WinRAR. Videospēļu piemēri, kurās tiek izmantoti PAK faili, ir Quake, Hexen, Crysis un Half-Life.

## PAK faila formāts — vairāk informācijas

Vairumā gadījumu PAK faili tiek saglabāti mapē [ZIP file format](/compression/zip/). Taču dažādas lietojumprogrammas šo failu glabāšanai var izmantot dažādus failu formātus.


## Kā atvērt PAK failus?

PAK failus var atvērt ar tādām lietojumprogrammām kā [PakExplorer](https://www.quaketerminus.com/tools.shtml) un [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- -----------------------**

## PAK faila formāts — Simutrans objekta fails

Fails ar paplašinājumu .pak ir [Simutrans](https://www.simutrans.com/en/) transporta simulācijas spēles faila formāts. Tajā ir simulācijā izmantotie objekti, piemēram, lietotāja veidota grafika un datu saturs. Tam var būt vairāki dažādi objekti, piemēram, spēļu transportlīdzekļi, ēkas, reljefs utt. PAK faili tiek ģenerēti, izmantojot MakeObject — utilītu, kas apkopo .dat failus un .png attēlus šo simulācijas objektu izveidei. Simutrans ļauj spēlētājiem vadīt veiksmīgu transporta sistēmu, veidojot un pārvaldot transporta sistēmas pasažieriem, pastam un precēm pa sauszemi

## Kā izveidot PAK failus?

Simutrans ir uzskaitījis piemērus PAK failu izveidei operētājsistēmās Windows un Linux OS.

### Windows OS

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

## Atsauces

 * [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

