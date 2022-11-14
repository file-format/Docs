{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PS-bestandsindeling",
  "description":"Meer informatie over PS-bestandsindelingen en API's die PS-bestanden kunnen maken en openen.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een .PS-bestand? ##

PostScript (PS) is een algemene paginabeschrijvingstaal die wordt gebruikt in desktop- en elektronische publicaties. De belangrijkste focus van PostScript (PS) is om het tweedimensionale grafische ontwerp te vergemakkelijken. De meeste talen vereisen een aparte compilatiefase voordat de code wordt uitgevoerd, terwijl het PostScript-formaat (PS) een ongecompliceerde runtime-interpretatie ondersteunt. De vroege versie definieert de grafische vormen, verschillende tekstweergaven en gemodelleerde afbeeldingen op afgedrukte pagina's of weergegeven pagina's, volgens de regels van het Adobe-beeldvormingsmodel. Een programma van PS is in staat om een documentbeschrijving te communiceren tussen een compositie- en printsysteem, waardoor het apparaat onafhankelijk en op hoog niveau blijft. Bovendien is dit programma ook in staat om de weergave van tekst en afbeeldingen op een display te regelen.

PostScript-paginabeschrijving is beschikbaar om te worden weergegeven en weergegeven op de printer en een ander uitvoerapparaat met behulp van de PostScript-interpreter van het apparaat. Omdat de opdrachten voor het afdrukken van tekens, grafische vormen en afbeeldingen worden uitgevoerd door een interpreter, wordt voor dat specifieke apparaat de PostScript-beschrijving op hoog niveau omgezet in het rastergegevensformaat op laag niveau. Over het algemeen worden verschillende toepassingen zoals illustratoren, documentcompositiesystemen en computer-aided design (CAD) geautomatiseerd om PostScript-paginabeschrijvingen te genereren. Over het algemeen moeten programmeurs PostScript-programma's schrijven op het moment dat nieuwe toepassingen worden gemaakt. Een programmeur kan echter profiteren van de mogelijkheden van de PostScript-taal die in geen enkele toepassing toegankelijk zijn door een PS-programma voor die speciale situatie te schrijven.

## Korte geschiedenis ##

Het concept van de PostScript-taal werd voor het eerst geïntroduceerd door John Warnock. In 1966 werkte hij aan een project van New York Harbor. Hij probeerde een tolk te ontwikkelen voor een grote driedimensionale afbeelding voor de database van dat project. Voor het verwerken van deze afbeeldingen bedacht John Warnock de Design System-taal. Ondertussen was Xerox PARC op zoek naar een standaard manier om paginabeelden te definiëren voor hun eerste laserprinter. Hoewel Bob Sproull en William Newman in 1975-76 het Press-formaat (dataformaat) ontwikkelden om laserprinters aan te drijven, was er toch een taal nodig voor meer flexibiliteit. In 1978 trad Warnock toe tot Martin Newell in Xerox PARC en herschreef de interpretatieve taal, JaM, die later werd uitgebreid tot de Interpress-taal. Warnock richtte in december 1982 Adobe Systems op met Chuck Geschke, Doug Brotz, Ed Taft en Bill Paxton. Ze begonnen te werken aan een eenvoudigere taal, PostScript genaamd, vergelijkbaar met Interpress, die in 1984 commercieel werd uitgebracht. Steve Jobs van Apple bezocht hen en adviseerde hen PostScript aan te passen om laserprinters aan te drijven.

In maart 1985 was de eerste printer met een ingebouwde PostScript-interpreter Apple's LaserWriter, die een revolutie teweegbracht in de desktop publishing (DTP). De technische degelijkheid en wijdverbreide beschikbaarheid maakten PostScript tot een taal bij uitstek voor desktop- en elektronische publicaties. In 1990 was een tolk voor de PostScript-taal een essentieel onderdeel van de laserprinters.

## Belangrijkste kenmerken ##

De mogelijkheden van de PostScript-taal om met interactieve afbeeldingen en paginabeschrijvingen om te gaan, hebben de volgende kenmerken:

**Vormen:** Willekeurig van aard, kan bestaan uit rechte lijnen, krommen, vierkanten en kubieke krommen die zowel zelfbewegend als losgekoppeld kunnen zijn (in secties en gaten).

**Schilderoperators:** staan de vormomtrek toe van elke dikte, kleur, vulling of laten de vorm tekenen als een knipsel om het bijsnijden van een andere afbeelding mogelijk te maken.

**Kleuren:** hebben de diversiteit zoals grijswaarden, RGB, CMYK en CIE. Speciale soorten kleuren worden gemodelleerd als verschillende kenmerken: steunkleuren, kleurtoewijzing, zelfs arcering en herhalende patronen.

**Tekst:** volledig geïntegreerd met afbeeldingen. Bovendien kunnen met het Adobe Imaging-model teksttekens worden weergegeven als grafische vormen die door alle normale grafische operators kunnen worden bediend.

**Voorbeeldafbeeldingen**: geëxtraheerd uit originele bronnen (gescande foto's) of kan synthetisch worden geproduceerd. De PostScript-taal biedt diverse middelen om afbeeldingen met elke resolutie en volgens verschillende kleurmodellen op een uitvoerapparaat te regenereren.

Een programmeertaal voor algemene doeleinden kan profiteren van de grafische mogelijkheden van de PostScript-taal door Ps in zijn raamwerk in te bedden. De primitieve datatypes, zoals getallen, karakters, arrays en strings; controle-primitieven, zoals lussen, procedures en voorwaarden; en sommige onconventionele functies, zoals woordenboeken, zijn gespecificeerd in de taal. Met deze functies kunnen programmeurs opdrachten schrijven om bewerkingen op een hoger niveau uit te voeren. Deze operaties op hoog niveau voldoen aan de behoeften van complexe toepassingen. Een dergelijke praktijk is compacter en efficiënter dan het gebruik van een vaste reeks basisbewerkingen.

Programma's die in PostScript zijn geschreven, kunnen worden geproduceerd, gecommuniceerd en geïnterpreteerd in de vorm van ASCII-brontekst. De hele taal kan worden gedefinieerd in de vorm van afdrukbare tekens en witruimte. Deze weergave ondersteunt programmeurs om de taal gemakkelijk te creëren, manipuleren en begrijpen. Bovendien bleef bestandsopslag en -overdracht tussen verschillende computers en besturingssystemen gemakkelijk door machine-onafhankelijkheid.

Binair gecodeerde vormen van de taal zijn mogelijk, wanneer het programma gegarandeerd een volledig transparant communicatiepad naar de PostScript-interpreter heeft. Strikte samenhang met de ASCII-weergave van PS-programma's wordt door Adobe geadviseerd voor documentuitwisseling of archiefopslag.

## Versies ##

PS(.ps) is de bestandsextensie voor een PostScript-document. UK National Archives categoriseren vijf chronologische versies van PostScript-bestanden, gedefinieerd in de DSC-versie: versies 1.0, 2.0, 2.1, 3.0, 3.1. Elke versie definieert belangrijke structurerende opmerkingen. Encapsulated PostScript-bestand (EPS) is een speciaal subtype van PostScript-bestand dat de taal gebruikt om een rechthoekige afbeelding te specificeren. PostScript Language Reference Manual beschrijft een EPS als: "Een ingekapseld PostScript-bestand (EPS) is een PostScript-programma dat ten hoogste één enkele pagina beschrijft in een vorm die door andere toepassingen kan worden geïmporteerd om in een document te worden ingesloten." Een PostScript-documentbestand kan er een EPS-bestand in inkapselen. Een extra gebruik van PostScript wordt vermeld als Display PostScript (DPS). DPS genereert afbeeldingen op het scherm via een grafische engine die gebruik maakt van PostScript-beeldvormingsmodel en -taal.

## Referenties ##

* [PostScript-formaatfamilie](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

