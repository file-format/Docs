{
  "date" : "2019-10-11",
  "keywords" :[ "vstx-bestand", "vstx-bestandsindeling", "wat is een vstx-bestand", "bestand", "vstx-voorbeeld", "vstx-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - Microsoft Visio-bestandsindeling",
  "description":"Meer informatie over de VSTX-bestandsindeling en API's die VSTX-bestanden kunnen maken en openen.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een VSTX-bestand?

Bestanden met de extensie .vstx zijn tekeningsjabloonbestanden die zijn gemaakt met Microsoft Visio 2013 en hoger. Deze VSTX-bestanden bieden een startpunt voor het maken van Visio-tekeningen, opgeslagen als [.VSDX](/nl/image/vsdx/)-bestanden, met standaardlay-out en instellingen. Over het algemeen worden Visio-bestanden gebruikt om tekeningen te maken die visuele objecten, stroomdiagrammen, UML-diagrammen, informatiestromen, organigrammen, softwarediagrammen, netwerklay-out, databasemodellen, objecttoewijzing en andere soortgelijke informatie bevatten. Bestanden die zijn gegenereerd met Visio kunnen ook worden geëxporteerd naar verschillende bestandsindelingen zoals [PNG](/nl/Image/PNG/), [BMP](/nl/Image/BMP/), [PDF](/nl/pdf/) en andere. Programma's die VSTX-bestanden openen, zijn onder meer Microsoft Visio voor Windows en Mac waarmee u deze bestanden kunt openen om ze te bekijken en te bewerken. Het maakt het ook mogelijk om Visio-bestandsindelingen naar een aantal andere indelingen te converteren.

# VSTX-bestandsindeling #

De "X" in de bestandsextensie verwijst naar de OpenOffice-bestandsindeling die door Microsoft werd geïntroduceerd als een [ZIP](/nl/compression/zip/) archiefbestandsindeling ter vervanging van eerder ondersteunde binaire bestandsindelingen. VSTX-bestanden zijn dus gebaseerd op het XML-bestandsformaat van OpenOffice-specificaties, in tegenstelling tot het [.VST](/nl/image/vst/) bestandsformaat dat in binair formaat is.

VSDX-bestanden zijn gebaseerd op de Open Packaging Conventions en XML en ontwikkelaars kunnen profiteren van dit formaat door programmatisch met deze bestanden te leren werken. De indeling erft veel van dezelfde XML-structuren als de onderdelen van de Visio XML Drawing-bestandsindeling (.vdx). De interoperabiliteit met Visio-bestanden is aanzienlijk verbeterd, aangezien software van derden Visio-bestanden op bestandsindelingsniveau kan manipuleren.

Bepaalde andere bestandstypen die deel uitmaken van de Visio 2013-bestandsindeling zijn onder meer:

* .vsdm (Visio macro-enabled tekening)
* .vssx (Visio-stencil)
* .vssm (Visio macro-enabled stencil)
* .vstx (Visio-sjabloon)
* .vstm (Macro-enabled Visio-sjabloon)

Onder de motorkap gebruikt het Visio 2013-bestandsformaat een gestructureerde manier om applicatiegegevens samen met gerelateerde bronnen op te slaan in een archief zoals [ZIP](/nl/compression/zip/). Het ZIP-bestand kan worden uitgepakt met behulp van elk standaard extractiehulpprogramma waar het ook andere soorten bestanden bevat. U kunt gewoon de .VSTX-bestandsextensie vervangen door .ZIP in Windows Explore om de inhoud in het VSTX-bestand te zien.

Elk Visio-bestand wordt een pakket genoemd dat andere bestanden of onderdelen bevat. Een pakketonderdeel kan een XML-bestand, een afbeelding of zelfs een VBA-oplossing zijn. De onderdelen binnen het pakket kunnen worden onderverdeeld in "document"- en "relatie"-gedeelten.

### Document ###

De documentonderdelen bevatten de feitelijke inhoud en metadata van het Visio-bestand, zoals de naam van het bestand, de eerste pagina en alle vormen die het bevat, en zelfs de gegevensverbindingen voor de vormen. Afbeeldingen en tekstbestanden in het pakket worden beschouwd als documentonderdelen.

### Verhoudingen ###

De relatiedelen van een Visio-bestand worden opgeslagen in de map "_rels" en beschrijven hoe de delen in het pakket aan elkaar gerelateerd zijn. Het geeft ook de structuur van het bestand. Een op zichzelf staand XML-document gebruikt de bovenliggende/onderliggende relatie van elementen om de relatie van entiteiten tot elkaar te bepalen. Een geldig Visio 2013-bestandsformaat bevat de juiste set onderdelen en het pakket bevat de relaties tussen de onderdelen.

Relatiedelen zijn XML-documenten die de relaties tussen verschillende documentdelen binnen het pakket beschrijven. Ze definiëren een associatie tussen twee items: een gespecificeerde bron (gedefinieerd door de naam en locatie van het relatiebestand) en een gespecificeerd doeldocumentonderdeel. Relatiedelen worden bijvoorbeeld gebruikt om te beschrijven welke vormmodellen aan het bestand zijn gekoppeld, hoe pagina's zich verhouden tot het bestand en tot elkaar, of hoe afbeeldingen en objecten zich verhouden tot een specifieke pagina.

## Referenties ##

* [Inleiding tot Visio-bestandsindeling](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

