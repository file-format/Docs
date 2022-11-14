{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "XSL Formatting Objects", "File", "Extension", "File Format", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Meer informatie over XSLFO-bestandsindeling en API's die XSLFO-bestanden kunnen maken en openen.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Wat is een XSL-FO-bestand? ##

XSL-FO (XSL Formatting Objects) is een krachtige stylesheettaal voor het opmaken van XML-documenten. De semantiek van de begrensde vorm van papier en drukwerk wordt uitgedrukt door XSL-FO wanneer de afmetingen vast zijn. In tegenstelling tot HTML, dat de semantiek van de onbegrensde vorm van een browservenster met variabele afmetingen weergeeft. De XML-documenten die door XSL-FO zijn opgemaakt, worden meestal gebruikt om PDF-bestanden te genereren. XSL (Extensible Stylesheet Language) is een set van feature-complete W3C-technologieën die bedoeld zijn om te ontwerpen voor het formatteren en uitwisselen van XML-documenten en XSL-FO als onderdeel van deze taal. XSLT en XPath zijn ook andere onderdelen van XSL.

Er wordt voorgesteld om XML-documenten eerst om te zetten in XSL-FO, PDF is een voorbeeld van dit criterium. In PDF worden resultaten weergegeven met eerst XSLT en vervolgens XSL-FO-formatter. Op deze manier kunnen XML-documenten willekeurig worden opgemaakt. Hoewel XSL-FO het voordeel haalt uit het gebruik van Cascading Style Sheet (CSS)-eigenschappen en deze waar nodig uitbreidt voor het echte formaat, bevat het de levering van paginasjablonen die paginamodellen worden genoemd in de terminologie van XSL-FO. XSL-FO biedt ook opmaak voor redelijk geavanceerde documenten en ondersteunt het genereren van indexen.

## Geschiedenis en basisconcepten ##

In januari 2012 is de Working Draft van XSL-FO voor het laatst geactualiseerd en in november 2013 was de Working Group gesloten. Een XSL-stylesheet specificeert de presentatie van een klasse van XML-documenten door te beschrijven hoe een instantie van de klasse wordt omgezet in een XML-document dat de opmaakvocabulaire gebruikt. XSL-FO is een geïntegreerde presentatietaal en heeft geen semantische markeringen die in HTML worden gebruikt. Bovendien slaat deze taal alle gegevens van het document in zichzelf op, in tegenstelling tot CSS dat de standaardinstellingen van een extern HTML- of XML-document wijzigt.

Het algemene criterium voor het gebruik van XSL-FO is dat de gebruiker een document in een XML-taal schrijft in plaats van in FO. Daarna vindt een XSLT-transformatie plaats. Deze XSLT-transformatie is verantwoordelijk voor de conversie van XML naar XSL-FO. Zodra het XSL-FO-document is gegenereerd, wordt het overgedragen aan een applicatie die een FO-processor wordt genoemd. FO-verwerkers zijn verantwoordelijk voor het omzetten van dit document in een leesbaar en een printbaar document. PDF-bestanden of PS zijn voorbeelden van de meest voorkomende uitvoer van XSL-FO. Maar het betekent niet dat de FO-processor alleen deze twee soorten formaten als uitvoer kan produceren. Sommige FO-processors kunnen de RTF-bestanden weergeven of er kan zelfs een venster verschijnen in de gebruikersinterface, dit venster toont de volgorde van de pagina en hun inhoud.

Een XSL-FO-document verschilt in die zin van een PDF of een PS, het definieert uiteindelijk niet de tekstlay-out op verschillende pagina's. Misschien stijlt het de pagina's en bepaalt het de plaatsen om de inhoud weer te geven. Bovendien organiseert een FO-processor de tekst binnen de grenzen die door het FO-document worden aangegeven. Deze specificatie maakt het zelfs mogelijk dat verschillende FO-processors zich overeenkomstig de resulterende pagina's gedragen. Een voorbeeld van dergelijk gedrag is woordafbreking, weinig FO-processors kunnen woorden afbreken om ruimte te besparen wanneer een regel breekt, terwijl sommige processors deze optie niet selecteren. Het hangt af van de processors om verschillende woordafbrekingsalgoritmen te kiezen die aan hun vereisten voldoen. Deze afbreekalgoritmen kunnen heel eenvoudig of misschien complexer zijn. In sommige situaties bestraft de XSL-FO-specificatie expliciet FO-processors, een zekere mate van keuze in de context van de lay-out.

Deze variatie tussen FO-processors genereert verschillende uitkomsten, waarover processors zich vaak geen zorgen maken. Omdat de algemene focus van XSL-FO ligt op het produceren van gepagineerde/gedrukte documenten. XSL-FO-documenten zelf fungeren meestal als tussenpersoon, hun belangrijkste functie is het genereren van PDF-bestanden of een document dat kan worden afgedrukt als uitvoer die moet worden gedistribueerd. In HTML/CSS of XSL-FO geeft het distribueren van de PDF als eindresultaat in plaats van het invoeren van de opmaaktaal aan dat ontvangers onaangetast blijven door de resulterende veelzijdigheid die wordt geproduceerd als gevolg van verschillen tussen vertolkers van opmaaktaal. Aan de andere kant is het duidelijk dat er geen gemakkelijke manier is dat een document kan voldoen aan de verschillende behoeften van ontvangers, bijvoorbeeld variabele paginagrootte of gewenste lettergrootte, of maatwerk voor pagina's of afdrukken.

## XSLFO-bestandsindeling ##

SL-FO-documenten zijn in feite XML-documenten, maar ze volgen geen schema. In plaats daarvan volgen SL-FO-documenten de syntaxis die is gedefinieerd in de specificatie van hun eigen taal. Er zijn twee secties vereist in elk XSL-FO-document:

1. Een sectie die een lijst met gelabelde paginalay-outs specificeert.
1. Een sectie met alle details van documentgegevens, met opmaak, die de weergave van inhoud op verschillende pagina's via verschillende paginalay-outs bepaalt.

Eigenschappen van de pagina worden vermeld in de paginalay-outs, die de organisatie voor de tekst kunnen definiëren, om te voldoen aan de conventies voor de specifieke taal. Bovendien worden de grootte van de pagina, hun marges en paginareeksen (die verschillende eigenschappen voor de oneven en even pagina's bekrachtigt) ook bepaald door de paginalay-outs.

Het gegevensgedeelte van het document is verdeeld in een reeks stromen, waarbij elke stroom is verbonden met een paginalay-out. De stromen bevatten een lijst met blokken. Deze lijst met blokken kan inline opmaakfuncties of een lijst met tekstgegevens bevatten, of misschien beide tegelijk. Marges van het document kunnen ook de paginanummers of hoofdstukkoppen weergeven. De functionaliteit van zowel blokken als inline-elementen blijft hetzelfde als in de CSS, maar sommige opvul- en margeregels verschillen tussen FO en CSS.

De richting van de paginarichting is volledig gespecificeerd voor de uitbreiding van blokken en inlines, waardoor FO-documenten presteren in andere talen dan Engels. De taal van de FO-specificatie gebruikt de woorden begin en einde in plaats van links en rechts voor de beschrijving van de routebeschrijving. XSL-FO's basisopmaak- en trapsgewijze regels voor inhoud zijn overgenomen van CSS. De taal van de XSL-FO stemt overeen met de volgende specificaties.

## Meerdere kolommen ##

Een pagina kan meerdere kolommen en blokken hebben en kan standaard van de ene kolom naar de andere worden uitgebreid. Meerdere pagina's mogen verschillende breedtes en aantallen kolommen hebben. Alle FO-kenmerken volgen de limieten van een pagina met meerdere kolommen.

### Lijsten ###

Een XSL-FO-lijst wordt opgesteld door twee sets blokken die wang voor wang zijn gerangschikt. Conceptueel gezien geeft een blok aan de linkerkant in een lijst een nummer, een opsommingsteken of een reeks tekst aan, terwijl het rechterblok kan werken zoals verwacht. De nummering van XSL-FO-lijsten wordt meestal gedaan door de XSLT.

### Tafels ###

Een FO-tabel is vergelijkbaar met een HTML/CSS-tabel. De gebruiker kan de rijen met gegevens, stijlinformatie, achtergrondkleur voor elke afzonderlijke cel selecteren. Met behulp van verschillende stijlinformatie heeft de gebruiker het voorrecht om de eerste rij als tabelkoprij te selecteren. De FO-processor kan expliciet worden geïnformeerd over de ruimtespecificatie van elke kolom, of om de tekst in de tabel automatisch aan te passen.

### Indexering ###

XSL-FO 1.1 heeft functies die helpen bij het genereren van een index door te verwijzen naar correct gemarkeerde elementen.

### Een uitkering ###

* Geschikt voor op inhoud gebaseerde publicaties
* Makkelijk te gebruiken
* Goedkoop

## Referenties ##

* [Wat is XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [XSL-opmaakobjecten](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

