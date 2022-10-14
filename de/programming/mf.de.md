{
  "date" : "2019-10-11",
"Schlüsselwörter": [ "mf-Datei", "mf", "Erweiterung", "Format", "mf-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Java-Manifest-Dateiformat",
  "description":"Erfahren Sie mehr über das MF-Dateiformat und APIs, die MF-Dateien erstellen und öffnen können.",
  "linktitle" :"MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine MF-Datei?

Eine Datei mit der Erweiterung .mf ist eine Java-Manifestdatei, die Informationen zu den einzelnen [JAR](/de/programming/jar/)-Dateieinträgen enthält. Die MF-Datei selbst ist in der JAR-Datei enthalten und enthält alle Erweiterungs- und paketbezogenen Definitionen. JAR-Dateien können zur Verwendung als ausführbare Datei erstellt werden. In diesem Fall gibt die mainfest-Datei die Hauptklasse der Anwendung an, die die Anweisung **`public static void main`** enthält. Manifestdateien heißen MANIFEST.MF und können mit jedem Texteditor auf Windows-, MacOS- und Linux-Betriebssystemen geöffnet werden.

## Manifest-Dateiformatspezifikationen

[Spezifikationen des Manifest-Dateiformats] (https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) sind von Oracle in ihrem Leitfaden für das JAR-Dateiformat verfügbar. Eine Manifestdatei besteht aus Hauptabschnitten, denen eine Liste von Abschnitten für einzelne JAR-Dateieinträge folgt. Jeder Abschnitt folgt einigen Regeln und Einschränkungen.

### Hauptabschnitte

Ein Hauptteil:

* enthält Informationen zur Sicherheit und Konfiguration der JAR-Datei
* enthält Informationen über die Anwendung oder Erweiterung, zu der die JAR-Datei gehört
* definiert die Hauptattribute für jedes einzelne Manifestelement

**Hinweis**: Kein Attribut in diesem Abschnitt darf "Name" heißen.

### Einzelne Abschnitte

Ein eigener Abschnitt definiert verschiedene Attribute für Pakete oder Dateien einer JAR-Datei. Jeder Abschnitt muss mit einem Attribut namens „Name“ beginnen, dessen Wert ein relativer Pfad zur Datei oder eine absolute URL sein muss, die auf Daten außerhalb des Archivs verweist.

### Manifestspezifikationen

|Attribute|Beschreibung|
---|---|
|manifest-file|hauptabschnitt newline *individual-section|
|Hauptabschnitt|Versionsinfo Zeilenumbruch *Hauptattribut|
|Versionsinfo|Manifest-Version : Versionsnummer|
|Versionsnummer|Ziffer+{.Ziffer+}*|
|Hauptattribut|(jedes legitime Hauptattribut) Zeilenumbruch|
|einzelner-abschnitt|Name : wert newline *perentry-attribute|
|perentry-attribute|(beliebiges legitimes perentry-attribut) newline|
|newline|CR LF | LF | CR (nicht gefolgt von LF)|
|Ziffer|{0-9}|

## Verweise

* [Oracle – JAR-Dateiformat] (https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [JAR-Dateiformat](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,in%20one%20file%20for% 20distribution.&text=Sie%20sind%20auf%20der,jar%20Datei-%20Erweiterung aufgebaut%20.)

