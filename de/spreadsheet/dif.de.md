{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "Datei", "Erweiterung", "Dateiformat", "Data Interchange File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ihr Dateiformatleitfaden, um zu wissen, was eine DIF-Dateierweiterung und APIs sind, die DIF-Dateien erstellen und öffnen können.",
  "title" :"DIF - Datenaustauschdateiformat",
  "linktitle" :"DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Was ist eine DIF-Datei?

DIF steht für Data Interchange Format, das zum Importieren/Exportieren von Tabellenkalkulationsdaten zwischen verschiedenen Anwendungen verwendet wird. Dazu gehören Microsoft Excel, OpenOffice Calc, StarCalc und viele andere. Es speichert Daten, die in einer einzigen Tabelle enthalten sind, was die einzige Einschränkung dieses Dateiformats darstellt.

## Kurze Geschichte des DIF-Dateiformats ##

Das DIF-Dateiformat wurde Anfang der 1980er Jahre von Software Arts, Inc. entwickelt. Die Dateiformatspezifikationen für DIF wurden in VisiCalc aufgenommen, dem ersten Tabellenkalkulationsprogramm für PCs. Diese Spezifikationen wurden 1981 urheberrechtlich geschützt und waren ein eingetragenes Warenzeichen der Software Arts Products Corp.

## DIF-Dateiformat ##

DIF speichert Tabelleninhalte in einer ASCII-Textdatei, die es ermöglicht, sie mit einem Texteditor anzuzeigen und zu bearbeiten. Das Format nimmt aufgrund seiner Eigenschaften des Datenaustauschs seinen Platz in der Liste der Datenserialisierungsformate ein. Eine DIF-Datei besteht aus 2 Abschnitten; ein Header und Daten.

Alles in DIF wird durch einen 2- oder 3-zeiligen Block dargestellt. Header erhalten einen 3-Zeilen-Chunk; Daten, 2.

* Header-Chunks beginnen mit einer Textkennung, die nur aus Großbuchstaben, nur alphabetischen Zeichen und weniger als 32 Buchstaben besteht. Die folgende Zeile muss ein Zahlenpaar sein, und die dritte Zeile muss eine Zeichenfolge in Anführungszeichen sein.
* Datenblöcke beginnen mit einem Zahlenpaar und die nächste Zeile ist eine Zeichenfolge in Anführungszeichen oder ein Schlüsselwort.

### Werte ###

Ein Wert belegt zwei Zeilen, die erste ein Zahlenpaar und die zweite entweder eine Zeichenkette oder ein Schlüsselwort. Die erste Zahl des Paares gibt den Typ an:

* −1 – Direktiventyp, die zweite Zahl wird ignoriert, die folgende Zeile ist eines dieser Schlüsselwörter:
** BOT – Beginn des Tupels (Start of Row)
** EOD – Ende der Daten
* 0 – numerischer Typ, Wert ist die zweite Zahl, die folgende Zeile ist eines dieser Schlüsselwörter:
** V – gültig
** NA – nicht verfügbar
** FEHLER – Fehler
** TRUE – wahrer boolescher Wert
** FALSCH – falscher boolescher Wert
* 1 – Zeichenfolgentyp, die zweite Zahl wird ignoriert, die folgende Zeile ist die Zeichenfolge in doppelten Anführungszeichen

### DIF-Header-Chunk ###

Der Header-Chunk einer DIF-Datei besteht aus einer Kennungszeile, gefolgt von zwei Zeilen mit einem Wert. Die numerischen Werte in Header-Chunks verwenden anstelle der Gültigkeitsschlüsselwörter nur eine leere Zeichenfolge. Die Details dieser Header-Chunks sind wie folgt.

* TABLE - es folgt ein numerischer Wert der Version, die unbenutzte zweite Zeile des Wertes enthält einen Generatorkommentar
* VEKTOREN - die Anzahl der Spalten folgt als Zahlenwert
* TUPLES - die Anzahl der Zeilen folgt als numerischer Wert
* DATA - nach einem numerischen Dummy-Wert von 0 folgen die Daten für die Tabelle, wobei jeder Zeile ein BOT-Wert vorangeht, die gesamte Tabelle durch einen EOD-Wert abgeschlossen wird

### DIF-Beispiel ###

Das folgende Beispiel zeigt den Inhalt eines einfachen Arbeitsblatts und seine äquivalente DIF-Darstellung.


|Name|Alter
---|---|
|Bob|34
|Blatt|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Verweise ##

* [DIF – von Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

