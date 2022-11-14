{
  "date" : "2019-10-11",
  "keywords" :[ "vsdx-bestand", "vsdx-bestandsformaat", "wat is een vsdx-bestand", "bestand", "vsdx-voorbeeld", "vsdx-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Meer informatie over VSDX-bestandsindelingen en API's die VSDX-bestanden kunnen maken en openen.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een VSDX-bestand?

Bestanden met de extensie .vsdx vertegenwoordigen de Microsoft Visio-bestandsindeling die is geïntroduceerd vanaf Microsoft Office 2013. Het is ontwikkeld om het binaire bestandsformaat [.VSD](/nl/image/vsd/) te vervangen, dat wordt ondersteund door eerdere versies van Microsoft Visio. Het wordt ook ondersteund op Visio Services in Microsoft SharePoint Server 2013 en vereist geen tussenliggende bestandsindeling voor publicatie naar SharePoint Server. Visio-bestanden worden gebruikt om tekeningen te maken die visuele objecten, stroomdiagrammen, UML-diagrammen, informatiestromen, organigrammen, softwarediagrammen, netwerklay-out, databasemodellen, objecttoewijzing en andere soortgelijke informatie bevatten. Bestanden die zijn gegenereerd met Visio kunnen ook worden geëxporteerd naar verschillende bestandsindelingen zoals [PNG](/nl/image/png/), [BMP](/nl/image/bmp/), [PDF](/nl/pdf/) en andere.

## Bestandsformaat ##

VSDX-bestanden zijn gebaseerd op de Open Packaging Conventions en XML en ontwikkelaars kunnen profiteren van dit formaat door programmatisch met deze bestanden te leren werken. De indeling erft veel van dezelfde XML-structuren als de onderdelen van de Visio XML Drawing-bestandsindeling (.vdx). De interoperabiliteit met Visio-bestanden is aanzienlijk verbeterd, aangezien software van derden Visio-bestanden op bestandsindelingsniveau kan manipuleren.

Bepaalde andere bestandstypen die deel uitmaken van de Visio 2013-bestandsindeling zijn onder meer:

* .vsdm (Visio macro-enabled tekening)
* .vssx (Visio-stencil)
* .vssm (Visio macro-enabled stencil)
* .vstx (Visio-sjabloon)
* .vstm (Macro-enabled Visio-sjabloon)

Onder de motorkap gebruikt het Visio 2013-bestandsformaat een gestructureerd middel om applicatiegegevens samen met gerelateerde bronnen op te slaan in een archief zoals [ZIP](/nl/compression/zip/). Het ZIP-bestand kan worden uitgepakt met behulp van elk standaard extractiehulpprogramma waar het ook andere soorten bestanden bevat. U kunt gewoon de .vsdx-bestandsextensie vervangen door .zip in Windows Explore om de inhoud in het VSDX-bestand te zien.

Elk Visio-bestand wordt een pakket genoemd dat andere bestanden of onderdelen bevat. Een pakketonderdeel kan een XML-bestand, een afbeelding of zelfs een VBA-oplossing zijn. De onderdelen binnen het pakket kunnen worden onderverdeeld in "document"- en "relatie"-gedeelten.

### Document ###

De documentonderdelen bevatten de feitelijke inhoud en metadata van het Visio-bestand, zoals de naam van het bestand, de eerste pagina en alle vormen die het bevat, en zelfs de gegevensverbindingen voor de vormen. Afbeeldingen en tekstbestanden in het pakket worden beschouwd als documentonderdelen.

### Verhoudingen ###

De relatiedelen van een Visio-bestand worden opgeslagen in de map "\_rels" en beschrijven hoe de delen in het pakket aan elkaar gerelateerd zijn. Het geeft ook de structuur van het bestand. Een op zichzelf staand XML-document gebruikt de bovenliggende/onderliggende relatie van elementen om de relatie van entiteiten tot elkaar te bepalen. Een geldig Visio 2013-bestandsformaat bevat de juiste set onderdelen en het pakket bevat de relaties tussen de onderdelen.

Relatiedelen zijn XML-documenten die de relaties tussen verschillende documentdelen binnen het pakket beschrijven. Ze definiëren een associatie tussen twee items: een gespecificeerde bron (gedefinieerd door de naam en locatie van het relatiebestand) en een gespecificeerd doeldocumentonderdeel. Relatiedelen worden bijvoorbeeld gebruikt om te beschrijven welke vormmodellen aan het bestand zijn gekoppeld, hoe pagina's zich verhouden tot het bestand en tot elkaar, of hoe afbeeldingen en objecten zich verhouden tot een specifieke pagina.

## Referenties ##

* [Inleiding tot Visio-bestandsindeling](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

