{
"Datum": "27.09.2023",
  "keywords": [
"cfg",
"cfg-Datei",
"cfg mame-Konfigurationsdatei",
"Was ist eine CFG-Datei",
"Wie öffnet man eine CFG-Datei",
"Datei",
"cfg-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CFG-Dateiformat – MAME-Konfigurationsdatei",
  "description":"Erfahren Sie mehr über das CFG MAME-Konfigurationsdateiformat und die APIs, mit denen CFG-Dateien erstellt und geöffnet werden können.",
"linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
"parent": "Einstellungen"
}
},
"lastmod": "27.09.2023"
}

## Was ist eine CFG-Datei?

Die CFG-Datei ist eine XML-Tastaturkonfigurationsdatei, die von MAME-Arcade-Videospiel-Emulatoren verwendet wird. Es ist eine entscheidende Komponente für die Anpassung von Tastatursteuerungen und Hotkeys an die Vorlieben des Spielers. In diesen Dateien werden Zuordnungen und Einstellungen gespeichert, die bestimmen, wie die Tastatur beim Spielen mit dem Emulator interagiert. Durch Bearbeiten dieser Datei können Benutzer ihr Spielerlebnis individuell anpassen, indem sie bestimmte Tastaturtasten Aktionen im Spiel zuweisen, z. B. Münzeinwurf, Start, Bewegung und verschiedene andere Funktionen.

## MAME-Konfigurationsdatei

MAME, was für **Multiple Arcade Machine Emulator** steht, ist eine Softwareanwendung, mit der Sie Arcade-Spiele auf Ihrem Computer emulieren und spielen können. MAME verwendet Konfigurationsdateien, um sein Verhalten und seine Einstellungen anzupassen. Diese Konfigurationsdateien befinden sich normalerweise im Ordner "cfg" in Ihrem MAME-Verzeichnis.

Hier sind die wichtigsten Konfigurationsdateien, auf die Sie beim Einrichten und Konfigurieren von MAME stoßen können:

1. **mame.ini:** Dies ist die Hauptkonfigurationsdatei für MAME. Es enthält globale Einstellungen, die für alle Spiele gelten. Sie finden diese Datei im Stammverzeichnis Ihrer MAME-Installation.

1. **default.cfg:** In dieser Datei werden Standardeinstellungen für alle Spiele gespeichert, die keine eigenen Konfigurationsdateien haben. Es wird als Fallback für spielspezifische Einstellungen verwendet.

1. **spielspezifische.cfg:** Diese Dateien werden zum Speichern von Einstellungen für einzelne Spiele verwendet. Sie werden normalerweise nach der ROM-Datei des Spiels benannt, dem sie entsprechen. Wenn Sie beispielsweise ein Spiel namens "pacman.zip" haben, lautet die Konfigurationsdatei dafür "pacman.cfg".

Hier sind einige allgemeine Einstellungen, die Sie möglicherweise in der MAME-Konfigurationsdatei finden.

1. **rompath:** Gibt das Verzeichnis an, in dem sich Ihre Arcade-Spiel-ROMs befinden.

1. **cfg_directory:** Gibt das Verzeichnis an, in dem spielspezifische Konfigurationsdateien gespeichert werden.

1. **nvram_directory:** Gibt das Verzeichnis an, in dem nichtflüchtige RAM-Dateien (NVRAM) gespeichert werden. NVRAM speichert Highscores und andere spielspezifische Daten.

1. **Artwork-Verzeichnis:** Gibt das Verzeichnis an, in dem Grafikdateien (z. B. Rahmen, Laufschrift und Flyer) gespeichert werden.

1. **Samplepath:** Gibt das Verzeichnis an, in dem sich Beispielsounddateien befinden.

1. **Cheatpfad:** Gibt das Verzeichnis an, in dem sich Cheat-Dateien befinden.

Sie können auch verschiedene andere Einstellungen konfigurieren, z. B. Video- und Audiooptionen, Steuerelemente und Eingabegeräte. Um diese Einstellungen zu ändern, können Sie die Konfigurationsdatei im Texteditor öffnen und die erforderlichen Änderungen vornehmen.

## MAME

MAME, was für **"Multiple Arcade Machine Emulator"** steht, ist eine Softwareanwendung, die entwickelt wurde, um die Hardware von Vintage-Arcade-Automaten und Arcade-Spielkonsolen zu emulieren und zu reproduzieren. Es ermöglicht Benutzern, eine umfangreiche Bibliothek klassischer Arcade-Spiele auf modernen Computern und anderen kompatiblen Geräten zu spielen. MAME ist ein Open-Source-Projekt und hat sich zu einem beliebten Emulator entwickelt, um die reiche Geschichte des Arcade-Gamings zu bewahren und zu genießen.

1. **Emulation:** Der Hauptzweck von MAME besteht darin, die Hardware von Arcade-Automaten genau zu emulieren, einschließlich ihrer Zentraleinheiten (CPUs), Soundchips, Grafikchips und Eingabegeräte. Dieses Maß an Genauigkeit stellt sicher, dass sich die Spiele so nah wie möglich an das ursprüngliche Arcade-Erlebnis verhalten.

1. **Kompatibilität:** MAME unterstützt eine Vielzahl von Arcade-Spiel-ROMs und ist damit einer der umfassendsten Arcade-Emulatoren auf dem Markt. Es kann Spiele von verschiedenen Arcade-Plattformen ausführen, darunter klassische Spiele aus den 70er, 80er und 90er Jahren und sogar einige neuere Arcade-Titel.

1. **Bewahrung:** Eine der Hauptaufgaben von MAME ist die Bewahrung der Geschichte des Arcade-Gamings. Durch die genaue Emulation von Arcade-Hardware trägt MAME dazu bei, den Verlust klassischer Spiele zu verhindern und sicherzustellen, dass zukünftige Generationen sie so erleben können, wie sie ursprünglich gedacht waren.

1. **Frontends:** Viele Benutzer nutzen Frontend-Anwendungen, die eine grafische Oberfläche zum Verwalten und Starten von Spielen über MAME bieten. Diese Frontends erleichtern die Navigation in der umfangreichen Spielebibliothek von MAME.

## Wie öffne ich eine CFG-Datei?

Programme, die CFG-Dateien öffnen oder darauf verweisen

- MAME (Kostenlos) (Windows)
- ExtraMAME (Testversion)
- MacMAME (MAC)

## Andere CFG-Dateien

Hier sind andere Dateitypen, die die Dateierweiterung **.cfg** verwenden.

**Einstellungen**
- [CFG – Celestia-Konfigurationsdatei](/settings/cfg-celestia/)
- [CFG – Citrix Server-Verbindungsdatei](/settings/cfg-citrix/)
- [CFG – MAME-Konfigurationsdatei](/settings/cfg-mame/)
- [CFG – LightWave-Konfigurationsdatei](/settings/cfg-lightwave/)

**Spiel**
- [CFG – Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG – MUGEN-Konfigurationsdatei](/game/cfg-mugen/)
- [CFG – Quell-Engine-Konfigurationsdatei](/game/cfg-sourceengine/)

**System & Sonstiges**
- [CFG – CFG-Datei](/system/cfg/)
- [CFG – Cal3D-Modellkonfigurationsdatei](/misc/cfg-cal3d/)

## Verweise
* [MAME](https://en.wikipedia.org/wiki/MAME)

