{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das ACCDB-Dateiformat und APIs, die ACCDB-Dateien erstellen und öffnen können.",
  "title" :"ACCDB-Dateiformat - Microsoft Access 2007-Datenbankdatei",
  "linktitle" :"ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Was ist eine ACCDB-Datei?

Eine Datei mit der Erweiterung .accdb ist eine Microsoft Access 2007-Datenbankdatei, die Benutzerdaten in Tabellen speichert. Es unterstützt das Speichern
benutzerdefinierte Formulare, SQL-Abfragen und andere Daten. ACCDB-Dateien ersetzten [MDB](/de/database/mdb/)-Dateien, nachdem Microsoft auf eine XML-basierte Dateistruktur umgestellt hatte. ACCDB-Dateien können weiterhin mit alter Kompatibilität in MDB konvertiert werden. ACCDB ist jedoch das inzwischen weit verbreitete Dateiformat für Access-Datenbanken. Microsoft unterstützte auch zusätzliche Funktionen im ACCDB-Format, wie z. B. die Möglichkeit, Dateianhänge, Binärdaten und mehrwertige Felder zu speichern.

## ACCDB-Dateiformat

Wie bei MDB gibt es keine öffentlichen Spezifikationen für das ACCDB-Dateiformat. Microsoft unterstützt den programmgesteuerten Zugriff auf diese Dateien über den Standard Open Database Connectivity (ODBC) und Visual Basic for Applications (VBA).

### Ein Einblick

Ein Hex-Dump einer einfachen ACCDB-Datei legt nahe, dass es allgemeine Ähnlichkeiten in der Struktur zu den neuesten Versionen der Vorgänger-MDB-Formatfamilie gibt. Beide Dateiformate verwenden feste Seitengrößen von 4096 Byte. Eine weitere Ähnlichkeit zwischen ACCDB und MDB ist die Form der magischen Zahl, die die Zeichenfolge „Standard ACE DB“ für ACCDB enthält. Ein Versions- oder Kompatibilitätscode befindet sich in beiden Formaten an derselben Stelle. Die mdbtools | In der HACKING-Datei heißt es: „Offset 0x14 enthält die Jet-Version dieser Datenbank“ und der inoffizielle MDB-Leitfaden stimmt zu. Die Informationen in diesen Quellen, kombiniert mit dem Wikipedia-Eintrag für [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), legen nahe, dass ein Wert von 0x02 ACE 12 (Access 2007) und 0x03 ACE anzeigt 14 (Zugang 2010). Eine in Access 2010 erstellte minimale Datenbank und eine ähnliche in Access 2016 erstellte Datenbank haben jedoch beide 0x02 an diesem Speicherort. Eine minimale Datenbank, die in Access 2016 erstellt wurde, aber eine Spalte mit dem neu eingeführten Datentyp „Large Integer“ definierte, hatte einen Wert von 0x05. In ACCDB-Dateien scheint dieser Indikator die Kompatibilität der Datei widerzuspiegeln und nicht die Version der ACE-Engine, die zu ihrer Erstellung verwendet wurde.

## Verweise

* [Access-Dateiformat](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Access 2016-Spezifikationen] (https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet-Datenbankmodul](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Welches Access-Dateiformat sollte ich verwenden?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=en-us&rs=en-us&ad=us)

