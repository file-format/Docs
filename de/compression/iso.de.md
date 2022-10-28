{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Disk-Image-Dateiformat",
  "description":"Was ist eine ISO-Datei und APIs, die ISO-Dateien erstellen und öffnen können.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
"identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Was ist eine ISO-Datei?

Eine Datei mit der Erweiterung .iso ist eine unkomprimierte Disk-Image-Archivdatei, die den Inhalt vollständiger Daten auf einer optischen Disc wie CD oder DVD darstellt. Basierend auf dem Standard [ISO-9660](https://www.iso.org/standard/17505.html) enthält das ISO-Image-Dateiformat die Disc-Daten zusammen mit den darin gespeicherten Dateisysteminformationen. Die Fähigkeit von ISO-Dateien, eine exakte Kopie des Inhalts zu enthalten, macht sie zum perfekten Dateityp zum Erstellen von Kopien von CDs/DVDs und wird hauptsächlich zum Speichern von bootfähigen Daten für die Installation verwendet. Meistens werden ISO-Dateien als bootfähiger Inhalt zum Booten des Computers für die Installation auf USB/CD/DVD gebrannt. ISO-Dateien haben den MIME-Typ application/x-iso9660-image.

## ISO-Dateiformat

Das ISO-Dateiformat ist nicht wie andere Containerdatei-Dateiformate, obwohl es die angegebenen Dateninhalte archiviert. Das Archiv wird als Binärdatei mit der genauen Struktur der Inhalte und Dateisysteminformationen erstellt. Das ISO-Dateiformat wird von [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) wie folgt beschrieben.

### Top-Level-Struktur der ISO-Datei

Die Gesamtstruktur der Datei besteht aus:

* `System Area` - 32.768 Bytes und wird von ISO_9660 nicht verwendet
* `Data Area` - besteht aus Volume-Deskriptorensatz und Pfadtabellen, Verzeichnissen und Dateien

### Volume Descriptor Set

Der Datenbereich beginnt mit dem Datenträgerdeskriptorsatz, einem Satz aus einem oder mehreren Datenträgerdeskriptoren, der mit einem Datenträgerdeskriptorsatz-Beendigungszeichen endet. Diese fungieren gemeinsam als Header für den Datenbereich und beschreiben dessen Inhalt (ähnlich dem BIOS-Parameterblock, der von FAT-, HPFS- und NTFS-formatierten Festplatten verwendet wird).

Ein Volumendeskriptorsatz ist wie unten gezeigt.

|Datenträgerdeskriptorsatz|
---|
|Volume-Deskriptor #1|
|...|
|Volume-Deskriptor #N|
|Terminator des Datenträgerdeskriptorsatzes|

#### Volume-Deskriptor

Jeder Datenträgerdeskriptor ist 2048 Byte groß und hat die folgende Struktur:

|Teil |Typ |Bezeichner |Version |Daten|
---|---|---|---|---|
|Größe |1 Byte |5 Byte (immer 'CD001') |1 Byte (immer 0x01) |2.041 Byte|

## Verweise

* [Optical Disk Image – Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Dateisignaturen](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 – Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

