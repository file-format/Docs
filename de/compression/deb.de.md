{
  "date" : "2021-04-08",
  "keywords" :[ "deb-Datei", "deb-Dateiformat", "was ist eine deb-Datei", "Datei", "deb-Beispiel", "deb-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip-komprimiertes Tar-Archiv",
  "description":"Erfahren Sie mehr über das DEB-Dateiformat und APIs, die DEB-Dateien erstellen und öffnen können.",
  "linktitle" :"DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Was ist eine DEB-Datei?

Eine Datei mit der Erweiterung .deb ist ein Debian-Binärpaketdateiformat, das für die Verteilung von Softwarepaketen unter Linux OS verfügbar ist. Es besteht aus zwei [TAR](/de/compression/tar/)-Archivdateien. Das DPKG stellt den Mechanismus zum Lesen und Installieren der DEB-Pakete bereit. DEB-Pakete können mithilfe der APT-Paketsoftwareverwaltungsschnittstelle installiert werden. DEB-Dateien haben den Internet Media Type als `application/vnd.debian.binary-package`.

## DEB-Dateiformat

Eine DEB-Datei besteht aus zwei [TAR](/de/compression/tar/)-Archivdateien. Ein Archiv enthält die Steuerinformationen und ein anderes die installierbaren Daten.

### Paketorganisation

Die DEB-Datei ist eine **ar**-Archivdatei mit dem magischen Wert `!<arch> `. Seit Debian 0.93 enthält der Archivierungsmechanismus von DEB-Dateien drei Dateien in einer bestimmten Reihenfolge.

1. `Debian Binary` - Es ist dazu bestimmt, eine Reihe von Zeilen zu haben, die durch Zeilenumbrüche getrennt sind. Derzeit ist nur eine einzige Zeile vorhanden, die die Versionsnummer beschreibt. Die aktuelle Versionsnummer ist 2.0.
1. „Kontrollarchiv“ – Es enthält ein control.tar-Archiv, das Betreuerskripte und Metainformationen über das Paket enthält, wie Paketname, Version, Abhängigkeiten und Betreuer.
1. „Datenarchiv“ – Es ist ein Tar-Archiv mit dem Namen data.tar und enthält die tatsächlich installierbaren Mediendateien. Das Archiv kann mit gz, bz2, lzma oder xz komprimiert werden, und die Dateierweiterung des Datenarchivs ändert sich entsprechend.

### Kontrollarchiv

Das Steuerarchiv kann folgende Inhalte enthalten.

* `control` - Es enthält eine kurze Beschreibung des Pakets sowie andere Informationen wie seine Abhängigkeiten.
* `md5sums` - Enthält MD5-Prüfsummen aller Dateien im Paket, um beschädigte oder unvollständige Dateien zu erkennen.
* `conffiles` - Es listet die Dateien des Pakets auf, die als Konfigurationsdateien behandelt werden sollen. Konfigurationsdateien werden während einer Aktualisierung nicht überschrieben, sofern nicht anders angegeben.
* `preinst`, postinst, prerm und postrm - Optionale Skripte, die vor oder nach der Installation oder Entfernung des Pakets ausgeführt werden
* `config` ist ein optionales Skript, das den Debconf-Konfigurationsmechanismus unterstützt.
* `shlibs` - Dies ist eine Liste von Abhängigkeiten von gemeinsam genutzten Bibliotheken.

## Verweise

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(Dateiformat))
* [Debian-Binärpaketformat](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

