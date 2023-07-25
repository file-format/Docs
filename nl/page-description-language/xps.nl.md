{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "XML-papierspecificaties", "Bestand", "Extensie", "Bestandsindeling", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Bestandsindeling pagina-indeling",
  "description":"Meer informatie over XPS-bestandsindelingen en API's die XPS-bestanden kunnen maken en openen.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Wat is een XPS-bestand? ##

Een XPS-bestand vertegenwoordigt paginalay-outbestanden die zijn gebaseerd op XML Paper-specificaties die zijn gemaakt door Microsoft. Het is ontwikkeld als vervanging van het EMF-bestandsformaat en is vergelijkbaar met het [PDF](/nl/pdf/)-bestandsformaat, maar gebruikt XML voor de lay-out, het uiterlijk en de afdrukinformatie van een document. Het is in feite meer gerechtvaardigd om te zeggen dat XPS een poging tot PDF is, maar om vele redenen niet genoeg populariteit kon krijgen als eigendom van PDF. Microsoft biedt vanaf Windows 7 standaard XPS Document Writer aan voor het maken van XPS-bestanden. XPS-bestanden kunnen worden gegenereerd door de "Microsoft XPS Document Writer" als printer te selecteren tijdens het afdrukken van het document.

XPS-viewers zijn geïntegreerd als onderdeel van Windows Vista, Windows 7, Windows 8 en Internet Explorer 6 of hoger. XPS-bestanden worden alleen-lezen zodra ze zijn gegenereerd. Dit draagt bij aan het vertrouwen van de gebruiker in ontvangen documenten die als XPS zijn verzonden voor de authenticiteit van het document. Een XPS-document kan een of meer pagina's bevatten zoals geconverteerd vanuit het originele document.

## Korte geschiedenis ##

Microsoft heeft de XPS-specificatie ingediend bij Ecma International. In juni 2007 is de Ecma Technical Committee 46 (TC46) opgericht om een standaard te ontwikkelen op basis van de OpenXPS Paper Specifications. Ecma International keurde de Ecma Standard (ECMA-388) [XPS-specificaties](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) goed in juni 2009 tijdens de 97e Algemene Vergadering.

## XPS-bestandsindeling ##

Het XPS-formaat bestaat uit XML-opmaak die de samenstelling van een document en het uiterlijk van elke pagina definieert, samen met weergaveregels voor het weergeven of afdrukken van het document. Het bewaart alle informatie om een document opnieuw te maken op elk systeem, waardoor het onafhankelijk is van de beschikbare bronnen op dat systeem. Het formaat is in wezen een ZIP-archief en als u de bestandsextensie hernoemt naar ZIP, ziet u de samenstellende bestanden die de documentgegevens bevatten. Deze documenten omvatten:

* documentpaginabestanden (.fpage) - Bevat documentinhoud en documentformaatinstellingen. Elke pagina in het XPS-document heeft één FPAGE-bestand.
* bestand met documentinstellingen (.fdoc) - Slaat instellingen op die zijn opgenomen in het XPS-archief.
* documentfragmentbestanden (.frag) - Definieert de instellingen voor het eigenlijke XPS-bestand en elke pagina in het document heeft zijn eigen .frag-bestand.

{{< figure src="../XPS-1.png" alt="XPS-bestandsindeling" >}}

Deze bestanden behouden de documentinhoud op zo'n manier dat als iemand bijvoorbeeld niet dezelfde lettertypen op zijn computer heeft geïnstalleerd, de XPS-viewer die originele lettertypen nog steeds zal weergeven. Dit impliceert de opname van een XML-opmaakbestand voor elk:

* Bladzijde
* Tekst
* Ingesloten lettertypen
* Rasterafbeeldingen
* 2D-vectorafbeeldingen
* Digitale Rechten Beheer

Het XPS-documentformaat bevat een goed gedefinieerde set onderdelen en relaties, die elk een bepaald doel in het document vervullen. Het formaat breidt ook de pakketfuncties uit, waaronder digitale handtekeningen, miniaturen en interleaving.

Een typisch XPS-document ziet er als volgt uit en kan worden geanalyseerd in het licht van het XPS-bestandsformaat [specificaties](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="XPS-bestandsindeling" >}}


## Referenties ##

* [Specificaties XPS-bestandsindeling](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - Door Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

