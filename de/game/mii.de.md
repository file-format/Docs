{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das MGX-Dateiformat von Age of Empires 2 Expansion Replay und APIs, die MGX-Dateien erstellen und öffnen können.",
  "title" :"MII-Datei - Virtuelles Wii-Avatar-Dateiformat",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Was ist eine MII-Datei?

Eine MII-Datei ist ein virtuelles Avatar-Dateiformat, das zum Speichern virtueller Avatare auf der Nintendo Wii-Spielekonsole verwendet wird. Diese Dateien enthalten Informationen wie das Aussehen, Bewegungen und Animationen des Avatars. Sie können in Spielen, Social-Networking-Anwendungen und anderer Software auf der Wii verwendet werden. Eine MII-Datei enthält auch andere Merkmale des Avatars wie Geschlecht, Haarfarbe, Hautfarbe, Gesichtszüge und Augentyp.

Sie können eine MII-Datei mit dem [My Avatar Editor](https://rc24.xyz/goodies/mii/) öffnen.

## MII-Dateiformat

Das MII-Dateiformat ist detailliert auf [Wii Brew] (https://wiibrew.org/wiki/Mii_data) definiert. Zeichenfolgen in einer MII-Datei werden im Unicode-Format (UTF-16), Big-Endian, gespeichert.

### MI-Block

MII-Dateidaten werden auf der Wiimote in zwei Blöcken gespeichert. Jeder Block ist 750 Byte lang, mit 2 Byte CRC, was eine Gesamtlänge von 752 Byte ergibt. Jeder Block beginnt mit einem 4-Byte-Wert ('RNCD'), der die magische Zahl für das MII-Dateiformat zu sein scheint.

## Wie erstelle ich MII-Dateien?

Es gibt verschiedene Möglichkeiten, Avatare für die Nintendo Wii zu erstellen:

1. `Verwenden des integrierten Mii-Kanals auf der Wii:` Dieser Kanal ermöglicht es Ihnen, benutzerdefinierte Avatare mit einer Vielzahl von Werkzeugen zu erstellen, darunter Gesichtszüge, Körperform und Kleidung. Sobald Sie Ihren Avatar erstellt haben, können Sie ihn als Mii-Datei speichern und in Spielen und anderer Software auf der Wii verwenden.

1. „Verwendung der Mii-Maker-App auf dem Nintendo 3DS:“ Mit der Mii-Maker-App können Sie mithilfe des Touchscreens und der Kamera Ihres Nintendo 3DS benutzerdefinierte Avatare erstellen. Sobald Sie Ihren Avatar erstellt haben, können Sie ihn als Mii-Datei speichern und über eine drahtlose Verbindung auf Ihre Wii übertragen.

1. „Verwenden von Software von Drittanbietern:“ Einige Entwickler haben Software erstellt, mit der Sie benutzerdefinierte Avatare für die Wii erstellen können. Diese Software ist normalerweise für die Verwendung auf einem Computer konzipiert und erfordert möglicherweise zusätzliche Schritte, um den Avatar auf Ihre Wii zu übertragen.

1. `Vorgefertigte Avatare verwenden:` Einige Spiele und andere Software auf der Wii enthalten möglicherweise vorgefertigte Avatare, die Sie verwenden können.

In jedem Fall benötigen Sie ein Nintendo-Konto, um Ihren Avatar auf der Wii zu erstellen und zu speichern.

## Verweise

* [Mein Avatar-Editor](https://rc24.xyz/goodies/mii/)
* [Wii Brew] (https://wiibrew.org/wiki/Mii_data)

