{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Lidar LASer-bestandsformaat",
  "description":"Leer meer over het LAS-bestandsformaat en API's die LAS-bestanden kunnen maken en openen.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Wat is een LAS-bestand?

Het LAS-bestandsformaat (Lidar LASer) is een binair bestandsformaat dat speciaal is ontworpen voor het opslaan van lidar-puntenwolkgegevens. Het is ontwikkeld en wordt onderhouden door de American Society for Photogrammetry and Remote Sensing (ASPRS) als een gestandaardiseerd formaat voor lidar-gegevensuitwisseling en interoperabiliteit.

LAS-bestanden slaan gedetailleerde informatie op over individuele lidarpunten, inclusief hun 3D-coördinaten (x, y en z), intensiteitswaarden, classificatiecodes en aanvullende attributen. Het formaat ondersteunt zowel discrete retourzendingen als lidargegevens met volledige golfvorm, waardoor de opslag van meerdere retourzendingen per laserpuls mogelijk is.

## LAS-bestandsformaat

De structuur van een LAS-bestand bestaat uit drie hoofdsecties: de bestandskop, de records met variabele lengte (VLR's) en de puntgegevensrecords.

1. Bestandskop: De bestandskop bevat essentiële informatie over het LAS-bestand, zoals de versie van het gegevensformaat, het puntgegevensformaat, het aantal punten, de coördinaten van het omsluitende kader, het coördinatenreferentiesysteem (CRS) en andere metagegevens. Het biedt een samenvatting van de lidargegevens in het bestand.

2. Variabele lengterecords (VLR's): VLR's zijn optioneel en kunnen aanvullende metagegevens en aangepaste informatie over de lidargegevens opslaan. VLR's bieden flexibiliteit bij het uitbreiden van het formaat om tegemoet te komen aan specifieke gebruikersvereisten. Voorbeelden van VLR's zijn onder meer informatie over het sensorsysteem, gegevensverwerkingsparameters of classificatieschema's.

3. Puntgegevensrecords: De puntgegevensrecords slaan de feitelijke lidarmetingen op. Elk puntgegevensrecord vertegenwoordigt een enkel lidarpunt en bevat attributen zoals x-, y- en z-coördinaten, intensiteitswaarden, classificatiecodes (bijvoorbeeld grond, vegetatie, gebouwen) en andere door de gebruiker gedefinieerde attributen. De puntrecords kunnen ook tijdstempels, retourtellingen en scanhoeken opslaan.

LAS-bestanden ondersteunen verschillende gegevensformaten (0 tot 10) om tegemoet te komen aan verschillende soorten lidargegevens en het benodigde informatieniveau. Formaat 0 vertegenwoordigt bijvoorbeeld een eenvoudig puntformaat met basisinformatie, terwijl formaten 1 tot en met 3 uitgebreidere gegevens bieden, inclusief golfvorminformatie voor elke retourzending.

LAS-bestanden worden breed ondersteund door lidar-software en verwerkingstools, waardoor ze een standaardformaat zijn voor lidar-gegevensuitwisseling en -analyse. Bovendien kunnen LAS-bestanden worden gecomprimeerd met behulp van verliesvrije compressietechnieken om de bestandsgrootte te verkleinen met behoud van de oorspronkelijke gegevensgetrouwheid. De gecomprimeerde versie van LAS-bestanden wordt vaak LAZ genoemd, wat efficiënte opslag- en gegevensoverdrachtmogelijkheden biedt.

## Referenties

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
