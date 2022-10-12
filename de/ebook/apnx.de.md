{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon Page Number Index", "extension", "file", "format", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das Amazon APNX-Dateiformat und APIs, die APNX-Dateien erstellen und öffnen können.",
  "title" :"APNX - Index der Amazon-Seitenzahl",
  "linktitle" :"APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Was ist eine APNX-Datei? ##

Die Amazon Page Number Index-Datei, die die Erweiterung .apnx verwendet, ist ein eBook-Dateityp; Wird von Amazon Kindle verwendet. Diese Dateien sind eigentlich als Paginierungsdateien bekannt, die von Kindle-Geräten verwendet werden. Daher werden die APNX-Dateien normalerweise erstellt, um die Seiten von Kindle eBooks zu markieren. Die Paginierungsfunktion wurde auf Amazon Kindle-Geräten seit der Firmware 3.1 gestartet. Es sucht in der APNX-Datei nach Seitenindizes und ordnet sie dann den Seitenzahlen im gedruckten Originalbuch zu. Diese Dateien werden zusammen mit Amazon eBooks-Dateien auf Kindle-Geräten gespeichert. Sie können die APNX-Dateien nicht öffnen oder bearbeiten.

## Spezifikationen des APNX-Dateiformats ##

### Layout

|Bytes| Inhalt| Kommentare|
---|---|---|
|4 |00010001 | Formatkennung. Wert von 65537 Little-Endian.|
|4 |Beginn des nächsten | Der Versatz nach der Endposition des ersten Headers. Startet eine neue Sequenz von Header info|
|4 |Länge| Länge des ersten Headers|
|N |erste Überschrift | Zeichenfolge mit Inhaltsheader. Es beginnt mit der nächsten Sequenz|
|2 |unbekannt | Immer 1|
|2 |Länge | Länge des zweiten Headers|
|2 |Seitenanzahl | Gesamtzahl der Bytes nach dem zweiten Header, die Seiten darstellen. Diese Gesamtzahl enthält Bytes, die von der pageMap ignoriert werden.|
|2 |unbekannt | Immer 32|
|N |zweiter Header | Zeichenfolge, die den Header der Seitenzuordnung enthält|
|4*N |Auffüllung | Die erste im Kopf der Seitenzuordnung angegebene Zahl gibt die Anzahl der 0-Bytes an.|
|4*N |Seitenliste ||

### Inhaltskopfzeile

Der Content-Header besteht aus einer in {} eingeschlossenen Zeichenfolge, die Schlüssel-Wert-Paare enthält:

|Inhalt| Kommentare|
---|---|
|contentGuide| Führer.|
|asin | Amazon-ID für die Kindle-Version des Buchs.|
|cdeTyp | MOBI cdeType. Sollte für eBooks immer EBOK sein.|
|fileRevisionId | Revision dieser Datei.|

#### Beispiel
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Seitenzuordnungskopf
Der Header der Seitenzuordnung besteht aus einer in {} eingeschlossenen Zeichenfolge, die Schlüssel-Wert-Paare enthält.

|Inhalt | Kommentare|
---|---|
|asin | Die ISBN 10 für das Papierbuch, dem die Seiten entsprechen|
|pageMap| Tupel mit drei Werten. Sieht so aus: "(N,N,N)\
1) Anzahl der Bytes nach dem Header, der die Seitennummerierungssequenz beginnt\
2) unbekannt\
3) unbekannt\|
#### Beispiel
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Seitenliste

Die Seitenliste ist eine Folge von Offsets im Roh-HTML. Jeder
Wert ist der Anfang einer neuen Seite. Jeder Eintrag ist ein 4-Byte-Big-Endian
int.



## Verweise

* [Amazon APNX-Dateiformat](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX – von MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

