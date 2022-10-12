{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "Erweiterung", "dbf-Datei", "dbf-Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "was ist eine dbf-Datei", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DBF-Dateiformat und APIs, die DBF-Dateien erstellen und öffnen können.",
  "title" :"DBF - dBase-Datenbankdatei",
  "linktitle" :"DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Was ist eine DBF-Datei?
Die Datei mit der Erweiterung .dbf ist eine Datenbankdatei, die von einer Datenbankverwaltungssystemanwendung namens **dBASE** verwendet wird. Ursprünglich wurde die dBASE-Datenbank als Project Vulcan bezeichnet; wurde 1978 von **Wayne Ratliff** gestartet. Der Dateityp DBF wurde 1983 mit dBASE II eingeführt. Er ordnet mehrere Datensätze mit Feldern vom Typ Array an. Die **xBase**-Datenbanksoftware, die aufgrund ihrer Kompatibilität mit einer Vielzahl von Dateiformaten beliebt ist; unterstützt auch die DBF-Dateien.

## DBF-Dateiformat
Das DBF-Dateiformat gehört zum dBASE-Datenbankverwaltungssystem, ist aber möglicherweise mit xBase oder anderer DBMS-Software kompatibel. Die ursprüngliche Version der dbf-Datei bestand aus einer einfachen Tabelle, in der Daten mithilfe des ASCII-Zeichensatzes hinzugefügt, geändert, gelöscht oder gedruckt werden konnten. Im Laufe der Zeit wurde .dbf verbessert und zusätzliche Dateien wurden hinzugefügt, um die Funktionen und Fähigkeiten des Datenbanksystems zu erweitern.

In modernen dBASE besteht eine DBF-Datei aus einem Header, den Datensätzen und der EOF-Markierung (End of File).

- Der Header enthält Informationen über die Datei, wie z. B. die Anzahl der Datensätze und die Anzahl der in den Datensätzen verwendeten Feldtypen.
- Die Datensätze enthalten die eigentlichen Daten.
- Das Ende der Datei wird durch ein einzelnes Byte mit dem Wert 0x1A gekennzeichnet.

### Dateikopf
Das Layout des Dateikopfs in dBase ist in der folgenden Tabelle angegeben:

| Byte | Inhalt | Bedeutung |
---|---|---|
| 0 | 1 Byte | Gültige dBASE für DOS-Datei; Bits 0–2 geben die Versionsnummer an, Bit 3 zeigt das Vorhandensein einer dBASE für DOS-Memodatei an, Bits 4–6 zeigen das Vorhandensein einer SQL-Tabelle an, Bit 7 zeigt das Vorhandensein einer beliebigen Memodatei an (entweder dBASE m PLUS oder dBASE for DOS) |
| 1–3 | 3 Bytes | Datum der letzten Aktualisierung; formatiert als JJMMTT |
| 4–7 | 32-Bit-Zahl | Anzahl der Datensätze in der Datenbankdatei |
| 8–9 | 16-Bit-Zahl | Anzahl der Bytes im Header |
| 10–11 | 16-Bit-Zahl | Anzahl der Bytes im Datensatz |
| 12–13 | 2 Bytes | Reserviert; mit 0 füllen |
| 14 | 1 Byte | Flag, das eine unvollständige Transaktion anzeigt [Anmerkung 1] |
| 15 | 1 Byte | Verschlüsselungs-Flag [Anmerkung 2] |
| 16–27 | 12 Bytes | Reserviert für dBASE für DOS in einer Mehrbenutzerumgebung |
| 28 | 1 Byte | Produktions-MDX-Datei-Flag; 1, wenn eine .mdx-Produktionsdatei vorhanden ist, 0, wenn nicht |
| 29 | 1 Byte | Sprachtreiber-ID |
| 30–31 | 2 Bytes | Reserviert; mit 0 füllen |
| 32–n [Anmerkung 3][Anmerkung 4] | je 32 Bytes | Array von Felddeskriptoren (siehe unten für das Layout der Deskriptoren) |
| n + 1 | 1 Byte | 0x0D als Felddeskriptor-Array-Terminator |

- Die Funktion ISMARKEDO überprüft dieses Flag (BEGIN TRANSACTION setzt es auf 1, END TRANSACTION und ROLLBACK setzen es auf 0 zurück).
- Wenn dieses Flag auf 1 gesetzt ist, erscheint die Meldung Datenbank verschlüsselt.
- Die maximale Anzahl von Feldern beträgt 255.
- n bedeutet das letzte Byte im Felddeskriptor-Array.

### Felddeskriptor-Array
Layout von Felddeskriptoren in dBASE:

| Byte | Inhalt | Bedeutung |
---|---|---|
| 0–10 | 11 Byte | Feldname in ASCII (mit Nullen gefüllt) |
| 11 | 1 Byte | Feldtyp. Zulässige Werte: C, D, F, L, M oder N (Bedeutung siehe nächste Tabelle) |
| 12–15 | 4 Bytes | Reserviert |
| 16 | 1 Byte | Feldlänge in Binär (maximal 254 (0xFE)). |
| 17 | 1 Byte | Felddezimalzahl in binär |
| 18–19 | 2 Bytes | Arbeitsbereichs-ID |
| 20 | 1 Byte | Beispiel |
| 21–30 | 10 Bytes | Reserviert |
| 31 | 1 Byte | Produktions-MDX-Feldflag; 1, wenn das Feld ein Index-Tag in der Produktions-MDX-Datei hat, 0, wenn nicht |

### Datenbankeinträge
Jeder Datensatz beginnt mit einem Lösch-Flag (1 Byte). Felder werden ohne Feldtrennzeichen in Datensätze eingeschlossen. Alle Felddaten sind ASCII. Je nach Art des Feldes erlegt die Anwendung weitere Einschränkungen auf. Hier sind Feldtypen in dBase:

| Feldtyp | Merkhilfe | Was es akzeptiert |
-------|-----|----|
| C | Zeichen | Beliebiger ASCII-Text (mit Leerzeichen bis zur Feldlänge aufgefüllt) |
| D | Datum | Zahlen und ein Zeichen zur Trennung von Monat, Tag und Jahr (intern als 8 Ziffern im Format JJJJMMTT gespeichert) |
| F | Fließkomma | -, ., 0–9 (rechtsbündig, mit Leerzeichen aufgefüllt) |
| L. | Logisch | Y, y, N, n, T, t, F, f oder ? (wenn nicht initialisiert) |
| M | Notiz | Beliebiger ASCII-Text (intern als 10 Ziffern gespeichert, die eine .dbt-Blocknummer darstellen, rechtsbündig, mit Leerzeichen aufgefüllt) |
| N. | Numerisch | -, ., 0–9 (rechtsbündig, mit Leerzeichen aufgefüllt) |









## Verweise ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

