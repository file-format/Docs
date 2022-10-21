{
  "date" : "2021-08-16",
  "keywords" :[ "NRG-Datei", "NRG-Dateiformat", "Was ist eine NRG-Datei", "Datei", "NRG-Beispiel", "NRG-Dateierweiterung", "Erweiterung", "Format", "NRG-Fußzeile", "Datei format von nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie mehr über das NRG-Dateiformat und APIs, die NRG-Dateien erstellen und öffnen können.",
  "title" :"NRG - Disk-Image-Dateiformat",
  "linktitle" :"NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## Was ist eine NRG-Datei?

Ein Bilddateiformat, das durch die Verwendung einer optischen Disc erstellt wird, wird als NRG-Dateiformat betrachtet. Dieses Format wurde von Nero speziell für das Dienstprogramm von Nero Burning Rom erstellt. Für die Speicherung von Disc-Images wird dieses Format als verwendet angesehen, da es für diese spezifischen Dateien geeignet ist. Diese Dateien können in Form einer exakten Kopie einer CD oder DVD vorliegen oder mehrere Dateien enthalten, die als Datenträger gemountet werden können. Andere populärere Dateiformate wie [ISO](/de/compression/iso/)-Dateiformate sind diejenigen, in die diese Dateien in einige grundlegende Dienstprogramme konvertiert werden können. Meistens werden die NRG-Dateien verwendet, um Backups oder Kopien einiger wichtiger Daten oder Discs zu erstellen.

## NRG-Dateiformat ##

Dieses Dateiformat wurde von der Nero AG als Disk-Image-Format entwickelt. Es hatte die spezifischen Eigenschaften des Dienstprogramms Nero Burning Rom, da es zum Speichern von Disc-Images entwickelt wurde. Seine erste Version wurde spezifiziert, um Werte als 32-Bit-Ganzzahlen zu speichern. Die zweite Version wurde jedoch gestartet und enthielt Unterstützung für 64-Bit-Ganzzahlen.

## Technische Spezifikation ##

Am Anfang der Datei speichert dieses Format seine Daten nicht als Header. Sie wird wie eine Fußzeile am Ende der Datei angehängt. In Form von IFF-Blöcken werden die Informationen des Bildes gespeichert. Der Offset des ersten Chunks kann durch Lesen der NRG-Fußzeile in den letzten 8 Bytes bis 12 Bytes der Datei erhalten werden. In allen Versionen des NRG-Dateiformats gibt es Chunks, DAOI, CD-Text, Sitzungsinformationen, Medientyp, Disc-Informationen, Relo und das Ende der damit verbundenen Kette. Die Byte-Reihenfolge ist Big-Endian und alle Integer-Werte sind zum Zeitpunkt der Speicherung vorzeichenlos.

### Hauptstücke ###

#### Cue-Sheet ####

Dieses Cue-Sheet ist in allen Versionen des NRG-Dateiformats leicht verfügbar. Der Chunk von **CUEX** bedeutet die Blöcke der Verkettung mit fester Größe, und jeder von ihnen repräsentiert den Cue-Punkt.

#### DAO-Informationen ####

Diese Informationen sind auch in allen Versionen des NRG-Formats vorhanden. Die Chunks von **DAOI** speichern die relevanten spezifischen Informationen in 2 Teilen. Ihr erster Teil besteht nur aus den sitzungsspezifischen Daten. Der zweite Teil wiederholt nur die grauen Informationen zum Tracking und es ist nur einmal für jeden Track.

#### CD-Text ####

Dies ist in der zweiten Version von NRG verfügbar. Der Chunk von **CDTX** besteht aus der rohen Verkettung des CD-Textpakets mit jeweils 18 Bytes.

#### Erweiterte Titelinformationen ####

Dies ist in jeder Version des Dateiformats von NRG verfügbar. Diese Chunks werden zum Speichern der Verfolgungsinformationen für die Verfolgung der einzelnen Sitzungen verwendet. Diese Daten werden bei jeder Spur nur einmal wiederholt.

#### Sitzungsinformationen ####

Dies ist auch in jeder Version des Dateiformats von NRG verfügbar. Die Informationen der Sitzungsblöcke müssen verwendet werden, um das Bild der Sitzung schnell zu scannen und dann die Anzahl zu verfolgen.

#### Ende der Kette ####

Der Chunk of End bedeutet, dass jetzt keine Chunks mehr gelesen werden müssen und dies ist auch in allen Versionen von NRG verfügbar.


## Verweise ##

* [NRG - von Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


