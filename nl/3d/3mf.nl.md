{
  "date" : "2019-12-09",
  "keywords" :[ "3mf-bestand", "3mf-bestandsformaat", "wat is een 3mf-bestand", "bestand", "3mf-voorbeeld", "3mf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Meer informatie over 3MF-bestandsindelingen en API's die 3MF-bestanden kunnen openen en maken.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Wat is een 3MF-bestand?

3MF, 3D Manufacturing Format, wordt door toepassingen gebruikt om 3D-objectmodellen weer te geven voor een groot aantal andere toepassingen, platforms, services en printers. Het is gebouwd om de beperkingen en problemen in andere 3D-bestandsindelingen, zoals [STL](/nl/cad/stl/), te vermijden voor het werken met de nieuwste versies van 3D-printers. 3MF is een relatief nieuw bestandsformaat dat is ontwikkeld en gepubliceerd door het 3MF-consortium. Het is rijk genoeg om een model volledig te beschrijven, met behoud van interne informatie, kleur en andere kenmerken die het uitbreidbaar maken voor het ondersteunen van nieuwe innovaties in 3D-printen. Het formaat is uitbreidbaar, breed toepasbaar en vrij van problemen met andere veelgebruikte bestandsformaten.

## Korte geschiedenis van het 3MF-bestandsformaat

De bestaande beperkingen in beschikbare modelbeschrijvende bestandsindelingen, zoals STL en andere, leiden ertoe dat de toonaangevende merken samenkomen en een meer uitbreidbaar bestandsformaat voor 3D-printen formuleren. Een belangrijke overweging was hoe applicaties modelgegevens moesten doorgeven aan 3D-printers. Het 3MF-consortium is daarom ontstaan om een nieuw 3D-bestandsformaat, 3MF genaamd, te ondersteunen met als doel het uitbreidbaar genoeg te maken om aan de behoeften van 3D-printen te voldoen. Verschillende bedrijven maakten deel uit van dit consortium, waaronder Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP en anderen. Microsoft schonk zijn 3D-bestandsformaat work-in-progress als uitgangspunt voor de gezamenlijke verdere ontwikkeling van de specificatie door het 3MF Consortium.

## 3MF-bestandsindeling - Meer informatie

3MF is een op XML gebaseerd gegevensformaat - door mensen leesbare gecomprimeerde XML - dat definities bevat voor gegevens met betrekking tot 3D-productie, inclusief uitbreidbaarheid door derden voor aangepaste gegevens. Het 3MF-bestandsformaat is ontworpen rekening houdend met de beperkingen en problemen waarmee andere 3D-bestandsindelingen worden geconfronteerd. Dit leidde tot de formulering van het 3MF-bestandsformaat dat is:

* **Compleet:** Bevat alle benodigde model-, materiaal- en eigendomsinformatie in één archief
* **Voor mensen leesbaar:** Gebruik van veelgebruikte structuren zoals OPC, [ZIP](/nl/compression/zip/) en XML om de ontwikkeling te vergemakkelijken
* **Eenvoudig:** Een korte, duidelijke specificatie, waardoor de ontwikkeling eenvoudig en de validatie snel verloopt
* **Uitbreidbaar:** Door gebruik te maken van XML-naamruimten zijn zowel openbare als privé-extensies mogelijk met behoud van compatibiliteit
* **Ondubbelzinnig:** Duidelijke taal- en conformiteitstests zorgen ervoor dat een bestand altijd consistent is, van digitaal tot fysiek
* **Gratis:** Toegang tot en implementatie van de 3MF-specificatie is en zal altijd vrij zijn van royalty's, patenten en licenties

De specificaties voor het 3MF-bestandsformaat worden gehost via [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) voor openbare toegang en continue updates. De huidige gepubliceerde versie is 1.2.3 die de reeks conventies beschrijft voor het gebruik van XML en andere algemeen beschikbare technologieën om de inhoud en het uiterlijk van een of meer 3D-modellen te beschrijven. Ontwikkelaars die systemen willen bouwen voor het verwerken van 3MF-bestandsindelingen, kunnen deze specificaties raadplegen voor implementatiedoeleinden.

## Specificaties 3MF-bestandsindeling

Het 3MF-bestandsformaat gebruikt de Open Packaging-specificaties in de vorm van een ZIP-archief voor het fysieke model. Het bevat een goed gedefinieerde set onderdelen en relaties die een bepaald doel in het document vervullen. Dit zorgt er ook voor dat het formaat de pakketfunctie volgt, inclusief digitale handtekeningen en miniaturen.

### Het 3MF-document - een overzicht

Een typisch 3MF-document ziet er als volgt uit:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

De payload omvat de volledige set onderdelen die nodig zijn voor het verwerken van het 3D-modelonderdeel. Alle inhoud die moet worden gebruikt om een object te vervaardigen dat wordt beschreven in de 3D-payload, MOET in het 3MF-document zijn opgenomen. De beschrijving van elk documentonderdeel samen met de status zoals vereist of optie is zoals gegeven in de volgende tabel.


|**Naam**|**Beschrijving**|**Relatiebron**|**Vereist/optioneel**
--- | --- | --- | ---
|3D-model|Bevat de beschrijving van een of meer 3D-objecten voor fabricage.|Pakket|VERPLICHT
|Kerneigenschappen|Het OPC-gedeelte dat verschillende documenteigenschappen bevat.|Pakket|OPTIONEEL
| Oorsprong digitale handtekening|Het OPC-gedeelte dat de basis vormt van digitale handtekeningen in het pakket.|Pakket|OPTIONEEL
|Digitale handtekening|OPC-delen die elk een digitale handtekening bevatten.|Oorsprong digitale handtekening|OPTIONEEL
|Digitale handtekeningcertificaat|OPC-onderdelen die een certificaat voor digitale handtekening bevatten.|Digitale handtekening|OPTIONEEL
|PrintTicket|Biedt instellingen die moeten worden gebruikt bij het uitvoeren van het (de) 3D-object(en) in het 3D-modelgedeelte.|3D-model|OPTIONEEL
|Thumbnail|Bevat een kleine JPEG- of PNG-afbeelding die de 3D-objecten in het pakket of het pakket als geheel vertegenwoordigt.|Pakket|OPTIONEEL
|3D-textuur|Bevat een textuur die wordt gebruikt om kleur toe te passen op een 3D-object in het 3D-modelgedeelte (beschikbaar voor uitbreidingen)|3D-model|OPTIONEEL
|Aangepaste onderdelen|OPC-onderdelen die zijn gekoppeld aan metadata|Pakket|OPTIONEEL

De [Onderdelen en relaties](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D-modellen](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Objectbronnen](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) en [Pakketkenmerken](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) secties van specificaties document geeft gedetailleerde informatie over het 3MF-document.

## Referenties ##

* [Specificaties voor 3MF-bestandsindelingen](https://github.com/3MFConsortium/spec_core)
* [3MF - Door Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

