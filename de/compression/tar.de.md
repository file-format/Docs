{
  "date" : "2019-10-11",
  "keywords" :[ "tar-Datei", "tar-Dateiformat", "was ist eine tar-Datei", "Datei", "tar-Beispiel", "tar-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Unix-Archivdateiformat",
  "description":"Erfahren Sie, was eine Tar-Datei und APIs sind, die TAR-Dateien erstellen und öffnen können.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine TAR-Datei?

Dateien mit der Erweiterung .tar sind Archive, die mit einem Unix-basierten Dienstprogramm zum Sammeln einer oder mehrerer Dateien erstellt wurden. Mehrere Dateien werden in einem unkomprimierten Format gespeichert, wobei das Hinzufügen von Dateien und Ordnern zum Archiv unterstützt wird. Das TAR-Dienstprogramm unter Unix ist befehlsbasiert, aber die so erstellten Dateien werden von den meisten Dateiarchivierungssystemen auf fast allen Betriebssystemen unterstützt. Es wurde erstmals 1979 von den AT&T Bell Laboratories erstellt und im Laufe der Zeit wurden nachfolgende Versionen veröffentlicht.

## TAR-Dateiformat

TAR ist ein offenes Dateiformat mit vollständigen Spezifikationen, die Entwicklern als Referenz zur Verfügung stehen. Seine Dateistruktur wurde in POSIX.1-1988 und später in POSIX.1-2001 standardisiert. Die von tar erstellten Datensätze enthalten Informationen über Dateisystemparameter wie:

* Name
* Zeitstempel
* Eigentum
* Dateizugriffsberechtigungen
* Verzeichnisorganisation

Eine Tar-Datei hat keine magische Zahl. Es enthält eine Reihe von Blöcken, wobei jeder Block aus BLOCKSIZE-Bytes besteht.

Jede archivierte Datei wird durch einen Kopfblock dargestellt, der die Datei beschreibt, gefolgt von null oder mehr Blöcken, die den Inhalt der Datei angeben. Am Ende der Archivdatei befinden sich zwei mit binären Nullen gefüllte 512-Byte-Blöcke als Dateiende-Markierung. Ein vernünftiges System sollte eine solche Dateiende-Markierung am Ende eines Archivs schreiben, darf aber beim Lesen eines Archivs nicht davon ausgehen, dass ein solcher Block existiert. Insbesondere GNU tar gibt immer eine Warnung aus, wenn es nicht darauf stößt.

Die Blöcke können für physische E/A-Operationen blockiert werden. Jeder Datensatz von n Blöcken (wobei n durch die Option "blocking-factor = 512-size" auf tar gesetzt wird) wird mit einer einzigen "write()"-Operation geschrieben. Auf Magnetbändern ist das Ergebnis eines solchen Schreibens ein einzelner Datensatz. Beim Schreiben eines Archivs sollte der letzte Satz von Blöcken in voller Größe geschrieben werden, wobei die Blöcke nach dem Nullblock nur Nullen enthalten. Beim Lesen eines Archivs sollte ein vernünftiges System ein Archiv richtig handhaben, dessen letzter Datensatz kürzer als der Rest ist oder das Mülldatensätze nach einem Nullblock enthält.

### Tar-Header

Wie alle anderen Datei-Header enthält der TAR-Datei-Header-Datensatz Metadaten zu einer Datei und wird in der folgenden Tabelle angezeigt.


|Feldoffset|Feldgröße (Bytes)|Feld
---|---|---|
|0|100|Dateiname
|100|8|Dateimodus
|108|8|Numerische Benutzer-ID des Besitzers
|116|8|Numerische Benutzer-ID der Gruppe
|124|12|Dateigröße in Byte (Oktalbasis)
|136|12|Letzte Änderungszeit im numerischen Unix-Zeitformat (oktal)
|148|8|Prüfsumme für Header-Datensatz
|156|1|Link-Indikator (Dateityp)
|157|100|Name der verknüpften Datei

Nicht verwendete Felder werden mit NUL-Bytes gefüllt. Ein Header besteht aus 257 Bytes, die mit NUL-Bytes aufgefüllt werden, damit sie einen 512-Byte-Datensatz füllen.

## Verweise ##

* [TAR - Von Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [TAR Basic Format](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

