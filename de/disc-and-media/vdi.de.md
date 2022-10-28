{
  "date" : "2021-08-11",
  "keywords" :[ "vdi-Datei", "vdi-Dateiformat", "was ist eine vdi-Datei", "Datei", "vdi-Beispiel", "vdi-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie mehr über das VDI-Dateiformat und APIs, die VDI-Dateien erstellen und öffnen können.",
  "title" :"VDI - Image-Datei der virtuellen VirtualBox-Festplatte",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Was ist eine VDI-Datei?
Eine Datei mit der Erweiterung .vdi ist ein virtuelles Disk-Image; spezifisch für das Open-Source-Desktop-Virtualisierungsprogramm von Oracle namens VirtualBox. Die VDI-Dateien werden verwendet, um die virtuelle VirtualBox-Maschine zu starten. Die VMs ermöglichen es den Benutzern, zusätzliche Betriebssysteme oder Programme auf einem einzelnen Computer auszuführen. Daher besteht der Vorteil von VDI-Dateien darin, dass Benutzer diese Disc-Image-Dateien auf ihrer Festplatte speichern und diese bei Bedarf mit Emulatoren ausführen können.

## VDI-Dateiformat
Virtual Disk Image (VDI) ist das primäre Festplattendateiformat für eine aktiv entwickelte Open-Source-Oracle-VM namens VirtualBox, ein Virtualisierungsprodukt der Enterprise-Klasse. Das VDI-Dateiformat wurde entwickelt, um ein tragbares Disc-Image zu erstellen, das problemlos mit anderen Virtualisierungsprogrammen ausgeführt werden kann. Es unterstützt sowohl dynamisch zugewiesenen als auch Speicher mit fester Größe. Sie können damit eine Bilddatei erweitern, nachdem sie erstellt wurde, selbst wenn sie bereits Daten enthält.

### Disc-Virtualisierung
Das System emuliert Festplatten im VDI-Disk-Image-Format. Eine VirtualBox-VM kann frühere Festplatten verwenden, die in Microsoft Virtual PC oder VMware erstellt wurden, sowie ihr eigenes natives Format. Die VirtualBox ist auch in der Lage, eine Verbindung zu iSCSI-Zielen und Raw-Partitionierung auf dem Host herzustellen, wobei beide als virtuelle Festplatten verwendet werden. VirtualBox emuliert IDE (PIIX4- und ICH6-Controller), SATA (ICH8M-Controller), SAS-Controller, an die Festplatten angeschlossen werden können, und SCSI.

Die Unterstützung für Open Virtualization Format (OVF) ist seit Version 2.2.0 von VirtualBox verfügbar. Sowohl mit dem Host verbundene physische Geräte als auch ISO-Images können als CD- oder DVD-Laufwerke gemountet werden.
Standardmäßig unterstützt VirtualBox Grafiken über eine VESA-kompatible benutzerdefinierte virtuelle Grafikkarte.

### Virtualisierungsunterstützung für Ethernet
VirtualBox virtualisiert die folgenden Netzwerkschnittstellenkarten für einen Ethernet-Netzwerkadapter:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT-Desktop (82540EM)
- Intel Pro/1000 MT-Server (82545EM)
- Intel Pro/1000 T-Server (82543GC)
- Paravirtualisierter Netzwerkadapter (virtio-net)

Die emulierten Netzwerkkarten ermöglichen die Ausführung von Gastbetriebssystemen, ohne dass Treiber für Netzwerkhardware gesucht und installiert werden müssen, da diese als Teil des Gastbetriebssystems verfügbar sind. Ein spezieller paravirtualisierter Netzwerkadapter verbessert die Netzwerkleistung, indem er die Anpassung an eine bestimmte Hardwareschnittstelle reduziert. Daher ist eine spezielle Treiberunterstützung im Gast erforderlich.


## Verweise

* [VirtualBox – von Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


