{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - Gecomprimeerd LIDAR-gegevensuitwisselingsbestand",
  "description":"Leer meer over het LAZ-bestandsformaat en API's die LAZ-bestanden kunnen maken en openen.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Wat is een LAZ-bestand?

Het LAZ-bestandsformaat is een gecomprimeerde versie van het LAS-bestandsformaat (Lidar LASer), dat speciaal is ontworpen voor het opslaan van lidar-puntenwolkgegevens. LAZ-bestanden behouden dezelfde gegevens en structuur als LAS-bestanden, maar maken gebruik van verliesloze compressietechnieken om de bestandsgrootte te verkleinen met behoud van de oorspronkelijke gegevensgetrouwheid.

## LAZ-bestandsindeling - korte geschiedenis

Het LAZ-bestandsformaat is ontwikkeld om tegemoet te komen aan de groeiende vraag naar efficiënte opslag en verzending van grote lidar-datasets. Door LAS-bestanden te comprimeren, verkleinen LAZ-bestanden hun omvang aanzienlijk, waardoor ze gemakkelijker te beheren en over te dragen zijn. De compressie wordt bereikt door een combinatie van verschillende algoritmen te gebruiken, zoals entropiecodering en codering met variabele lengte, om lidar-puntattributen in een compactere vorm weer te geven.

## LAZ-bestandsindeling

Ondanks de compressie behouden LAZ-bestanden de mogelijkheid om de originele LAS-gegevens volledig te herstellen zonder enig verlies van informatie. Dit betekent dat zodra een LAZ-bestand is gedecomprimeerd, het op dezelfde manier kan worden verwerkt en geanalyseerd als een niet-gecomprimeerd LAS-bestand. Het compressie- en decompressieproces wordt doorgaans uitgevoerd met behulp van gespecialiseerde software of bibliotheken die het LAZ-formaat ondersteunen.

Het LAZ-bestandsformaat blijft compatibel met LAS-bestanden, waardoor interoperabiliteit tussen lidar-software en verwerkingstools wordt gegarandeerd. Dit betekent dat toepassingen die LAS-bestanden kunnen lezen en verwerken doorgaans LAZ-bestanden zonder enige wijziging kunnen verwerken. Bovendien bevatten LAZ-bestanden nog steeds de bestandskop, records met variabele lengte (VLR's) en puntgegevensrecords, waarbij dezelfde structuur als LAS-bestanden behouden blijft.

## Voordelen van LAZ-bestandsformaat

**Verkleinde bestandsgrootte:** LAZ-compressie verkleint de bestandsgrootte van lidar-datasets aanzienlijk, waardoor ze beter beheersbaar en gemakkelijker op te slaan en over te dragen zijn.

**Gegevensintegriteit:** LAZ-compressie is verliesvrij, wat betekent dat de gedecomprimeerde gegevens een exacte replica zijn van de originele LAS-gegevens, waardoor geen verlies van informatie of precisie wordt gegarandeerd.

**Interoperabiliteit:** LAZ-bestanden zijn compatibel met LAS-bestanden, waardoor naadloze integratie met bestaande lidar-software en workflows mogelijk is.

**Efficiënte verwerking:** Vanwege hun kleinere omvang kunnen LAZ-bestanden sneller worden geladen en verwerkt, waardoor de algehele verwerkings- en analysetijden worden verbeterd.

Het LAZ-bestandsformaat is in de lidar-gemeenschap algemeen aanvaard als standaard voor de gecomprimeerde opslag en uitwisseling van lidar-gegevens. Het biedt een balans tussen efficiënte datacompressie en data-integriteit, waardoor het eenvoudiger wordt om grote lidar-datasets te verwerken, terwijl de nauwkeurigheid en kwaliteit van de originele data behouden blijft.

## Referenties

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
