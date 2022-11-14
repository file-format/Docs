{
  "date" : "2021-04-08",
  "keywords" :[ "rpm-bestand", "rpm-bestandsindeling", "wat is een rpm-bestand", "bestand", "rpm-voorbeeld", "rpm-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Red Hat Package Manager-bestand",
  "description":"Meer informatie over RPM-bestandsindeling en API's die RPM-bestanden kunnen maken en openen.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Wat is een RPM-bestand?

Een bestand met de extensie .rpm is een Red Hat Linux-besturingssysteempakket voor installaties van programma's op Linux-systemen. De Red Hat Package Manager gebruikt het RPM-bestandsformaat en is een gratis en open-source pakketbeheersysteem. Hoewel RPM-bestanden als zodanig kunnen worden gebruikt voor de installatie van programma's, kunnen deze worden geconverteerd naar andere pakketindelingen zoals [DEB](/nl/compression/deb/) met behulp van het Debian-programma Alien.

## RPM-bestandsindeling

Een RPM-bestand is een binair bestand dat een reeks bestanden kan bevatten. Meestal zijn RPM-bestanden "binaire RPM's", de gecompileerde uitvoerbare bestanden van de software. Het RPM-bestand kan bron-RPM's (SRPM's) bevatten die kunnen worden gebruikt om het pakket op basis van de broncode te bouwen. Het RPM-bestandsformaat bestaat uit vier secties.

* Lead - Het identificeert het bestand als een RPM-bestand
* Handtekening - Het kan worden gebruikt om de integriteit en/of authenticiteit te waarborgen
* Header - Bevat metadata inclusief pakketnaam, versie, architectuur, bestandslijst, etc.
* Bestandsarchief - Ook bekend als payload, meestal in cpio-formaat, gecomprimeerd met [GZIP](/nl/compression/gz/)

## Referenties

* [RPM - Wikipedia](https://rpm.org)
* [RPM-documentatie](https://rpm.org/documentation.html)

