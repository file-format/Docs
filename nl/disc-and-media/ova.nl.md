{
  "date" : "2021-08-10",
  "keywords" :[ ".ova-bestand", "bestandsindeling", "wat is een .ova-bestand", "bestand", "bestandsextensie"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over wat een .ova-bestandsindeling is en API's die ova-bestanden kunnen maken en openen.",
  "title" :"OVA-bestandsindeling - Open Virtual Appliance-bestand",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Wat is een OVA-bestand?

Een OVA-bestand (Open Virtual Appliance) is een OVF-directory die is opgeslagen als een archief met behulp van de .tar-archiveringsindeling. Het is een pakketbestand voor virtuele apparaten dat bestanden bevat voor de distributie van software die op een virtuele machine draait. Een OVA-pakket bevat een [.ovf](/nl/disc-and-media/ovf/) descriptorbestand, certificaatbestanden, een optioneel [.mf](/nl/programming/mf/)-bestand samen met andere gerelateerde bestanden. OVA-bestanden hebben het mediatype als applicatie/ovf.

## OVA-bestandsindeling

Zoals vermeld, is een OVA-bestand een archiefbestand dat is gemaakt met behulp van de OVF-directory in TAR-bestandsindeling. Het bestand zelf wordt opgeslagen als een binair bestand. De meeste virtualisatieplatforms, zoals VMware, Microsoft, Oracle en Citrix, kunnen virtuele apparaten installeren vanuit een OVF-bestand dat een descriptorbestand is met de details van de afbeelding die in de virtuele machine moet worden geladen.

## Voordelen van een OVA-bestand

* OVA-bestanden zijn gecomprimeerd, waardoor snellere downloads mogelijk zijn.
* De vSphere Client valideert een OVA-bestand voordat het wordt geïmporteerd en zorgt ervoor dat het compatibel is met de beoogde doelserver. Als het apparaat niet compatibel is met de geselecteerde host, kan het niet worden geïmporteerd en verschijnt er een foutmelding.
* OVA kan toepassingen met meerdere lagen en meer dan één virtuele machine inkapselen.

## Referenties

* [OVA-bestandsindelingen en sjablonen](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [OVF-bestandsformaatspecificaties](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualisatie-format-specification-dsp0243_1-1-0.pdf)

