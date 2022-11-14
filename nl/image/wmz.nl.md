{
  "date" : "2019-10-11",
  "keywords" :[ "wmz-bestand", "wmz-bestandsformaat", "wat is een wmz-bestand", "bestand", "wmz-voorbeeld", "wmz-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMZ-bestandsindeling - gecomprimeerd Windows-metabestand",
  "description":"Meer informatie over WMZ-bestandsindelingen en API's die WMZ-bestanden kunnen maken en openen.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Wat is een WMZ-bestand?

Een bestand met de extensie .wmz is een gecomprimeerde versie van [WMF](/nl/image/wmf/) en wordt gebruikt om metabestanden op te slaan. Het is een bestand op gemiddeld niveau dat wordt gegenereerd door oudere versies van Microsoft Office-toepassingen en wordt niet erg populair gebruikt. WMZ-bestanden worden gegenereerd tijdens het opslaan van documenten in de [HTML](/nl/web/html/)-indeling. Deze kunnen ook worden gegenereerd tijdens het e-mailen van documenten die ingebedde illustraties, vergelijkingen, enz. bevatten. Toepassingen die WMZ-bestanden kunnen openen, zijn onder meer (maar niet beperkt tot) Corel Winzip en Apple Archive Utility.

## WMZ-bestandsindeling

WMZ-bestanden zijn [Gzip](/nl/compression/gz/) gecomprimeerd en bevatten [WMF](/nl/image/WMF/) binnenin. Gzip gebruikt het DEFLATE-algoritme voor het comprimeren van het archief. GZIP verschilt van het [ZIP](/nl/compression/zip/) archiefformaat omdat het een compressie-algoritme toepast op het volledige archief in plaats van op de individuele bestanden. Het bestandsformaat bestaat uit:

* Bestandskoptekst
* Optionele kopteksten
* Gecomprimeerde gegevens
* Bestandsvoettekst

Het GZIP-bestandsformaat [specificaties versie 4.3](http://tools.ietf.org/html/rfc1952) gepubliceerd door Internet Engineering Task Force (IETF) bevat gedetailleerde informatie over het bestandsformaat.

## Referenties

* [RFC1952: GZIP-bestandsformaatspecificatie](http://tools.ietf.org/html/rfc1952), door [IETF](https://ietf.org)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

