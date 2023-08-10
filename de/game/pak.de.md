{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "Dateiformat", "Was ist eine PAK-Datei", "Datei", "Pak-Beispiel", "Videospiel-Paketdatei", "Erweiterung"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über .pak-Dateien und APIs, die PAK-Dateien erstellen und öffnen können.",
  "title" :"PAK-Dateiformat - Videospielpaketdatei",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
"identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Was ist eine PAK-Datei?

Eine PAK-Datei ist eine Paketdatei, die von verschiedenen Videospielen erstellt wurde, um Spieldaten zu archivieren. Im Wesentlichen ist es ein Dateiformat für Spiele. Dies kann mehrere Spielelemente wie Grafiken, Texturen, Sounds, Objekte sowie andere Spieldaten umfassen. Das Archiv wird meist als .zip-Datei gespeichert und kann mit gängiger Dekomprimierungssoftware wie WinZip und WinRAR entpackt werden. Beispiele für Videospiele, die PAK-Dateien verwenden, sind Quake, Hexen, Crysis und Half-Life.

## PAK-Dateiformat – Weitere Informationen

In den meisten Fällen werden PAK-Dateien im [ZIP-Dateiformat](/de/compression/zip/) gespeichert. Verschiedene Anwendungen können jedoch unterschiedliche Dateiformate zum Speichern dieser Dateien verwenden.


## Wie öffnet man PAK-Dateien?

Sie können PAK-Dateien mit Anwendungen wie [PakExplorer](https://www.quaketerminus.com/tools.shtml) und [SpriteExplorer](http://www.slackiller.com/hlprograms.htm) öffnen.

**------------------------------------------------------------- -------------------------------------------------- -----------------------**

## PAK-Dateiformat - Simutrans-Objektdatei

Eine Datei mit der Erweiterung .pak ist ein [Simutrans](https://www.simutrans.com/en/) Transportsimulationsspiel-Dateiformat. Es enthält Objekte, die in der Simulation verwendet werden, wie z. B. benutzerdefinierte Grafiken und Dateninhalte. Es kann mehrere verschiedene Objekte wie Spielfahrzeuge, Gebäude, Gelände usw. enthalten. PAK-Dateien werden mit MakeObject generiert, einem Dienstprogramm, das .dat-Dateien und .png-Bilder zum Erstellen dieser Simulationsobjekte kompiliert. Simutrans ermöglicht es den Spielern, ein erfolgreiches Transportsystem zu betreiben, indem sie Transportsysteme für Passagiere, Post und Waren auf dem Landweg bauen und verwalten

## Wie erstelle ich PAK-Dateien?

Simutrans hat Beispiele für die Erstellung von PAK-Dateien unter Windows und Linux aufgelistet.

### Windows-Betriebssystem

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

## Verweise

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

