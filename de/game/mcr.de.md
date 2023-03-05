{
  "date" : "2022-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das MCR-Dateiformat und APIs, die MCR-Dateien erstellen und öffnen können.",
  "title" :"MCR - Minecraft-Regionsdateiformat",
  "linktitle" : "MCR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2022-12-14"
}

## Was ist eine MCR-Datei?

Das Minecraft MCR-Dateiformat ist ein Datenformat, das von Minecraft verwendet wird, um Geländestücke einer Minecraft-Welt zu speichern. Es basiert auf dem NBT-Format (Named Binary Tag), das von den Entwicklern der beliebten Open-Source-Game-Engine Minecraft Forge entwickelt wurde. Der MCR-Dateityp wurde ganz am Anfang eingeführt und später durch das [MCA-Dateiformat](/de/game/mca/) ersetzt.

## MCR-Dateiformat

Das MCR-Dateiformat ist als eine Reihe benannter binärer Tags strukturiert, von denen jedes einen bestimmten Datentyp enthält. Das Top-Level-Tag ist das "Level"-Tag, das alle Daten für ein einzelnes Spiellevel enthält. Innerhalb des Level-Tags gibt es mehrere andere benannte Tags, die verschiedene Arten von Daten speichern, z. B. das „Data“-Tag, das Informationen über die Spielwelt speichert, und die „Entities“- und „TileEntities“-Tags, die Daten über die Spielobjekte bzw. Kacheleinheiten in der Welt.

## Was ist im MCR-Dateiformat enthalten?

Im Minecraft-MCR-Dateiformat ist eine Region ein 32x32-Blockbereich der Spielwelt. Das MCR-Format unterteilt die Spielwelt in Regionen, um die Daten effizienter zu verwalten und ein schnelleres Laden und Speichern von Spielleveln zu ermöglichen. Jede Region wird in einer separaten Datei gespeichert, und das MCR-Dateiformat verwendet ein Koordinatensystem, um die Position jeder Region innerhalb der Spielwelt zu identifizieren. Die Koordinaten einer Region werden durch die Blockkoordinaten der unteren linken Ecke der Region bestimmt. Beispielsweise würde eine Region mit den Koordinaten (-1,0) eine Region links und null Regionen unterhalb des Ursprungs der Spielwelt liegen.

## Spezifikationen des MCR-Dateiformats

Die Spezifikationen des MCR-Dateiformats sind öffentlich verfügbar. Die Spezifikationen für das NBT-Format, auf dem das MCR-Format basiert, sind auf der Website von Minecraft Forge verfügbar. Darüber hinaus enthält das [Minecraft-Wiki](https://minecraft.fandom.com/wiki/Region_file_format) auch detaillierte Informationen über das MCR-Dateiformat, einschließlich seiner Struktur und der verschiedenen unterstützten Datentypen.

### Komprimierte Daten in MCR-Dateien

Das Minecraft MCR-Dateiformat unterstützt die Komprimierung. Das MCR-Dateiformat basiert auf dem [NBT-Format](https://minecraft.fandom.com/wiki/NBT_format), das es ermöglicht, Daten in komprimierter Form zu speichern. Dies trägt dazu bei, die Größe von MCR-Dateien zu reduzieren und sie effizienter zu übertragen und zu speichern. Dies ist ein wichtiges Merkmal des MCR-Dateiformats, da es Spielern ermöglicht, große Geländedaten von Minecraft World mit anderen zu teilen.

## Verweise

* [Welteditor für Minecraft](https://www.mcedit.net/)
* [Über Minecraft](https://www.minecraft.net/en-us)
* [Dateiformat der Region](https://minecraft.fandom.com/wiki/Region_file_format)
* [NBT-Format](https://minecraft.fandom.com/wiki/NBT_format)

