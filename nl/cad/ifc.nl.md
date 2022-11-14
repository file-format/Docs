{
  "date" : "2020-03-16",
  "keywords" :[ "IFC-bestand", "Formaat", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over IFC-bestandsindeling en API's die IFC-bestanden kunnen maken en openen.",
  "title" :"IFC-bestandsindeling",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een IFC-bestand?

Bestanden met de IFC-extensie verwijzen naar de bestandsindeling Industry Foundation Classes (IFC) die internationale normen vaststelt voor het importeren en exporteren van bouwobjecten en hun eigenschappen. Dit bestandsformaat biedt interoperabiliteit tussen verschillende softwaretoepassingen. Specificaties voor dit bestandsformaat zijn ontwikkeld en onderhouden door buildingSMART International als datastandaard. Het uiteindelijke doel van het IFC-bestandsformaat is het verbeteren van communicatie, productiviteit, levertijd en kwaliteit gedurende de hele levenscyclus van een gebouw.

Vanwege de vastgestelde normen voor veelvoorkomende objecten in de bouwsector, vermindert het het verlies van informatie tijdens de overdracht van de ene toepassing naar de andere. IFC kan gegevens bewaren voor geometrie, berekening, hoeveelheden, facility management, prijzen enz. voor veel verschillende beroepen (architect, elektrotechniek, HVAC, constructief, terrein enz.).

## Korte geschiedenis ##

Het IFC-initiatief werd in 1994 door Autodesk genomen om geïntegreerde applicatie-ontwikkeling te ondersteunen en omvatte bedrijven als Honeywell, Butler Manufacturing en AT&T. In 1995 werd het lidmaatschap opengesteld voor iedereen en werd de naam veranderd in International Alliance for Interoperability. De bedoeling van de non-profitorganisatie was om de Industry Foundation Class (IFC) te publiceren als een AEC-productmodel. In 2005 werd de naam opnieuw veranderd en buildSMART onderhoudt deze nu.

## IFC-bestandsindeling ##

Het IFC-bestandsformaat heeft in het verleden verschillende wijzigingen ondergaan om de bestandsformaatspecificaties v4. Er zijn van tijd tot tijd enkele kleine wijzigingen doorgevoerd en deze zijn als addendum in de specificaties opgenomen. Hieronder volgt een lijst met verschillende versies van bestandsspecificaties die in het verleden openbaar zijn gemaakt.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (maart 2013) ifcXML2x3 (juni 2007)
* IFC2x3 (februari 2006) ifcXML2 voor IFC2x2 add1 (RC2)
* IFC2x2 Addendum 1 (juli 2004)ifcXML2 voor IFC2x2 (RC1)
* IFC 2x2IFC 2x Addendum 1ifcXML1 voor IFC2x en
* IFC2x Addendum 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

De nieuwste versies van de specificaties van de IFC-bestandsindelingen zijn altijd beschikbaar op de buildingSMART-website en de ontwikkelaar dient deze te raadplegen voor elk type toepassing dat hij van plan is te ontwikkelen. Op het moment van schrijven van dit artikel zijn de specificaties van versie 4 de nieuwste die online beschikbaar zijn.

### IFC-gegevensbestandsindelingen ###

Het IFF-bestandsformaat ondersteunt gegevensuitwisseling tussen applicaties die verschillende formaten gebruiken, zoals hieronder vermeld:

**IFC:** Dit is het standaard IFC-uitwisselingsformaat en gebruikt de fysieke STEP-bestandsstructuur volgens ISO 10303-21. Dit bestandsformaat heeft de bestandsextensie .ifc en is het meest gebruikte IFC-formaat.

**IFC-XML:** Het is een XML-bestandsformaatversie van IFC die rechtstreeks kan worden gegenereerd door de verzendende toepassing volgens de ISO 10303-28-structuur, ook wel STEP-XML genoemd. Het IFC-XML-bestandsformaat wordt geschikt geacht voor interoperabiliteit tussen XML-tools. In vergelijking met het IFC-bestandsformaat is de IFC-XML 300-400% groter in omvang.

**IFC-ZIP:** Het is een [ZIP](/nl/compression/zip/) gecomprimeerde versie van IFC of IFC-XML waarbij één van deze bestanden zich in de hoofdmap van het zip-archief bevindt. Dit formaat comprimeert een .ifc met 60-80% en een .ifc XML-bestand met 90-95%.

### IFC Architectuur ###

De IFC-specificatie omvat termen, concepten en gegevensspecificatie-items die afkomstig zijn uit gebruik binnen disciplines, ambachten en beroepen van de bouw- en facility management-industrie. Termen en concepten gebruiken de gewone Engelse woorden, de gegevensitems binnen de gegevensspecificatie volgen een naamgevingsconventie.

de namen van gegevensitems voor typen, entiteiten, regels en functies beginnen met het voorvoegsel "Ifc" en gaan verder met de Engelse woorden in de naamgevingsconventie van CamelCase (geen onderstrepingsteken, eerste letter van het woord in hoofdletters); de attribuutnamen binnen een entiteit volgen de CamelCase-naamgevingsconventie zonder prefix; de definities van eigenschappensets die deel uitmaken van deze standaard beginnen met het voorvoegsel "Pset_" en gaan verder met de Engelse woorden in CamelCase-naamgevingsconventie; de definities van de hoeveelheidset die deel uitmaken van deze standaard beginnen met het voorvoegsel "Qto_" en gaan verder met de Engelse woorden in CamelCase-naamgevingsconventie.

De dataschema-architectuur van IFC definieert vier conceptuele lagen, elk individueel schema is toegewezen aan precies één conceptuele laag.

**Resourcelaag** — de onderste laag omvat alle individuele schema's die resourcedefinities bevatten, deze definities bevatten geen globaal unieke identifier en mogen niet onafhankelijk worden gebruikt van een definitie die op een hogere laag is gedeclareerd;

**Kernlaag** — de volgende laag bevat het kernelschema en de kernuitbreidingsschema's, die de meest algemene entiteitsdefinities bevatten, alle entiteiten die in de kernlaag of daarboven zijn gedefinieerd, hebben een wereldwijd unieke id en optioneel eigenaar- en geschiedenisinformatie;

**Interoperabiliteitslaag** — de volgende laag bevat schema's met entiteitsdefinities die specifiek zijn voor een algemeen product-, proces- of resourcespecialisatie die in verschillende disciplines wordt gebruikt. Deze definities worden doorgaans gebruikt voor uitwisseling tussen domeinen en het delen van constructie-informatie;

**Domeinlaag** — de hoogste laag bevat schema's met entiteitsdefinities die specialisaties zijn van producten, processen of bronnen die specifiek zijn voor een bepaalde discipline. Deze definities worden doorgaans gebruikt voor uitwisseling binnen het domein en het delen van informatie.

## Referenties ##

* [Industry Foundation Classes - Door Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

