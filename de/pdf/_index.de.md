{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "Grundlagen" ],
  "description":"Portable Document Format (PDF) ist eine Standarddarstellung von Dokumenten unabhängig von Software, Hardware und Betriebssystem. Zu den PDF-Standards gehören PDF/A, PDF/E, PDF/UA, PDF/VT und PDF/X.",
  "title" :"PDF-Dateiformat - Was ist eine PDF-Datei?",
  "linktitle" :"PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) ist ein Dokumenttyp, der von Adobe in den 1990er Jahren erstellt wurde. Der Zweck dieses Dateiformats bestand darin, einen Standard für die Darstellung von Dokumenten und anderem Referenzmaterial in einem Format einzuführen, das unabhängig von Anwendungssoftware, Hardware und Betriebssystem ist. Das PDF-Dateiformat kann Informationen wie Text, Bilder, Hyperlinks, Formularfelder, Rich Media, digitale Signaturen, Anhänge, Metadaten, Geodaten und 3D-Objekte enthalten, die Teil des Quelldokuments werden können.

In den meisten Fällen werden vorhandene Dokumente in PDF konvertiert, anstatt ein neues PDF von Grund auf neu zu erstellen. Aber das bedeutet nicht, dass es keine Software zum Erstellen oder Bearbeiten von PDF-Dateien gibt.

**(Möchten Sie etwas über das PDF-Dateiformat mitteilen? Sie können Ihre Ergebnisse im Abschnitt [Neuigkeiten zum PDF-Dateiformat](https://news.fileformat.com/t/PDF) posten.)**

## PDF-Dateiformat - Kurze Geschichte

Ein kurzer Überblick über die Zeitleiste über die Erstellung der PDF-Datei in Bezug auf die Zeitleiste ist wie folgt:

**1993** - Adobe Systems stellte die PDF-Spezifikationen kostenlos zur Verfügung

**2008** - PDF wurde am 1. Juli 2008 als offener Standard veröffentlicht und von der International Organization for Standardization als **ISO 32000-1:2008** veröffentlicht.

**2008** – Adobe veröffentlichte eine öffentliche Patentlizenz für gebührenfreie Rechte im ISO 32000-1-Format für alle Patente im Besitz von Adobe, die erforderlich sind, um PDF-konforme Implementierungen zu erstellen, zu verwenden, zu verkaufen und zu verteilen.

Die erste Version von PDF, die als PDF 1.0 bezeichnet wurde und später bis zu PDF 1.7 überarbeitet wurde. PDF 1.7, das zu ISO 32000-1 wurde, enthält einige nicht standardisierte proprietäre Technologien sowie Adobe XML Forms Architecture (XFA) und die JavaScript-Erweiterung für Acrobat. Am 28. Juli 2017 wurde PDF 2.0, bekannt als ISO 32000-2:2017, veröffentlicht, das keine nicht standardisierten Technologien enthält.

## Spezifikationen für das PDF-Dateiformat

Eine PDF-Datei ist ein Satz von Bytes, die gemäß den in den PDF-Spezifikationen definierten Syntaxregeln zu Token gruppiert werden können. Ein oder mehrere Token werden kombiniert, um syntaktische Einheiten höherer Ebene zu bilden, hauptsächlich Objekte, die die grundlegenden Datenwerte sind, aus denen ein PDF-Dokument aufgebaut ist.

### Dateistruktur von PDF-Dateien

Der Inhalt der PDF-Datei ist in der folgenden Reihenfolge innerhalb der Datei angeordnet.

|Kopfzeile
|Körper
|Querverweistabelle
|Anhänger

#### Kopfzeile der PDF-Datei ####

Unabhängig von der PDF-Version beginnt eine PDF-Datei mit einem Header, der eine eindeutige Kennung für PDF und die Version des Formats enthält, z. B. %PDF-1.x, wobei x von 1 bis 7 reicht.

#### Dateikörper ####

Der Hauptteil einer PDF-Datei besteht aus einer Folge von indirekten Objekten, die den Inhalt eines Dokuments darstellen. Die Objekte stellen, wie oben beschrieben, Komponenten des Dokuments dar, wie Schriftarten, Seiten und abgetastete Bilder. Ab PDF 1.5 kann der Hauptteil auch Objektströme enthalten, von denen jeder eine Folge von indirekten Objekten enthält.

#### Querverweistabelle ####

Die Querverweistabelle enthält Informationen, die einen wahlfreien Zugriff auf indirekte Objekte innerhalb der Datei ermöglichen, so dass nicht die gesamte Datei gelesen werden muss, um ein bestimmtes Objekt zu lokalisieren. Die Tabelle muss einen einzeiligen Eintrag für jedes indirekte Objekt enthalten, der den Byte-Offset dieses Objekts innerhalb des Hauptteils der Datei angibt. (Ab PDF 1.5 können einige oder alle Querverweisinformationen alternativ in Querverweis-Streams enthalten sein.

#### Dateitrailer ####

Der Trailer einer PDF-Datei ermöglicht es einem konformen Leser, die Querverweistabelle und bestimmte spezielle Objekte schnell zu finden. Konforme Leser sollten eine PDF-Datei von ihrem Ende lesen. Die letzte Zeile der Datei darf nur die Dateiende-Markierung %%EOF enthalten. Die zwei vorangehenden Zeilen müssen, eine pro Zeile und der Reihe nach, das Schlüsselwort startxref und den Byte-Offset im dekodierten Stream vom Anfang der Datei bis zum Anfang des xref-Schlüsselworts im letzten Querverweisabschnitt enthalten.

### PDF-Objekte ###

Eine PDF-Datei enthält mehrere unterschiedliche Arten von Objekten, die den folgenden Typen angehören

* Boolesche Werte - repräsentieren bedingt wahr oder falsch
* Zahlen - Integer- und Real-Werte
* Zeichenfolgen - enthält Zeichen in Klammern
* Namen - beginnen mit einem Vorwärtszeichen / zB /ASomewhatLongerName ergibt ASomewhatLongerName
* Arrays - PDF unterstützt eindimensionale Arrays. Arrays mit höheren Dimensionen können konstruiert werden, indem Arrays als verschachtelte Elemente verwendet werden
* Wörterbücher - Sammlung von Objekten als Schlüssel-Wert-Paare. Es kann null Einträge haben.
* Streams - stellt eine Folge von Bytes dar, die auch eine unbegrenzte Länge haben kann
* Null-Objekt – stellt einen Nullwert dar

Es kann andere Objekte wie Kommentare geben, die mit dem %-Zeichen eingeleitet werden und 8-Bit-Zeichen enthalten können.

### Indirekte Objekte ###

Jedes Objekt in einer PDF-Datei kann als indirektes Objekt bezeichnet werden. Indirekte Objekte erhalten eine eindeutige Objektkennung, mit der andere Objekte darauf verweisen können. Querverweise zu diesen werden in einer Indextabelle geführt und mit dem Schlüsselwort xref gekennzeichnet, das dem Hauptteil folgt und den Byte-Offset jedes indirekten Objekts vom Anfang der Datei angibt.

### Lineare und nichtlineare PDF-Layouts ###

PDF-Layouts werden in Abhängigkeit von den Zielanwendungen und anderen Faktoren als Llnear und Non-Linear kategorisiert.

Nichtlinear – Nichtlineare PDF-Dateien benötigen im Vergleich zu linearen PDF-Dateien weniger Speicherplatz. PDF-Seiten des Dokuments befinden sich in verstreuter Form über die PDF-Datei, weshalb nichtlineare Dateien im Vergleich zu linearen Dateien langsamer sind.

Lineares PDF – Lineare PDF-Dateien, die auf Online-PDF-Viewer abzielen, sind so aufgebaut, dass sie linear auf die Festplatte geschrieben werden. Dies erfordert keine Browser-Plugins, damit das gesamte Dokument zuerst geladen wird, bevor es angezeigt wird.

### Objektübersicht ###

Wie bereits erwähnt, ist der PDF-Körper eine Sammlung der oben erwähnten Objekte. PDF basiert weitgehend auf PostScript ohne die Steuerfunktionen von Programmiersprachen wie if- und loop-Befehlen. Vom Postscript-Code ausgegebene Befehle zum Generieren von grafischen Inhalten werden gesammelt und zusätzlich zu allen Dateien, Grafiken oder Schriftarten, auf die das Dokument verweist, in Tokens zerlegt. Alle diese Inhalte werden in einer einzigen Datei gesammelt, was zu einer zusammengesetzten PostScript-Ausgabe führt.

#### Text ####

Text in PDF wird durch Textelemente dargestellt, die tatsächlich mit Glyphen aus Schriftarten angezeigt werden. Eine Glyphe ist eine grafische Form und unterliegt allen grafischen Manipulationen, wie z. B. einer Koordinatentransformation. Aufgrund der Bedeutung von Text in den meisten Seitenbeschreibungen bietet PDF höherwertige Einrichtungen zum bequemen und effizienten Beschreiben, Auswählen und Rendern von Glyphen.

#### Grafiken ####

Die in PDF-Inhaltsströmen verwendeten Grafikoperatoren beschreiben das Erscheinungsbild von Seiten, die auf einem Rasterausgabegerät wiedergegeben werden sollen. Die Einrichtungen sind sowohl für Drucker- als auch Anzeigeanwendungen vorgesehen. Die Grafikoperatoren bilden sechs Hauptgruppen:

* Grafikzustandsoperatoren manipulieren die als Grafikzustand bezeichnete Datenstruktur, den globalen Rahmen, innerhalb dessen die anderen Grafikoperatoren ausgeführt werden. Der Grafikzustand umfasst die Stromtransformationsmatrix (CTM), die Benutzerraumkoordinaten, die in einem PDF-Inhaltsstrom verwendet werden, in Ausgabegerätekoordinaten abbildet. Es enthält auch die aktuelle Farbe, den aktuellen Beschneidungspfad und viele andere Parameter, die implizite Operanden der Maloperatoren sind.
* Pfadkonstruktionsoperatoren spezifizieren Pfade, die Formen, Linientrajektorien und Bereiche verschiedener Art definieren. Sie enthalten Operatoren zum Beginnen eines neuen Pfads, zum Hinzufügen von Liniensegmenten und Kurven und zum Schließen.
* Operatoren zum Malen von Pfaden füllen einen Pfad mit einer Farbe, malen einen Strich darauf oder verwenden ihn als Schnittgrenze.
* Andere Maloperatoren malen bestimmte selbstbeschreibende Grafikobjekte. Dazu gehören abgetastete Bilder, geometrisch definierte Schattierungen und ganze Inhaltsströme, die wiederum Sequenzen von Grafikoperatoren enthalten.
* Textoperatoren wählen und zeigen Zeichenglyphen aus Schriftarten (Beschreibungen von Schriftarten zur Darstellung von Textzeichen). Da PDF Glyphen als allgemeine grafische Formen behandelt, könnten viele der Textoperatoren mit den Grafikzustands- oder Zeichenoperatoren gruppiert werden. Die Datenstrukturen und Mechanismen zum Umgang mit Glyphen- und Zeichensatzbeschreibungen sind jedoch ausreichend spezialisiert.
* Operatoren für markierte Inhalte verknüpfen logische Informationen höherer Ebene mit Objekten im Inhaltsstrom. Diese Informationen wirken sich nicht auf die gerenderte Darstellung des Inhalts aus; Es ist nützlich für Anwendungen, die PDF für den Dokumentenaustausch verwenden.

## Verweise ##

* [PDF-Dateiformat: Grundstruktur](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [PDF-Referenz – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

