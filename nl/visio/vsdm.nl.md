{
  "date" : "2019-10-11",
  "keywords" :[ "vsdm-bestand", "vsdm-bestandsformaat", "wat is een vsdm-bestand", "bestand", "vsdm-voorbeeld", "vsdm-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Microsoft Visio-bestandsindeling voor tekeningen",
  "description":"Meer informatie over VSDM-bestandsindeling en API's die VSDM-bestanden kunnen maken en openen.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een VSDM-bestand?

Bestanden met de extensie .vsdm zijn tekenbestanden die zijn gemaakt met de Microsoft Visio-toepassing die macro's ondersteunt. VSDM-bestanden zijn OPC/XML-tekeningen die vergelijkbaar zijn met VSDX, maar die ook de mogelijkheid bieden om macro's uit te voeren wanneer het bestand wordt geopend. Macro's zijn door de gebruiker gedefinieerde acties/stappen die zijn ontwikkeld in Visual Basic for Applications (VBA) en kunnen worden gebruikt om repetitieve taken uit te voeren. Het VSDM-bestandsformaat werd geïntroduceerd met de lancering van Microsoft Visio 2013. Visio-bestanden worden gebruikt om tekeningen te maken die visuele objecten, stroomdiagrammen, UML-diagrammen, informatiestroom, organigrammen, softwarediagrammen, netwerklay-out, databasemodellen, objecttoewijzing en andere bevatten. vergelijkbare informatie. Bestanden die zijn gegenereerd met Visio kunnen ook worden geëxporteerd naar verschillende bestandsindelingen zoals [PNG](/nl/image/png/), [BMP](/nl/image/bmp/), [PDF](/nl/pdf/) en andere.

## VSDM-bestandsindeling

VSDM-bestanden zijn gebaseerd op de Open Packaging Conventions en XML en ontwikkelaars kunnen van dit formaat profiteren door programmatisch met deze bestanden te leren werken. De indeling erft veel van dezelfde XML-structuren als de onderdelen van de Visio XML Drawing-bestandsindeling (.vdx). De interoperabiliteit met Visio-bestanden is aanzienlijk verbeterd, aangezien software van derden Visio-bestanden op bestandsindelingsniveau kan manipuleren.

Elk Visio-bestand wordt een pakket genoemd dat andere bestanden of onderdelen bevat. Een pakketonderdeel kan een XML-bestand, een afbeelding of zelfs een VBA-oplossing zijn. De onderdelen binnen het pakket kunnen worden onderverdeeld in "document"- en "relatie"-gedeelten.

### Document ###

De documentonderdelen bevatten de feitelijke inhoud en metadata van het Visio-bestand, zoals de naam van het bestand, de eerste pagina en alle vormen die het bevat, en zelfs de gegevensverbindingen voor de vormen. Afbeeldingen en tekstbestanden in het pakket worden beschouwd als documentonderdelen.

### Verhoudingen ###

De relatiedelen van een Visio-bestand worden opgeslagen in de map "\_rels" en beschrijven hoe de delen in het pakket aan elkaar gerelateerd zijn. Het geeft ook de structuur van het bestand. Een op zichzelf staand XML-document gebruikt de bovenliggende/onderliggende relatie van elementen om de relatie van entiteiten tot elkaar te bepalen. Een geldig Visio 2013-bestandsformaat bevat de juiste set onderdelen en het pakket bevat de relaties tussen de onderdelen.

Relatiedelen zijn XML-documenten die de relaties tussen verschillende documentdelen binnen het pakket beschrijven. Ze definiëren een associatie tussen twee items: een gespecificeerde bron (gedefinieerd door de naam en locatie van het relatiebestand) en een gespecificeerd doeldocumentonderdeel. Relatiedelen worden bijvoorbeeld gebruikt om te beschrijven welke vormmodellen aan het bestand zijn gekoppeld, hoe pagina's zich verhouden tot het bestand en tot elkaar, of hoe afbeeldingen en objecten zich verhouden tot een specifieke pagina.

## Referenties ##

* [Inleiding tot Visio-bestandsindeling](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

