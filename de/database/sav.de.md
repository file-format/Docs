{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "was ist eine SAV-Datei" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das SAV-Dateiformat und APIs, die SAV-Dateien erstellen und öffnen können.",
  "title" :"SAV - SPSS-Datendatei",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
"identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Was ist eine SAV-Datei?
Die SAV-Datei ist eine Datendatei, die vom Statistical Package for the Social Sciences (SPSS) erstellt wurde, einer Anwendung, die häufig von Marktforschern, Gesundheitsforschern, Umfrageunternehmen, Regierungen, Bildungsforschern, Marketingorganisationen und Data Minern für statistische Analysen verwendet wird. Das SAV wird in einem proprietären Binärformat gespeichert und besteht aus einem Datensatz sowie einem Wörterbuch, das den Datensatz darstellt, speichert Daten in Zeilen und Spalten.

## SAV-Dateiformat
Das SAV-Dateiformat ist relativ stabil geworden, aber wir können nicht sagen, dass es statisch ist. Abwärts- und Aufwärtskompatibilität ist gegebenenfalls optional verfügbar, wird jedoch nicht ordnungsgemäß gepflegt. Die Daten in einer SAV-Datei sind in folgende Abschnitte kategorisiert:

### Dateikopf
Es besteht aus 176 Bytes. Die ersten 4 Bytes geben die Zeichenfolge **$FL2** oder **$FL3** in der für die Datei verwendeten Zeichenkodierung an. Die letzten drei Bytes stellen dar, dass die Daten in der Datei mit **ZLIB** komprimiert werden. Die nächste 60-Byte-Zeichenfolge beginnt mit **@(#) SPSS DATA FILE** und bestimmt auch das Betriebssystem und die SPSS-Version, die die Datei erstellt haben. Der Header setzt sich dann mit sechs Ziffernfeldern fort, die die Anzahl der Variablen pro Beobachtung und einen Zifferncode für die Komprimierung enthalten, und endet mit Zeichendaten, die Erstellungsdatum und -zeit sowie eine Dateibezeichnung angeben.
### Variablendeskriptordatensätze
Der Datensatz enthält eine feste Folge von Feldern, die den Typ und Namen der Variablen zusammen mit den von SPSS verwendeten Formatierungsinformationen klassifizieren. Jeder Variablensatz kann optional eine Variablenbezeichnung von bis zu 120 Zeichen und bis zu drei Angaben zu fehlenden Werten enthalten.
### Wertelabels
Die Wertelabels sind optional und werden in Datensatzpaaren mit den Integer-Tags 3 und 4 gespeichert. Der erste Datensatz, der Tag 3 ist, hat eine Folge von Feldpaaren, wobei jedes Paar einen Wert und das zugehörige Wertelabel enthält. Der zweite Datensatz, Tag 4, stellt dar, für welche Variablen der Satz von Werten/Bezeichnungen gilt.
### Dokumente
Einzelne oder mehrere Datensätze mit Integer-Tag 6. Optionale Dokumentation. enthält Zeilen mit 80 Zeichen.
### Erweiterungsdatensätze
Einzelne oder mehrere Datensätze mit dem Integer-Tag 7. Erweiterungsdatensätze stellen Informationen bereit, die sicher ignoriert werden können, aber in vielen Situationen beibehalten werden, sodass Dateien, die von neuerer Software geschrieben wurden, die Abwärtskompatibilität bewahren können. Erweiterungsdatensätze haben ganzzahlige Untertyp-Tags.
### Wörterbuchabschlusszeichen
Nehmen Sie nur mit dem Integer-Tag 999 auf. Es trennt das Wörterbuch von den Datenbeobachtungen.
### Datenbeobachtungen
Es wird davon ausgegangen, dass die Daten in Beobachtungsreihenfolge vorliegen, z. B. alle Variablenwerte für die erste Beobachtung, gefolgt von allen Werten für die zweite Beobachtung usw. Das Format des Datensatzes variiert je nach Komprimierungscode im Dateikopfdatensatz. Der Datenteil einer .sav-Datei kann dekomprimiert werden:
- **Code 0**: Bytecode komprimiert
- **Code 1**: komprimiert mit ZLIB-Komprimierung
 







## Verweise ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

