{
  "date" : "2021-04-08",
  "keywords" :[ "dar-Datei", "dar-Dateiformat", "was ist eine dar-Datei", "Datei", "dar-Beispiel", "dar-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Disk Archiver-Dateiformat",
  "description":"Erfahren Sie mehr über das DAR-Dateiformat und APIs, die DAR-Dateien erstellen und öffnen können.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Was ist eine DAR-Datei?

Eine Datei mit der Erweiterung .dar ist ein komprimiertes Archiv, das mit dem DAR Disk-Archiv erstellt wurde. Es kann eine Sicherung/Archivierung für eine ganze Festplatte oder eine Gruppe von Dateien erstellen. Es wurde erstellt, um das Dateiformat [TAR](/de/compression/tar/) auf UNIX-Betriebssystemen zu ersetzen, und kann als aufgeteilte Archivdateien für eine große Anzahl von Dateien erstellt werden. Das DAR-Archiv unterstützt die Möglichkeit, Dateien aus dem System zu löschen, die mit den Hauptdateien im Archiv verknüpft sind. Seine Fähigkeit, differenzielle, inkrementelle und dekrementelle Sicherungen bereitzustellen, macht es besser als TAR-Dateien.

## DAR-Dateiformat

DAR-Dateien sind komprimierte Archive, die jede dateispezifische Komprimierung wie [gzip](/de/compression/gz/), [bzip2](/de/compression/bz2/), lzo, xz oder lzma verwenden können. Das genaue Dateiformat einer DAR-Datei hängt davon ab, welche Art von Formatierung verwendet wird, um den Inhalt des Archivs zu komprimieren. Es ermöglicht auch optionale Blowfish-, Twofish-, AES-, Serpent-, Camellia-Verschlüsselung und Public-Key-Verschlüsselung und -Signatur (OpenPGP).

### DAR-Funktionen

Einige der Merkmale des DAR-Dateiformats sind wie folgt.

* Kümmert sich um jede Art von Inode (Verzeichnis, einfache Dateien, Symlinks, spezielle Geräte, Named Pipes, Sockets, Doors, ...)
* Kümmert sich um fest verknüpfte Inodes (fest verknüpfte einfache Dateien, Zeichengeräte, Blockgeräte, fest verknüpfte Symlinks)
* Kümmert sich um spärliche Dateien
* Kümmert sich um die erweiterten Attribute der Linux-Datei,
* Kümmert sich um die ACL der Linux-Datei
* Kümmert sich um Mac OS X-Dateigabelungen
* Berücksichtigt einige dateisystemspezifische Attribute wie Geburtsdatum des HFS+-Dateisystems und unveränderliche, Daten-Journaling, sichere Löschung, No-Tail-Merging, undeletable, Noatime-Attribute des ext2/3/4-Dateisystems.
* Komprimierung pro Datei mit gzip, bzip2, lzo, xz oder lzma (im Gegensatz zur Komprimierung des gesamten Archivs). Eine Person kann entscheiden, bereits komprimierte Dateien basierend auf ihrem Dateinamensuffix nicht zu komprimieren.
* Schnelles Extrahieren von Dateien von überall im Archiv
* Schnelles Auflisten von Archivinhalten durch Speichern des Dateikatalogs im Archiv
* Live-Dateisystem-Backup: erkennt, wenn eine Datei geändert wurde, während sie zur Sicherung gelesen wurde, und kann bis zu einer bestimmten maximalen Anzahl von Wiederholungen versuchen, sie zu speichern
* Hash-Datei (MD5, SHA1 oder SHA-512), die on-fly für jeden Slice generiert wird, die resultierende Datei ist mit md5sum oder sha1sum kompatibel, um die Integrität jedes Slice schnell überprüfen zu können
* Unabhängig vom Dateisystem: Es kann verwendet werden, um ein System auf einer Partition mit einer anderen Größe und/oder auf einer Partition mit einem anderen Dateisystem wiederherzustellen[5]

## Verweise

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

