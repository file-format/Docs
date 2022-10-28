{
  "date" : "2019-10-11",
  "keywords" :[ "aba-Datei", "aba-Dateiformat", "was ist eine aba-Datei", "Datei", "aba-Beispiel", "aba-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - CemText-Dateiformat",
  "description":"Erfahren Sie mehr über das ABA-Dateiformat und APIs, die ABA-Dateien erstellen und öffnen können.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
"identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Was ist eine ABA-Datei?

Eine Datei mit der Erweiterung .aba ist ein Dateiformat der Australian Bankers Association (ABA) oder des [Cemtext](https://www.cemtexaba.com/)-Dateiformats, das von Banken für Batch-Transaktionen verwendet wird. Es wird von den meisten Banken für die Führung von Finanzunterlagen verwendet. Das ABA-Dateiformat, das auch als Direkteingabedatei bekannt ist, wurde von den meisten australischen Banken als Standardformat für Stapeltransaktionen übernommen. Es wurde immer noch nicht als Standardformat anerkannt, obwohl es von der Bank of Queensland, NAB und Westpac verwendet wurde. ABA-Dateien können mit jedem Texteditor wie Notepad++ geöffnet werden.


## ABA-Dateiformat

Eine ABA-Datei verwendet das ASCII-Format, um Daten zum Weiterleiten oder Laden in Banksysteme zu speichern. Das Format wurde einfach gehalten, um die Integration in das unternehmenseigene Finanzsystem zur Verarbeitung von Transaktionsstapeln zu erleichtern. Beispielsweise kann in einem Gehaltsabrechnungssystem eine Reihe von Transaktionen hochgeladen werden, um sie auf einmal zu verarbeiten. Die Spezifikationen des ABA-Dateiformats sind als vollständige Abschrift auf der Website [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) verfügbar und können als Referenz für Entwickler herangezogen werden .

Eine ABA-Datei besteht aus mehreren Zeilen, wobei jede Zeile als „Datensatz“ bezeichnet wird. Es gibt drei Hauptdatensätze in einer ABA-Datei:

* Beschreibender Datensatz
* Detailaufnahme
* Gesamtaufzeichnung der Datei

### Beschreibender Datensatz

Ein "beschreibender Datensatz" enthält Informationen wie beispielsweise die Rollenfolgenummer, den Namen des Finanzinstituts des Benutzers, den Namen der liefernden Datei des Benutzers und andere Informationen.

### Detaildatensatz

Der Typ „Detaildatensatz“ umfasst Informationen wie Bank-/Staats-/Zweigstellennummer, Kontonummer, die gutgeschrieben/belastet werden soll, Indikator, Transaktionscode, Betrag und andere Informationen.

### Datei-Gesamtdatensatz

Der "Datei-Gesamtdatensatz"-Typ umfasst Datensatztyp 7, BSB-Format-Füller, Datei (Benutzer)-Nettogesamtbetrag, Datei (Benutzer)-Guthaben-Gesamtbetrag, Datei (Benutzer)-Soll-Gesamtbetrag und andere Informationen.

### Transaktionscodes

Eine Liste gültiger Transaktionscodes ist wie folgt. Meistens wird in ABA-Dateien der Code "53 - Pay" verwendet. Diese Transaktionscodes umfassen Belastungen, Gutschriften und Quellensteuern.

|Code|Transaktionsbeschreibung|
---|---|
|13|Fremd veranlasste Belastungspositionen|
|50|Extern initiierte Gutschriften mit Ausnahme von Transaktionscodes|
|51|Sicherheitsinteresse der australischen Regierung|
|52|Familienbeihilfe|
|53|Bezahlen|
|54|Rente|
|55|Zuteilung|
|56|Dividende|
|57|Schuldverschreibungszinsen|

## Beispiel für eine ABA-Datei

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Verweise

* [Cemtext ABA](https://www.cemtexaba.com/)

