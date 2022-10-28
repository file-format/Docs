{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extension", "file", "format", "system", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows Cabinet-Datei",
  "description":"Erfahren Sie mehr über das CAB-Dateiformat und APIs, die CAB-Dateien erstellen und öffnen können.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Was ist eine CAB-Datei? ##

Eine Datei mit der Erweiterung .cab gehört zu einer Windows Cabinet-Datei, die zur Kategorie der Systemdateien gehört. Es handelt sich um eine Datei, die im Archivdateiformat in den Versionen von Microsoft Windows gespeichert wird, die komprimierte Datenalgorithmen unterstützen, wie [LZX](/de/compression/lzx/), Quantum und [ZIP](/de/compression/zip/ ). Die Datei ist von entscheidender Bedeutung, wenn ein Benutzer oder Entwickler Softwareinstallationsdaten und -dateien enthalten und freigeben möchte. Die Funktionen der verlustfreien Datenkomprimierung und die in diesen Dateien enthaltene digitale Zertifizierung machen diese Datei perfekt zum Speichern und Teilen solcher Dateien. Es unterstützt verschiedene Microsoft-Installationsprogramme wie Device Installer, SetUp API und AdvPak.

## Kurze Geschichte ##

CAB-Datei ist ein Datenkomprimierungsdateityp, der von Microsoft entwickelt wurde. Es hieß ursprünglich "Diamond", wurde dann aber im Volksmund als CAB-Datei bekannt, kurz für das Wort "Cabinet".

## Technische Spezifikation ##

Eine CAB-Datei kann normalerweise bis zu maximal 65535 Ordner enthalten, die wiederum jeweils maximal 65536 Dateien enthalten können. Der CAB-Dateispeichermechanismus ist zeit- und platzsparend, da er jeden Ordner als komprimierten Block speichert, anstatt jede Datei separat zu komprimieren und zu speichern. Leere Ordner können nicht in CAB-Archivordnern gespeichert werden. Die CAB-Datei wurde zuerst von Microsoft entwickelt und wird in verschiedenen Installern wie InstallShield mit einem etwas anderen Format verwendet. CAB-Dateien sind häufig mit selbstextrahierenden Programmen verbunden. Microsoft CAB-Dateien sind aufgrund ihrer eindeutigen Markierung, die bei der Identifizierung des Formats hilft, leicht erkennbar. Die eindeutige Markierung für alle Microsoft CAB-Dateien ist ein aus vier Wörtern bestehendes Präfix, MSCF. Wenn ein Benutzer diesen Code sieht, kann er eine Microsoft CAB-Datei leicht von anderen Dateien unterscheiden und sie entsprechend in Kompressoren oder Versionen verwenden. Die Dateien können mit mehr Softwareinstallationsdaten komprimiert werden, oder die vorhandenen Daten können mit der richtigen Software dekomprimiert werden.


## CAB-Beispiel ##

Das folgende Beispiel veranschaulicht die Beziehung zwischen Dateien und Ordnern in einer CAB-Dateistruktur:

{{< figure src="../cab.png" alt="CAB-Dateiformat" >}}

## Bezug ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
