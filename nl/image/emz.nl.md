{
  "date" : "2019-10-11",
  "keywords" :[ "emz-bestand", "emz-bestandsformaat", "wat is een emz-bestand", "bestand", "emz-voorbeeld", "emz-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMZ-bestandsindeling - een Windows-gecomprimeerd verbeterd metabestand",
  "description":"Meer informatie over EMZ-bestandsindelingen en API's die EMZ-bestanden kunnen maken en openen.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Wat is een EMZ-bestand?

Een bestand met de extensie .emz is een gecomprimeerde container van Enhanced Metafile ([EMF](/nl/image/emf/)-bestand). Deze worden gecomprimeerd met behulp van de [GZIP](/nl/compression/gz/)-compressietechniek, de meest gebruikte compressiemethode op UNIX- en LINUX-besturingssystemen. Ontkoppel ZIP (/nl/compression/zip/), GZIP comprimeert het archief als geheel in plaats van individuele bestanden te comprimeren. EMZ-bestanden zijn kleiner in vergelijking met de EMF-bestanden en helpen bij een snelle overdracht tijdens het online delen van bestanden. Enkele van de toepassingen die EMZ-bestanden kunnen openen, zijn Microsoft Visio 2019, Microsoft Office 2019, XnView MP en File Viewer Plus.

## EMZ-bestandsindeling

EMZ-bestanden zijn [Gzip](/nl/compression/gz/) gecomprimeerd en bevatten [EMF](/nl/image/emf/) binnenin. Gzip gebruikt het DEFLATE-algoritme voor compressie van het archief en is anders bij het toepassen van compressie. Een EMZ-bestand kan worden gedecomprimeerd met behulp van GZip-compressiehulpprogramma's zoals GNU Zip. Het bestandsformaat bestaat uit:

* Bestandskoptekst
* Optionele kopteksten
* Gecomprimeerde gegevens
* Bestandsvoettekst

Het GZIP-bestandsformaat [specificaties versie 4.3](https://datatracker.ietf.org/doc/html/rfc1952) gepubliceerd door Internet Engineering Task Force (IETF) bevat gedetailleerde informatie over het bestandsformaat.

## Referenties

* [RFC1952: GZIP-bestandsformaatspecificatie](https://datatracker.ietf.org/doc/html/rfc1952), door [IETF](https://www.ietf.org/)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

