{
  "date" : "2021-10-20",
  "keywords" : [ ".pak", "file format", "what is a pak file", "file", "pak example", "Video Game Package File","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om .pak-filer og API'er, der kan oprette og åbne PAK-filer.",
  "title" : "PAK-filformat - videospilpakkefil",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak-da",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Hvad er PAK fil?

En PAK-fil er en pakkefil oprettet af forskellige videospil til at arkivere spildata. Grundlæggende er det et spilfilformat. Dette kan omfatte flere spilelementer såsom grafik, teksturer, lyde, objekter sammen med andre spildata. Arkivet gemmes for det meste som .zip-fil og kan udpakkes med populær dekompressionssoftware som WinZip og WinRAR. Eksempler på videospil, der bruger PAK-filer, omfatter Quake, Hexen, Crysis og Half-Life.

## PAK-filformat - flere oplysninger

I de fleste tilfælde gemmes PAK-filer i [ZIP file format](/compression/zip/). Men forskellige programmer kan bruge forskellige filformater til at gemme disse filer.


## Hvordan åbner jeg PAK filer?

Du kan åbne PAK-filer med programmer såsom [PakExplorer](https://www.quaketerminus.com/tools.shtml) og [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- ----------------------------**

## PAK-filformat - Simutrans-objektfil

En fil med .pak-udvidelsen er et [Simutrans](https://www.simutrans.com/en/)-transportsimuleringsspil-filformat. Den indeholder objekter, der bruges i simuleringen, såsom brugerlavet grafik og dataindhold. Det kan have flere forskellige objekter såsom spilkøretøjer, bygninger, terræn osv. PAK-filer genereres ved hjælp af MakeObject, et værktøj, der kompilerer .dat-filer og .png-billeder til at skabe disse simuleringsobjekter. Simutrans lader spillerne drive et succesfuldt transportsystem ved at konstruere og administrere transportsystemer til passagerer, post og gods på land.

## Hvordan opretter man PAK-filer?

Simutrans har listet eksempler på, hvordan du kan oprette PAK-filer på Windows og Linux OS.

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

## Referencer

 * [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

