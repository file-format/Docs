{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PET-Dateiformat - Puppy Linux-Installationspaketdatei",
  "description":"Erfahren Sie mehr über das PET-Dateiformat und APIs, die PET-Dateien erstellen und öffnen können.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
"identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Was ist eine Linux-PET-Datei?

Eine PET-Datei ist eine Anwendungsinstallationspaketdatei, die mit der PuppyLinux-Variante des Linux-Betriebssystems erstellt und verwendet wird. Es wird als komprimierte [TGZ](/de/compression/tgz/)-Datei erstellt, die die Dateigröße des komprimierten Archivs reduziert. Die Integrität des PET-Dateiformats wird durch die Prüfsumme md5sum sichergestellt, die zur Überprüfung am entfernten Ende an das Ende der Datei angehängt wird. PET-Dateien können mit dem standardmäßigen TGZ-Dateiextraktor und WinRAR extrahiert werden. PET-Dateien ersetzten die alten [PUP](/de/compression/pup/)-Paketinstallationsdateien.

## PET-Dateiformat

PET-Dateien werden als komprimierte Archive im Binärdateiformat auf Disc gespeichert. Die internen Dateiformatdetails des PET-Dateiformats sind jedoch nicht bekannt. Ähnlich wie [.exe](/de/executable/exe/)- und [.msi](/de/executable/msi/)-Paketinstallationsdateien starten die PET-Dateien eine Installation, wenn sie ausgeführt werden.

## Verweise

* [WelpenLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Index der PuppyLinux-PET-Pakete](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

