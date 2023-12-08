{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "filformat", "vad är en pakfil", "fil", "pakexempel", "videospelspaketfil","tillägg"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om .pak-filer och API:er som kan skapa och öppna PAK-filer.",
  "title" :"PAK-filformat - videospelspaketfil",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Vad är en PAK fil?

En PAK-fil är en paketfil som skapats av olika videospel för att arkivera speldata. I huvudsak är det ett spelfilformat. Detta kan inkludera flera spelelement som grafik, texturer, ljud, objekt, tillsammans med annan speldata. Arkivet sparas mestadels som .zip-fil och kan extraheras med populära dekompressionsprogram som WinZip och WinRAR. Exempel på videospel som använder PAK-filer inkluderar Quake, Hexen, Crysis och Half-Life.

## PAK-filformat - Mer information

I de flesta fall sparas PAK-filer i [ZIP-filformat](/sv/compression/zip/). Men olika program kan använda olika filformat för att lagra dessa filer.


## Hur öppnar man PAK filer?

Du kan öppna PAK-filer med applikationer som [PakExplorer](https://www.quaketerminus.com/tools.shtml) och [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- ----------------------------**

## PAK-filformat - Simutrans-objektfil

En fil med .pak-förlängningen är ett [Simutrans](https://www.simutrans.com/en/) filformat för transportsimuleringsspel. Den innehåller objekt som används i simuleringen såsom användargjord grafik och datainnehåll. Den kan ha flera olika objekt som spelfordon, byggnader, terräng etc. PAK-filer genereras med MakeObject, ett verktyg som kompilerar .dat-filer och .png-bilder för att skapa dessa simuleringsobjekt. Simutrans låter spelarna driva ett framgångsrikt transportsystem genom att konstruera och hantera transportsystem för passagerare, post och gods på land

## Hur skapar man PAK-filer?

Simutrans har listat exempel på hur man skapar PAK-filer på Windows och Linux OS.

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

## Referenser

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)
