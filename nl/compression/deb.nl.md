{
  "date" : "2021-04-08",
  "keywords" :[ "deb-bestand", "deb-bestandsindeling", "wat is een deb-bestand", "bestand", "deb-voorbeeld", "deb-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip gecomprimeerd teerarchief",
  "description":"Meer informatie over DEB-bestandsindeling en API's die DEB-bestanden kunnen maken en openen.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Wat is een DEB-bestand?

Een bestand met de extensie .deb is een binair pakketbestandsformaat van Debian dat beschikbaar is voor distributie van softwarepakketten op Linux OS. Het bestaat uit twee [TAR](/nl/compression/tar/) archiefbestanden. De DPKG biedt het mechanisme om de DEB-pakketten te lezen en te installeren. DEB-pakketten kunnen worden geïnstalleerd met behulp van de APT-pakketsoftwarebeheerinterface. DEB-bestanden hebben Internet Media Type als `application/vnd.debian.binary-package`.

## DEB-bestandsindeling

Een DEB-bestand bestaat uit twee [TAR](/nl/compression/tar/) archiefbestanden. Het ene archief bevat de besturingsinformatie en het andere bevat de installeerbare gegevens.

### Pakketorganisatie

Het DEB-bestand is een **ar** archiefbestand met de magische waarde `!<arch> `. Sinds Debian 0.93 bevat het archiveringsmechanisme van DEB-bestanden drie bestanden in een specifieke volgorde.

1. `Debian Binary` - Het is voorbestemd om een reeks regels te hebben, gescheiden door nieuwe regels. Op dit moment is er slechts één regel aanwezig die het versienummer beschrijft. Het huidige versienummer is 2.0.
1. `Control Archive` - Het bevat een control.tar-archief met onderhoudsscripts en meta-informatie over het pakket, zoals pakketnaam, versie, afhankelijkheden en onderhouder.
1. `Data Archive` - Het is een tar-archief met de naam data.tar en bevat de daadwerkelijk installeerbare mediabestanden. Het archief kan worden gecomprimeerd met gz, bz2, lzma of xz en de bestandsextensie van het gegevensarchief verandert dienovereenkomstig.

### Beheerarchief

Het controlearchief kan de volgende inhoud bevatten.

* `control` - Het bevat een korte beschrijving van het pakket en andere informatie zoals de afhankelijkheden.
* `md5sums` - Het bevat MD5-controlesommen van alle bestanden in het pakket om corrupte of onvolledige bestanden te detecteren.
* `conffiles` - Het geeft de bestanden van het pakket weer die als configuratiebestanden moeten worden behandeld. Configuratiebestanden worden tijdens een update niet overschreven, tenzij anders aangegeven.
* `preinst`, postinst, prerm en postrm - Optionele scripts die worden uitgevoerd voor of na het installeren of verwijderen van het pakket
* `config` is een optioneel script dat het debconf-configuratiemechanisme ondersteunt.
* `shlibs` - Het is een lijst met afhankelijkheden van gedeelde bibliotheken.

## Referenties

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Debian binaire pakketindeling](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

