{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Computer Graphics Metafile", "File", "Extension", "File Format", "Vector Graphics", "Metafile Descriptor"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CGM-bestandsindeling",
  "description":"Meer informatie over CGM-bestandsindelingen en API's die CGM-bestanden kunnen maken en openen.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Wat is een CGM-bestand? ##

Computer Graphics Metafile (CGM) is een gratis, platformonafhankelijk, internationaal standaard metabestandsformaat voor het opslaan en uitwisselen van vectorafbeeldingen (2D), rasterafbeeldingen en tekst. CGM hanteert een objectgeoriënteerde benadering en veel functievoorzieningen voor beeldproductie. CGM gebruikt deze objectgeoriënteerde kenmerken voor het opnieuw vormen van grafische elementen om een afbeelding weer te geven. Een metabestand bevat noodzakelijke informatie die andere bestanden definieert. In CGM bevat een op tekst gebaseerd bronbestand alle grafische elementen die later kunnen worden gecompileerd tot een binair bestand. Kortom, CGM is een manier om 2D grafische gegevensuitwisseling te vergemakkelijken, onafhankelijk van een bepaald platform of apparaat.

Het CGM-formaat biedt verschillende elementen om functies uit te voeren en objecten aan te duiden om geometrische primitieven en grafische informatie aan te passen. Hoewel CGM is vervangen door andere formaten om grafische kunst op webpagina's weer te geven, omdat het niet goed wordt ondersteund door webpagina's, is het nog steeds erg populair bij industriële, luchtvaart- en andere technische toepassingen. Hoewel World Wide Web Consortium WebCGM heeft ontwikkeld, een alternatieve benadering voor het gebruik van CGM op het web. De primaire CGM-implementatie was een illustratie van de volgorde van basisbewerkingen van het Graphical Kernel System (GKS). Het is niet veel gebruikt in professionele ontwerpen, maar is grotendeels verdrongen door andere formaten zoals DXF en SVG.

## Geschiedenis ##

CGM bleek in 1987 een internationale standaard te zijn (ISO 8632-1987) en werd ook in het VK door BSI en de VS door ANSI als nationale standaard aangenomen. Na een aantal wijzigingen in 1991 werd in 1992 een herziene norm van CGM vrijgegeven (ISO 8632:1992). In 2001 ontwikkelde World Wide Web Consortium WebCGM met verbeterde mogelijkheden voor gebruik met de webpagina's. In 2007 werd de tweede versie van WebCGM uitgebracht en de derde versie werd uitgebracht in 2010 met verbeterde mogelijkheden.

## CGM-bestandsindeling ##

Metabestanden voor computergraphics zijn in feite een database voor grafische informatie en bieden de middelen voor het vastleggen, opslaan en verzenden van grafische gegevens. Bijgevolg moet er een grafische systeemcomponent zijn voor het gelijktijdig creëren van de database samen met het uitvoeren van een applicatie in een metabestandsformaat. In de meeste gevallen is dit onderdeel de Metafile-generator. Daarnaast is er behoefte aan een andere component die grafische gegevens in een metabestand kan ophalen, interpreteren en weergeven. Aan deze behoefte wordt voldaan door de aanwezigheid van een metafile-tolk. De volgende afbeelding geeft de grafische metafile-werkomgeving weer.

De relatie van CGM met andere componenten van een typisch grafisch systeem wordt geïllustreerd in de bovenstaande afbeelding. Uit de figuur blijkt ook dat de functionaliteit van het metabestand niet afhankelijk is van de uiteindelijke apparaatuitvoer.

Over het algemeen zijn er twee categorieën metabestanden: **sectie-opname** en **foto-opname**. De primaire functionaliteit van het metabestand voor het vastleggen van afbeeldingen is het vastleggen van apparaatonafhankelijke, meerdere beelddefinities. Terwijl metabestanden voor het vastleggen van sessies de systeeminterface gebruiken om de uitvoerdialoog in een grafisch systeem vast te leggen. CGM behoort tot de categorie van metabestanden voor het vastleggen van statische afbeeldingen. CGM zorgt voor een overzichtelijke opstelling van componenten met een structuur op twee niveaus.

1. Metabestandsbeschrijving
1. Een verzameling logisch onafhankelijke afbeeldingen

Elke afbeelding is een verzameling afbeeldingsbeschrijvingen en een afbeeldingslichaam inclusief een afbeeldingsdefinitie. metabestandsdescriptor definieert beschrijvende informatie die gelijkelijk van toepassing is op alle afbeeldingen van dat metabestand. Deze informatie helpt de tolk om een metabestand correct te ontleden en de bronnen te herkennen die nodig zijn voor het correct weergeven van een afbeelding. Hoewel de afbeeldingsdescriptor ook de beschrijvende informatie insluit, kan hij alleen de afbeelding herkennen waarin de descriptor zich bevindt. In dit bestandsformaat is elke beelddefinitie op zichzelf staand en logisch soeverein. Ze zijn onafhankelijk van alle andere beelddefinities in een bestand. Direct na de interpretatie van de meta-descriptor kunnen afbeeldingen willekeurig worden benaderd en geïnterpreteerd. Verandering in de staat van eerdere foto's heeft geen effect op hun opvolgers. Deze beeldonafhankelijkheid is een ander opvallend kenmerk van CGM.CGM bestaat uit een coördinatenruimte die 2D Cartesiaanse coördinaten zijn die virtuele apparaatcoördinaten worden genoemd en die kunnen worden weergegeven door middel van een getal of precisie die het bereik en de granulariteit vertegenwoordigt. CGM specificeert zowel de directe selectie van kleuren als op index gebaseerde selectie. In het eerste geval bestaat de kleurspecificatie uit een RGB-triple, terwijl later de kleurspecificatie een index in een kleurentabel aangeeft.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
