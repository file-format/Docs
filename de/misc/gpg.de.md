{
  "date" : "2022-02-17",
  "keywords" :["gpg-Datei", "gpg-Dateiformat", "was ist eine gpg-Datei", "Datei", "gpg-Beispiel", "gpg-Dateierweiterung", "Erweiterung", "Format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG-Datei - GNU Privacy Guard Public Keyring-Datei",
  "description":"Erfahren Sie mehr über GPG-Dateien und APIs, die GPG-Dateien erstellen und öffnen können.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Was ist eine GPG-Datei?

Eine GPG-Datei ist eine Verschlüsselungs-/Entschlüsselungsschlüsseldatei, die vom Verschlüsselungsprogramm GNU Privacy Guard (GnuPG) verwendet wird. Das GnuPC-Programm selbst basiert auf dem OpenPGP-Standard, der als RFC4880 definiert ist und auch als PGP bekannt ist. Der Schlüssel zum erfolgreichen Einsatz von GPG in modernen Betriebssystemen ist sein vielseitiges Schlüsselverwaltungssystem. Das Befehlszeilenprogramm von GPG ermöglicht eine einfache Integration mit anderen Anwendungen.

## GPG-Dateiformat

GPG-Dateien werden als verschlüsselte Binärdateien gespeichert und sind natürlich nicht für Menschen lesbar. Um eine verschlüsselte GPG-Datei zu entschlüsseln, müssen Sie denselben sicheren Schlüssel verwenden. Und deshalb ist das interne Dateiformat dieser Dateien nicht bekannt.

## Verschlüsseln und Entschlüsseln von Dateien mit GPG unter Linux

Das GPG-Befehlszeilendienstprogramm kann zum Verschlüsseln und Entschlüsseln von Dateien unter Linux verwendet werden.

### Verschlüsseln einer Datei

Eine Datei kann mit dem gpg-Befehl mit der Option -c (create) wie unten gezeigt verschlüsselt werden.

```
gpg -c file1.txt
```
Das Ausführen dieses Befehls fragt nach einem Schlüsselsatz, mit dem der Inhalt der Originaldatei „file1.txt“ verschlüsselt werden soll. Dies führt zur Erstellung der verschlüsselten Datei file1.txt.gpg.

### Entschlüsseln und Extrahieren einer Datei

Um eine verschlüsselte Datei zu entschlüsseln und zu extrahieren, kann der folgende Befehl verwendet werden.

```
gpg cfile.txt.gpg
```

## Verweise

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

