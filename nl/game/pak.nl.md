{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "bestandsindeling", "wat is een pakbestand", "bestand", "pakvoorbeeld", "Videogamepakketbestand","extensie"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over .pak-bestanden en API's die PAK-bestanden kunnen maken en openen.",
  "title" :"PAK-bestandsindeling - Videogamepakketbestand",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Wat is een PAK-bestand?

Een PAK-bestand is een pakketbestand dat door verschillende videogames is gemaakt om gamegegevens te archiveren. In wezen is het een bestandsindeling voor games. Dit kan meerdere game-elementen bevatten, zoals afbeeldingen, texturen, geluiden, objecten en andere gamegegevens. Het archief wordt meestal opgeslagen als .zip-bestand en kan worden uitgepakt met populaire decompressiesoftware zoals WinZip en WinRAR. Voorbeelden van videogames die PAK-bestanden gebruiken, zijn Quake, Hexen, Crysis en Half-Life.

## PAK-bestandsindeling - Meer informatie

In de meeste gevallen worden PAK-bestanden opgeslagen in [ZIP-bestandsformaat](/nl/compression/zip/). Maar verschillende toepassingen kunnen verschillende bestandsindelingen gebruiken om deze bestanden op te slaan.


## Hoe PAK-bestanden openen?

U kunt PAK-bestanden openen met toepassingen zoals [PakExplorer](https://www.quaketerminus.com/tools.shtml) en [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- -----------------------**

## PAK-bestandsindeling - Simutrans-objectbestand

Een bestand met de extensie .pak is een [Simutrans](https://www.simutrans.com/en/) bestandsformaat voor transportsimulatiegames. Het bevat objecten die in de simulatie worden gebruikt, zoals door de gebruiker gemaakte afbeeldingen en gegevensinhoud. Het kan verschillende objecten hebben, zoals game-voertuigen, gebouwen, terrein, enz. PAK-bestanden worden gegenereerd met MakeObject, een hulpprogramma dat .dat-bestanden en .png-afbeeldingen compileert voor het maken van deze simulatie-objecten. Simutrans laat de spelers een succesvol transportsysteem runnen door transportsystemen voor passagiers, post en goederen over land te bouwen en te beheren

## Hoe PAK-bestanden maken?

Simutrans heeft voorbeeldvoorbeelden gegeven voor het maken van PAK-bestanden op Windows en Linux OS.

### Windows-besturingssysteem

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

## Referenties

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

