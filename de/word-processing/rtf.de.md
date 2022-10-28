{
  "date" : "2019-10-11",
  "keywords" :[ "rtf-Datei", "rtf-Dateiformat", "was ist eine rtf-Datei", "Datei", "rtf-Beispiel", "rtf-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Rich-Text-Format",
  "description":"Erfahren Sie mehr über das RTF-Dateiformat und APIs, die RTF-Dateien erstellen und öffnen können.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine RTF-Datei?

Das von Microsoft eingeführte und dokumentierte Rich Text Format (**RTF**) stellt eine Methode zum Codieren von formatiertem Text und Grafiken für die Verwendung in Anwendungen dar. Das Format erleichtert den plattformübergreifenden Austausch von Dokumenten mit anderen Microsoft-Produkten und dient somit dem Zweck der Interoperabilität. Diese Fähigkeit macht es zu einem Standard für die Datenübertragung zwischen Textverarbeitungssoftware und daher können Inhalte von einem Betriebssystem auf ein anderes übertragen werden, ohne dass die Dokumentformatierung verloren geht. Die Dateiformatspezifikationen sind von Microsoft zum öffentlichen [Download] verfügbar (https://www.microsoft.com/en-us/download/details.aspx?id#10725) und können aus Entwicklersicht herangezogen werden.

## Kurze Geschichte des RTF-Dateiformats ##

Das RTF-Dateiformat wurde seit seiner Veröffentlichung mehrfach überarbeitet. Die offizielle Version zum Lesen/Schreiben wurde als Teil von Microsoft Word 3.0 für Macintosh mit den Spezifikationen der Version 1.0 veröffentlicht. Die endgültige Version der Spezifikationen, 1.9.1, wurde von Microsoft im März 2008 veröffentlicht. Danach werden keine weiteren Verbesserungen an den Spezifikationen vorgenommen. Derzeit verfügen fast alle Betriebssysteme über funktionsreichere Anwendungen, die die Verwendung des RTF-Dateiformats minimiert/beseitigt haben.

## RTF-Dateiformatspezifikationen ##

RTF dient als Standard für die Datenübertragung zwischen Textverarbeitungsprogrammen und die Übertragung von Inhalten von einem Betriebssystem auf ein anderes. Dies wird mithilfe von Steuerwörtern erreicht, die von Microsoft Office Word bis 2007 eingeführt wurden. Eine Standard-RTF-Datei besteht aus ASCII zur Darstellung von Rich-Text und Nicht-ASCII-Zeichen, die in entsprechende Codewerte konvertiert werden. Neuere Versionen von Word können RTF-Dateien lesen, die mit früheren Versionen erstellt wurden, während die älteren Versionen Steuerwörter und Gruppen ignorieren, die sie nicht verstehen.

### Die Grundlagen von RTF verstehen ###

RTF-Dateien verwenden 7-Bit-ASCII-Klartext, bestehend aus:

* Kontrollwörter
* Steuersymbole und
* Gruppen.

Diese fungieren als Bausteine für die Darstellung von RTF-Daten als verständlicher Text und Zeichenkodierung.

#### Steuerwort ####

Diese stellen speziell formatierte Befehle dar, die zum Markieren von Zeichen für die Anzeige verwendet werden, und dürfen nicht länger als 32 Buchstaben sein. Ein Steuerwort wird definiert durch:

\<ASCII Letter Sequence> //<//Delimiter//> //

Jedes Steuerwort unterscheidet zwischen Groß- und Kleinschreibung und beginnt mit einem umgekehrten Schrägstrich. Die ASCII-Buchstabenfolge kann ASCII-Alphabete (a bis z und A bis Z) enthalten. Das<Delimite> markiert das Ende des Namens des Steuerworts und kann einer der folgenden sein:

* Ein Leerzeichen. Dies dient nur zur Begrenzung eines Steuerwortes und wird bei der weiteren Verarbeitung ignoriert.
* Eine numerische Ziffer oder ein ASCII-Minuszeichen, das angibt, dass dem Steuerwort ein numerischer Parameter zugeordnet ist. Die nachfolgende digitale Folge wird dann durch ein beliebiges anderes Zeichen als eine ASCII-Ziffer (üblicherweise ein anderes Steuerwort, das mit einem umgekehrten Schrägstrich beginnt) begrenzt. Der Parameter kann eine positive oder negative Dezimalzahl sein. Der Wertebereich für die Zahl ist nominell –32768 bis 32767, dh eine vorzeichenbehaftete 16-Bit-Ganzzahl. Eine kleine Anzahl von Steuerwörtern nimmt Werte im Bereich –2.147.483.648 bis 2.147.483.647 (32-Bit-Ganzzahl mit Vorzeichen) an. Diese Steuerwörter beinhalten **\binN**, **\revdttmN//**, **\rsidN** verwandte Steuerwörter und einige Bildeigenschaften wie **\bliptagN**. Dabei steht **N** für den numerischen Parameter. Ein RTF-Parser muss bis zu 10 Ziffern zulassen, denen optional ein Minuszeichen vorangestellt ist. Wenn das Trennzeichen ein Leerzeichen ist, wird es verworfen, d. h. es wird nicht in die nachfolgende Verarbeitung einbezogen.
* Jedes andere Zeichen als ein Buchstabe oder eine Ziffer. In diesem Fall schließt das Begrenzungszeichen das Steuerwort ab und ist nicht Teil des Steuerworts. Beispielsweise folgt ein Backslash „\“, was bedeutet, dass ein neues Steuerwort oder ein Steuersymbol folgt.

#### Steuersymbol ####

Ein Steuersymbol stellt ein besonderes Ereignis dar, das abhängig von seinem Inhalt eine bestimmte Bedeutung hat. Es besteht aus einem Backslash gefolgt von einem Sonderzeichen (nicht alphabetisches Zeichen) und hat keine Trennzeichen.

#### Gruppe ####

Eine Gruppe kann aus Text, Steuerwörtern oder Steuersymbolen in geschweiften Klammern (**{ }**) bestehen. Die öffnende geschweifte Klammer (**{** ) gibt den Beginn der Gruppe an und die schließende geschweifte Klammer ( **}**) zeigt das Ende der Gruppe an. Jede Gruppe spezifiziert den von der Gruppe betroffenen Text und die verschiedenen Attribute dieses Textes.

### RTF-Dateistruktur ###

Eine RTF-Datei hat die folgende Standard-Syntax:

Das von Microsoft eingeführte und dokumentierte Rich Text Format (**RTF**) stellt eine Methode zum Codieren von formatiertem Text und Grafiken für die Verwendung in Anwendungen dar. Das Format erleichtert den plattformübergreifenden Austausch von Dokumenten mit anderen Microsoft-Produkten und dient somit dem Zweck der Interoperabilität. Diese Fähigkeit macht es zu einem Standard für die Datenübertragung zwischen Textverarbeitungssoftware und daher können Inhalte von einem Betriebssystem auf ein anderes übertragen werden, ohne dass die Dokumentformatierung verloren geht. Die Dateiformatspezifikationen sind von Microsoft zum öffentlichen [Download] verfügbar (https://www.microsoft.com/en-us/download/details.aspx?id#10725) und können aus Entwicklersicht herangezogen werden.

#### RTF-Header ####

Ein RTF-Header hat die folgende Darstellung.

|Feld|Beschreibung
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Header-Tabellen müssen in dieser Reihenfolge erscheinen, falls sie vorhanden sind. Die RTF-Datei kann Gruppen für Schriftarten, Stile, Bildschirmfarbe, Bilder, Fußnoten, Kommentare (Anmerkungen), Kopf- und Fußzeilen, zusammenfassende Informationen, Felder, Lesezeichen, Dokument-, Abschnitts-, Absatz- und Zeichenformatierungseigenschaften, Mathematik, Bilder und Objekte. Wenn Schriftart, Datei, Stil, Farbe, Überarbeitungsmarkierung und zusammenfassende Informationsgruppen sowie Dokumentformatierungseigenschaften in der Datei enthalten sind, müssen sie im RTF-Header erscheinen, der dem RTF-Hauptteil vorangeht. Wenn der Inhalt einer Gruppe nicht verwendet wird, kann die Gruppe weggelassen werden. Jede Gruppe, die die in einer anderen Gruppe definierten Eigenschaften verwendet, muss nach der Gruppe erscheinen, die diese Eigenschaften definiert. Farb- und Schrifteigenschaften müssen beispielsweise der Stilgruppe vorangestellt werden.

#### RTF-Version ####

Ein RTF-Dokument muss mit diesen sechs Zeichen beginnen:

```
{\rtf1
```
wobei die 1 die RTF-Versionsnummer anzeigt.

#### Zeichensatz ####

Nach dem {\rtf1 sollte das Dokument angeben, welchen Zeichensatz es verwendet. Der Weg, einen Zeichensatz zu deklarieren, ist mit einem dieser Befehle:

`\ansi` - Das Dokument ist im ANSI-Zeichensatz, auch bekannt als Codepage 1252, dem üblichen MSWindows-Zeichensatz.

`\mac` - Das Dokument ist im MacAscii-Zeichensatz, dem üblichen Zeichensatz unter alten (vor 10) Versionen von Mac OS.

`\pc` - Das Dokument befindet sich in DOS Code Page 437, dem Standardzeichensatz für MS-DOS. Schreibkräfte mit gutem Muskelgedächtnis werden feststellen, dass dies der Zeichensatz ist, der immer noch zum Interpretieren von „Alt-Numerik“-Codes verwendet wird – dh wenn Sie die Alt-Taste gedrückt halten und „130“ auf dem Ziffernblock eingeben, wird ein é erzeugt, weil Zeichen 130 in CP437 ist ein é. Das ist ungefähr die einzige Verwendung, die CP437 heutzutage sieht.

`\pca` - Das Dokument befindet sich in der DOS-Codepage 850, auch bekannt als MS-DOS Multilingual Codepage.

#### Schriftartbefehl ####

Nach der Zeichensatzdefinition folgt der Befehl `\deffN`. Dadurch wird festgelegt, dass die Schriftartnummer N die Standardschriftart für dieses Dokument ist. Die Schriftartnummer N wird aus der Schriftarttabelle bezogen. Der Befehl `\deffN` ist technisch optional, sollte aber sicherheitshalber da sein, da ein gängiger Prolog wie folgt den Font 0 als Standardfont auswählt.

`{\rtf1\ansi\deff0`

#### Schriftartentabelle ####

Alle Schriften, die in einem Dokument verwendet werden können, sind in einer Schrifttabelle aufgeführt, in der jede Schrift durch eine Schriftnummer dargestellt wird. Das Dokument muss eine Schrifttabelle haben, obwohl einige Programme auch ohne diese funktionieren.

Die Syntax für eine Schriftarttabelle ist {\fonttbl //...declarations//...}, wobei jede Deklaration diese grundlegende Syntax hat:

`{\fnumber\familycommand Fontname;}`

Eine Fonttabelle mit vier Deklarationen sieht wie folgt aus:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

In einem Dokument mit dieser Schriftartentabelle würde `{\f2 stuff}` „Zeug“ in Courier New ausgeben. Eine Schriftart kann in einem Dokument erst verwendet werden, wenn sie in der Schriftartentabelle aufgeführt ist.

### Ende des Dokuments ###

Jedes RTF-Dokument muss mit einem } enden, um die Gruppe zu schließen, die durch das {, das das erste Zeichen im Dokument ist, geöffnet wurde. Auf das abschließende } darf nichts folgen, außer möglicherweise ein Zeilenumbruch.

## Verweise ##

* [RTF 1.9.1-Spezifikationen](https://www.microsoft.com/en-us/download/details.aspx?id#10725)
* [Rich-Text-Format](https://en.wikipedia.org/wiki/Rich_Text_Format)

