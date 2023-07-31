{
  "date" : "2019-10-11",
  "keywords" :[ "vstm-bestand", "vstm-bestandsindeling", "wat is een vstm-bestand", "bestand", "vstm-voorbeeld", "vstm-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Microsoft Visio-sjabloonbestandsindeling",
  "description":"Meer informatie over VSTM-bestandsindeling en API's die VSTM-bestanden kunnen maken en openen.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een VSTM-bestand?

Bestanden met de extensie VSTM zijn sjabloonbestanden die zijn gemaakt met Microsoft Visio en die macro's ondersteunen. In tegenstelling tot VSDX-bestanden kunnen bestanden die zijn gemaakt met VSTM-sjablonen macro's uitvoeren die zijn ontwikkeld in Visual Basic for Applications (VBA)-code. Er kan een sjabloonbestand worden gemaakt om basisinstellingen van het document te bieden die kunnen worden gebruikt om met deze instellingen verdere documenten te genereren. Visio-bestanden worden gebruikt om tekeningen te maken die visuele objecten, stroomdiagrammen, UML-diagrammen, informatiestromen, organigrammen, softwarediagrammen, netwerklay-out, databasemodellen, objecttoewijzing en andere soortgelijke informatie bevatten. Bestanden die zijn gegenereerd met Visio kunnen ook worden geëxporteerd naar verschillende bestandsindelingen zoals PNG, BMP, PDF en andere.

## Bestandsformaat ##

VSTM-bestanden zijn gebaseerd op de Open Packaging Conventions en XML en ontwikkelaars kunnen profiteren van dit formaat door programmatisch met deze bestanden te leren werken. De indeling erft veel van dezelfde XML-structuren als de onderdelen van de Visio XML Drawing-bestandsindeling (.vdx). De interoperabiliteit met Visio-bestanden is aanzienlijk verbeterd, aangezien software van derden Visio-bestanden op bestandsindelingsniveau kan manipuleren.

Elk Visio-bestand wordt een pakket genoemd dat andere bestanden of onderdelen bevat. Een pakketonderdeel kan een XML-bestand, een afbeelding of zelfs een VBA-oplossing zijn. De onderdelen binnen het pakket kunnen worden onderverdeeld in "document"- en "relatie"-gedeelten.

### Document ###

De documentonderdelen bevatten de feitelijke inhoud en metadata van het Visio-bestand, zoals de naam van het bestand, de eerste pagina en alle vormen die het bevat, en zelfs de gegevensverbindingen voor de vormen. Afbeeldingen en tekstbestanden in het pakket worden beschouwd als documentonderdelen.

### Verhoudingen ###

De relatiedelen van een Visio-bestand worden opgeslagen in de map "_rels" en beschrijven hoe de delen in het pakket aan elkaar gerelateerd zijn. Het geeft ook de structuur van het bestand. Een op zichzelf staand XML-document gebruikt de bovenliggende/onderliggende relatie van elementen om de relatie van entiteiten tot elkaar te bepalen. Een geldig Visio 2013-bestandsformaat bevat de juiste set onderdelen en het pakket bevat de relaties tussen de onderdelen.

Relatiedelen zijn XML-documenten die de relaties tussen verschillende documentdelen binnen het pakket beschrijven. Ze definiëren een associatie tussen twee items: een gespecificeerde bron (gedefinieerd door de naam en locatie van het relatiebestand) en een gespecificeerd doeldocumentonderdeel. Relatiedelen worden bijvoorbeeld gebruikt om te beschrijven welke vormmodellen aan het bestand zijn gekoppeld, hoe pagina's zich verhouden tot het bestand en tot elkaar, of hoe afbeeldingen en objecten zich verhouden tot een specifieke pagina.

## Referenties ##

* [Inleiding tot Visio-bestandsindeling](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

