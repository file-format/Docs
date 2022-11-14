{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/VT-bestandsindeling",
  "description":"Meer informatie over PDF/VT-bestandsindelingen en API's die PDF/VT-bestanden kunnen maken en openen.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Wat is PDF/VT? #

PDF/VT, gepubliceerd als [ISO 16612-2](https://www.iso.org/standard/46428.html) in augustus 2010 als standaard, is ontworpen om het afdrukken van variabele documenten (VDP) in verschillende omgevingen. De standaard maakt Variabele informatie en Transactioneel printen als basis voor de standaard. Het afdrukken van variabele gegevens wordt gebruikt wanneer een deel van de informatie voor elke ontvanger van de inhoud anders is. Het transactioneel printen omvat facturen, overzichten en andere documenten die factureringsinformatie combineren met marketinginformatie. Dit resulteert in een mix van verbeterde verwerking van afbeeldingen, tekst en andere soorten inhoud. PDF/VT maakt betrouwbaar en dynamisch beheer van pagina's voor High Volume Transactional Output (HVTO)-afdrukgegevens mogelijk door gebruik te maken van het concept met metagegevens van documentonderdelen (DPM). PDF/VT-bestanden kunnen worden geopend in Adobe Acrobat-viewer zonder dat u een ander onderdeel hoeft toe te voegen.

## Documentonderdeel hiërarchie ##

De documentonderdeel (DPart) hiërarchie is als een boomstructuur van documentonderdeelknooppunten die is gebaseerd op alle pagina's in het document. De elementen van deze boom worden DPart-knooppunten genoemd. Elk intern knooppunt bevat andere DPart-knooppunten en elk bladknooppunt specificeert een of meer pagina's voor een ontvanger. In wezen specificeert de DPart-hiërarchie de volgorde en relatie van documenten of klopjes van documenten in een PDF/VT-bestand. De boomstructuur van DPart-knooppunten geeft gemakkelijk de interne inhoud van een PDF/VT-document weer, omdat het subdocumenten voor veel ontvangers kan bevatten en elk documentdeel overeenkomt met de pagina's voor een enkele ontvanger. De DPart-hiërarchie is vereist in PDF/VT-bestanden.

## Metadata documentonderdelen (DPM) ##

De documentonderdeelmetagegevens (DPM) zijn gekoppeld aan elk knooppunt in de documentonderdeelhiërarchie en kunnen worden gebruikt om informatie over het subdocument van een bepaalde ontvanger en zijn onderdelen te communiceren. In het bijzonder kan de DPM informatie over de eigenschappen of informatie over de ontvangers in gecodeerde vorm bevatten.

## Conformiteitsniveaus ##

PDF/VT wordt toegekend op de volgende drie conformiteitsniveaus. Deze zijn allemaal gebaseerd op [PDF](/nl/pdf/) 1.6.

* `PDF/VT-1` - Het is gebaseerd op PDF/X-4 en bevat alle bronnen die nodig zijn voor het weergeven van een PDF-document.
* `PDF/VT-2` - Ontworpen voor uitwisseling van meerdere bestanden, PDF/VT-2-documenten kunnen verwijzen naar externe uitvoerintenties, externe inhoud of beide. Een PDF/VT-document en alle PDF-bestanden waarnaar wordt verwezen en externe uitvoerintenties worden gezamenlijk een PDF/VT-2-bestandenset genoemd. Acrobat 9 en ondersteunt deze functie.
* `PDF/VT-2s` - Ondersteunt PDF/VT-2 live streaming. Hierdoor kunnen gesegmenteerde delen van gegevens worden verwerkt.

## Referenties ##

* [PDF/VT - Door Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 grafische technologie](https://www.iso.org/standard/46428.html)

