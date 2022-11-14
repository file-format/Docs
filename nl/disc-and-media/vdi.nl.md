{
  "date" : "2021-08-11",
  "keywords" :[ "vdi-bestand", "vdi-bestandsformaat", "wat is een vdi-bestand", "bestand", "vdi-voorbeeld", "vdi-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over VDI-bestandsindeling en API's die VDI-bestanden kunnen maken en openen.",
  "title" :"VDI - VirtualBox virtueel schijfkopiebestand",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Wat is een VDI-bestand?
Een bestand met de extensie .vdi is een virtuele schijfkopie; specifiek voor het open source desktopvirtualisatieprogramma van Oracle, VirtualBox. De VDI-bestanden worden gebruikt om de virtuele VirtualBox-machine te starten. Met de VM's kunnen gebruikers extra besturingssystemen of programma's op één computer uitvoeren. Het voordeel van VDI-bestanden is dus dat gebruikers deze schijfkopiebestanden op hun harde schijf kunnen opslaan en deze kunnen uitvoeren met emulators wanneer ze maar willen.

## VDI-bestandsindeling
Virtual Disk Image (VDI) is de primaire schijfbestandsindeling voor een actief ontwikkelde, open-source Oracle VM, bekend als VirtualBox, een virtualisatieproduct van enterprise-klasse. Het VDI-bestandsformaat is ontworpen om een draagbare schijfkopie te maken die gemakkelijk kan worden uitgevoerd met andere virtualisatieprogramma's. Het ondersteunt zowel dynamisch toegewezen als opslag met een vaste grootte. Hiermee kunt u een afbeeldingsbestand uitbreiden nadat het is gemaakt, zelfs als het al gegevens bevat.

### Schijfvirtualisatie
Het systeem emuleert harde schijven in VDI-schijfkopieformaat. Een VirtualBox VM kan eerdere schijven gebruiken die zijn gemaakt in Microsoft Virtual PC of VMware, evenals zijn eigen native formaat. De VirtualBox is ook in staat om verbinding te maken met iSCSI-doelen en onbewerkte partities op de host, ofwel als virtuele harde schijven. VirtualBox emuleert IDE (PIIX4- en ICH6-controllers), SATA (ICH8M-controller), SAS-controllers waarop harde schijven kunnen worden aangesloten en SCSI.

De ondersteuning is beschikbaar voor Open Virtualization Format (OVF) sinds versie 2.2.0 van VirtualBox. Zowel op de host aangesloten fysieke apparaten als ISO-images kunnen worden gemount als cd- of dvd-stations.
Standaard ondersteunt VirtualBox grafische afbeeldingen via een VESA-compatibele aangepaste virtuele grafische kaart.

### Virtualisatie-ondersteuning voor Ethernet
VirtualBox virtualiseert de volgende netwerkinterfacekaarten voor een Ethernet-netwerkadapter:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Desktop (82540EM)
- Intel Pro/1000 MT-server (82545EM)
- Intel Pro/1000 T-server (82543GC)
- Geparavirtualiseerde netwerkadapter (virtio-net)

Dankzij de geëmuleerde netwerkkaarten kunnen gast-besturingssystemen worden uitgevoerd zonder dat u stuurprogramma's voor netwerkhardware hoeft te zoeken en installeren, aangezien deze beschikbaar zijn als onderdeel van het gast-besturingssysteem. Een speciale para-gevirtualiseerde netwerkadapter verbetert de netwerkprestaties door de noodzaak om een specifieke hardware-interface aan te passen, te verminderen. Daarom vereist het speciale chauffeursondersteuning in de gast.


## Referenties

* [VirtualBox - door Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


