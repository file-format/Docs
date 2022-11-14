{
  "date" : "2021-08-10",
  "keywords" :[ ".ovf-bestand", "bestandsindeling", "wat is een .ovf-bestand", "bestand", "bestandsextensie"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over wat een .ovf-bestandsindeling is en API's die OVF-bestanden kunnen maken en openen.",
  "title" :"OVF-bestandsindeling - Open virtualisatiebestand",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Wat is een OVF-bestand?

Een OVF-bestand is een tekstbestand dat informatie bevat over de verpakking en distributie van software die op een virtuele machine draait. Het is geformatteerd volgens de [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) die alle vereisten beschrijft (zoals beveiliging, draagbaarheid, efficiëntie en uitbreidbaarheid) voor het draaien van applicaties op virtuele machines. De International Organization for Standardization (ISO) heeft OVF aangenomen als ISO 17203-standaard.

## Korte geschiedenis van het OVF-bestandsformaat

Het OVF-bestandsformaat is geïntroduceerd door DMTF (Distributed Management Task Force) dat open beheersstandaarden creëert. Het is onafhankelijk van een bepaalde hypervisor- of instructiesetarchitectuur. Het OVF-pakket bevat een of meer virtuele systemen, die elk op een virtuele machine kunnen worden geïmplementeerd.

## OVF-bestandsindeling - Meer informatie

Een OVF-pakket bestaat uit meerdere bestanden die in een enkele map zijn geplaatst. Hiervan bevat het precies één OVF-descriptorbestand (met extensie .ovf) dat is opgeslagen in de bestandsindeling [XML](/nl/web/xml/). Het beschrijft de verpakte virtuele machine-informatie en metadata-informatie over het OVF-pakket, zoals:

* naam
* hardwarevereisten
* verwijzingen naar de andere bestanden in het OVF-pakket, en
* door mensen leesbare beschrijvingen

Andere bestanden die in een OVF-pakket kunnen worden gevonden, zijn een of meer schijfkopieën en optioneel certificaatbestanden en andere hulpbestanden.

## Referenties

* [Open virtualisatie-indeling - DMTF](https://www.dmtf.org/standards/ovf)
* [OVF-bestandsformaatspecificaties](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

