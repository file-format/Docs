{
  "date" : "2021-09-08",
  "keywords" :[ "rel-Datei", "rel-Dateiformat", "was ist eine rel-Datei", "Datei", "rel-Beispiel", "rel-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das REL-Dateiformat und APIs, die REL-Dateien erstellen und öffnen können.",
  "title" :"REL - Verschiebbare Moduldatei",
  "linktitle" :"REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Was ist eine REL-Datei?
Eine Datei mit der Erweiterung .rel kann für verschiedene Zwecke verwendet werden. Daher ist es in Bezug auf die Spielklassifizierung als verschiebbare Moduldatei bekannt, die von einigen Nintendo Wii-Spielen wie Brawl, Super Smash Bros und Mario Kart Wii verwendet wird. Es umfasst die Spieldaten, einschließlich Charaktermodelle und Stufen. REL-Dateien verhalten sich ähnlich wie die von Microsoft Windows verwendeten .DLL-Dateien.

## REL-Dateiformat
In einem REL-Dateiformat ist die Datei in mehrere Abschnitte unterteilt, die nach gleichem Zugriff gruppiert sind, z. B. schreibgeschützte Daten in einem Abschnitt, der gesamte ausführbare Code wird in einem anderen platziert usw. Die Datei beginnt mit einem Header-Abschnitt, gefolgt von:
- Tabelle mit Abschnittsinformationen.
- Die Abschnittsdaten.
- Umzugsinformationen.

### Dateikopf
Die Datei beginnt mit einem Header von bis zu 0x4C Bytes:
| Versatz | Größe | Feldname | Beschreibung |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | ID | Willkürliche Identifikationsnummer. Muss unter allen von einem Spiel verwendeten RELs eindeutig sein. Darf nicht 0 sein. |
| 0x04 | 4 | weiter | Zeiger auf nächstes Modul, gefüllt zur Laufzeit. |
| 0x08 | 4 | zurück | Zeiger auf vorheriges Modul, zur Laufzeit gefüllt. |
| 0x0c | 4 | numSections | Anzahl der Abschnitte in der Datei. |
| 0x10 | 4 | sectionInfoOffset | Offset zum Beginn der Abschnittstabelle. |
| 0x14 | 4 | NameOffset | Offset zur ASCII-Zeichenfolge, die den Namen des Moduls enthält. Kann NULL sein. Relativ zum Beginn der REL-Datei. |
| 0x18 | 4 | nameGröße | Größe des Modulnamens in Byte. |
| 0x1c | 4 | Fassung | Versionsnummer des REL-Dateiformats. |
| 0x20 | 4 | bssGröße | Größe des Abschnitts „.bss“. |
| 0x24 | 4 | relOffset | Offset zur Verschiebungstabelle. |
| 0x28 | 4 | impOffset | Versatz zur Imp-Tabelle. |
| 0x2c | 4 | impSize | Größe der Imp-Tabelle in Byte. |
| 0x30 | 1 | prologAbschnitt | Index in die Abschnittstabelle, zu der der Prolog relativ ist. Überspringen, wenn dieses Feld 0 ist. |
| 0x31 | 1 | epilogSection | Index in Abschnittstabelle, auf die sich der Epilog bezieht. Überspringen, wenn dieses Feld 0 ist. |
| 0x32 | 1 | ungelöster Abschnitt | Index in die Abschnittstabelle, auf die sich der ungelöste Wert bezieht. Überspringen, wenn dieses Feld 0 ist. |
| 0x33 | 1 | bssAbschnitt | Index in die Abschnittstabelle, zu der bs relativ ist. Zur Laufzeit gefüllt! |
| 0x34 | 4 | Prolog | Offset in den angegebenen Abschnitt der _prolog-Funktion. |
| 0x38 | 4 | Epilog | Offset in den angegebenen Abschnitt der _epilog-Funktion. |
| 0x3c | 4 | ungelöst | Offset in den angegebenen Abschnitt der _unresolved-Funktion. |
| 0x40 | 4 | ausrichten | Nur Version ≥ 2. Ausrichtungsbeschränkung für alle Abschnitte, ausgedrückt als Potenz von 2. |
| 0x44 | 4 | bssAusrichten | Nur Version ≥ 2. Ausrichtungseinschränkung für alle '.bss'-Abschnitte, ausgedrückt als Potenz von 2. |
| 0x48 | 4 | fixSize | Nur Version ≥ 3. Wenn REL mit OSLinkFixed (anstelle von OSLink) verknüpft ist, kann das Leerzeichen nach dieser Adresse für andere Zwecke (wie BSS) verwendet werden. |

### Abschnitt-Info-Tabelle
Die Abschnittsinfotabelle enthält **numSections**-Einträge mit jeweils 0x8 Bytes Länge:
| Versatz | Größe | Beschreibung |
-------|------------|-------------|
| 0x0 | 30 Bit | Versatz vom Anfang des REL zum Abschnitt. Wenn dies null ist, ist der Abschnitt ein nicht initialisierter Abschnitt (dh .bss). |
| 0x3,6 | 1 Bit | Unbekannt. |
| 0x3,7 | 1 Bit | Ausführbares Flag; wenn dies 1 ist, ist der Abschnitt ausführbar. |
| 0x4 | 4 | Länge in Byte des Abschnitts. Ist dieser Null, wird dieser Eintrag übersprungen. |
| 0x8 | Nächster Eintrag | Nächster Eintrag |

### Umzugsdaten
Die Verschiebungsdaten sind eine oder mehrere Listen von 0x8-Byte-Strukturen. Das Ende jeder Liste wird durch den speziellen Typencode 203 gekennzeichnet:
| Versatz | Name | Größe | Beschreibung |
-------|------------|------------|-----|
| 0x0 | Offset | 2 | Offset in Bytes von der vorherigen Verschiebung zu dieser. Handelt es sich um die erste Verschiebung im Abschnitt, ist dies relativ zum Abschnittsanfang. |
| 0x2 | Typ | 1 | Der Umzugstyp. Nachstehend beschrieben. |
| 0x3 | Abschnitt | 1 | Der Abschnitt des Symbols, gegen den verschoben werden soll. Für den speziellen Umzugstyp 202 ist dies stattdessen die Nummer des Abschnitts in dieser Datei, für den die folgenden Umzugseinträge gelten. |
| 0x4 | Nachtrag | 4 | Offset in Bytes des Symbols, gegen das verschoben werden soll, relativ zum Beginn seines Abschnitts. Dies ist stattdessen eine absolute Adresse für Umzüge gegen main.dol. |
| 0x8 | Nächster Eintrag | Nächster Eintrag | Nächster Eintrag |


 




## Verweise


* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


