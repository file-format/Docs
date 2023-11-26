{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO-Datei – Unix CPIO-Archivdateiformat",
  "description":"Erfahren Sie, was eine CPIO-Datei ist und welche APIs es gibt, mit denen CPIO-Dateien erstellt und geöffnet werden können.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Was ist eine CPIO-Datei?

Eine CPIO-Datei ist eine Archivdatei, die im Unix-CPIO-Format (Copy In Copy Out) erstellt wurde. Es ähnelt dem TAR-Dateiformat, ist jedoch unkomprimiert. CPIO-Dateien können Gerätedateien, symbolische Links und erweiterte Dateiattribute speichern.

## CPIO-Dateiformat

Ein CPIO-Archiv wird als Binärdatei erstellt, die nicht für Menschen lesbar ist. Es speichert die Sammlung von Dateien und Verzeichnissen. Der Inhalt eines CPIO-Archivs wird durch Metadateninformationen wie Dateinamen, Berechtigungen, Eigentümer und Zeitstempel identifiziert. Diese Metadateninformationen werden auch in der Archivdatei für den seitlichen Zugriff durch das System gespeichert.

## Format des CPIO-Archivs

Eine CPIO-Datei besteht aus einer oder mehreren verketteten Mitgliedsdateien. Jede Datei im Archiv besteht aus einem Header, optional gefolgt vom Dateiinhalt, wie im Header angegeben. Das Archiv enthält am Ende einen weiteren Header, der durch eine leere Datei namens TRAILER!! beschrieben wird.

### Arten von CPIO-Archiven

Es gibt zwei Arten von CPIO-Archiven. Diese unterscheiden sich lediglich im Stil der Kopfzeile.

* ASCII-Archive – Diese CPIO-Archive verfügen über einen druckbaren Header, der Teil des CPIO-Archivs wird, wenn das Archiv selbst aus ASCII-Dateien besteht
* Binäre Archive – Diese CPIO-Archive haben binäre Header.

## Arbeiten mit CPIO-Archiv

### Wie erstelle ich CPIO-Archive?

Sie können einen CPIO auf Unix-ähnlichen Systemen mit dem Befehl **cpio** erstellen. Der folgende Befehl findet alle Dateien und Verzeichnisse im aktuellen Verzeichnis und seinen Unterverzeichnissen. Diese Ausgabe wird dann an den cpio-Befehl weitergeleitet, der ein neues CPIO-Archiv mit dem Namen archive.cpio generiert.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Wie extrahiere ich Dateien aus CPIO-Archiven?

Der folgende Befehl extrahiert die Dateien aus einem vorhandenen Archiv.

```
cpio -id < archive_cpio.cpio
```
Es liest die Datei archive.cpio aus der Standardeingabe und extrahiert die Dateien in das aktuelle Verzeichnis.


## Verweise

* [CPIO – Von Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [CPIO-Dateiformat](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

