{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "formát souboru", "co je soubor pak", "soubor", "příklad pak", "soubor balíčku videohry","přípona"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o souboru .pak a rozhraních API, která mohou vytvářet a otevírat soubory PAK.",
  "title" :"PAK File Format - Video Game Package File",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Co je soubor PAK?

Soubor PAK je soubor balíčku vytvořený různými videohrami k archivaci herních dat. V podstatě je to formát souboru hry. To může zahrnovat více herních prvků, jako je grafika, textury, zvuky, předměty, spolu s dalšími herními daty. Archiv je většinou uložen jako soubor .zip a lze jej extrahovat pomocí oblíbeného dekompresního softwaru, jako je WinZip a WinRAR. Příklady videoher využívajících soubory PAK zahrnují Quake, Hexen, Crysis a Half-Life.

## Formát souboru PAK – Další informace

Ve většině případů se soubory PAK ukládají ve [formát souboru ZIP](/cs/compression/zip/). Různé aplikace však mohou používat různé formáty souborů pro ukládání těchto souborů.


## Jak otevřít soubory PAK?

Soubory PAK můžete otevřít pomocí aplikací, jako je [PakExplorer](https://www.quaketerminus.com/tools.shtml) a [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- ------------------------**

## Formát souboru PAK - Objektový soubor Simutrans

Soubor s příponou .pak je formát souboru hry simulující dopravu [Simutrans](https://www.simutrans.com/en/). Obsahuje objekty používané v simulaci, jako je uživatelská grafika a datový obsah. Může mít několik různých objektů, jako jsou herní vozidla, budovy, terén atd. Soubory PAK se generují pomocí nástroje MakeObject, který kompiluje soubory .dat a obrázky .png pro vytváření těchto simulačních objektů. Simutrans umožňuje hráčům provozovat úspěšný dopravní systém budováním a řízením dopravních systémů pro cestující, poštu a zboží po zemi.

## Jak vytvořit soubory PAK?

Simutrans uvedl ukázkové příklady pro vytváření souborů PAK v OS Windows a Linux.

### OS Windows

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

## Reference

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)
