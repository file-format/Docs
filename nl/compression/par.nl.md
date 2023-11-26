{
"date":"2023-07-18",
   "keywords":[
"PAR",
"PAR-bestand",
"hoe een par-bestand te openen",
"bestand",
"PAR bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"PAR-bestandsindeling - Parchive-indexbestand",
   "description":"Leer meer over het PAR-formaat en API's waarmee PAR-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent":"compressie"
}
},
"lastmod":"2023-07-18"
}

## Wat is een PAR-bestand?

Binnen Parchive-archieven (PAR) verwijst een .par-bestand naar een indexbestand dat een groep pariteitsvolumes of pariteitsblokken bevat. Dit indexbestand wordt gebruikt voor foutdetectie en hersteldoeleinden wanneer een of meer bestanden in het archief verloren of beschadigd zijn.

Een Parchive-archief bestaat doorgaans uit zowel de originele gegevensbestanden als de overeenkomstige pariteitsvolumes. Pariteitsvolumes worden gemaakt met behulp van Reed-Solomon-foutcorrectie-algoritmen. Deze pariteitsvolumes bevatten redundante informatie die kan worden gebruikt om de originele gegevensbestanden te herstellen.

Het .par-bestand, ook wel een pariteitsvolumeset genoemd, bevat informatie over de structuur en locatie van de pariteitsvolumes binnen het archief. Het dient als index of kaart voor het herstelproces. Door het .par-bestand te gebruiken, kan gespecialiseerde PAR-software bepalen welke pariteitsvolumes nodig zijn en hoe deze moeten worden gebruikt om de ontbrekende of beschadigde bestanden te reconstrueren.

Wanneer een of meer bestanden in het Parchive-archief ontoegankelijk of beschadigd raken, kan het .par-bestand worden gebruikt in combinatie met de beschikbare pariteitsvolumes om de verloren gegevens te herstellen. De PAR-software leest het .par-bestand, identificeert de ontbrekende of beschadigde bestanden en gebruikt de pariteitsvolumes om ze te reconstrueren.

## Hoe open je een PAR-bestand?

Om .par-bestanden te openen en te gebruiken, hebt u gespecialiseerde PAR-software nodig. Hier zijn een paar populaire softwareopties die overweg kunnen met .par-bestanden:

- **QuickPar:** QuickPar is een veelgebruikte PAR-software voor Windows. Hiermee kunt u PAR-bestanden maken, verifiëren en repareren. U kunt een .par-bestand openen in QuickPar om de integriteit ervan te verifiëren of het gebruiken om beschadigde of ontbrekende bestanden in een Parchive-archief te repareren.

- **MultiPar:** MultiPar is een andere populaire PAR-software die beschikbaar is voor Windows. Het ondersteunt zowel de PAR- als PAR2-bestandsindelingen en biedt geavanceerde functies voor het maken, verifiëren en repareren van archieven. MultiPar kan .par-bestanden openen en foutdetectie- en herstelbewerkingen uitvoeren op basis van de geleverde pariteitsvolumes.

- **MacPAR deLuxe:** MacPAR deLuxe is PAR-software die speciaal is ontworpen voor macOS. Het ondersteunt PAR- en PAR2-bestandsformaten en biedt vergelijkbare functionaliteit als QuickPar en MultiPar. MacPAR deLuxe kan .par-bestanden openen en helpen bij het verifiëren van archieven en het herstellen van beschadigde of ontbrekende bestanden.

## PAR-bestandsindeling - Meer informatie

Het PAR-bestandsformaat, gewoonlijk Parchive genoemd, is een specifiek bestandsformaat dat wordt gebruikt voor het creëren van pariteitsgegevens en het uitvoeren van foutdetectie en herstel in bestandsarchieven. Het PAR-bestandsformaat bestaat doorgaans uit drie typen: PAR, PAR2 en PAR3.

- **PAR:** Het originele PAR-bestandsformaat, ook bekend als PAR1, is ontwikkeld door het Parchive-project. Het bevat pariteitsgegevens die zijn gegenereerd op basis van de originele gegevensbestanden. PAR-bestanden bieden een basisniveau van foutdetectie en -herstel, maar hebben beperkingen wat betreft de mogelijkheden voor foutcorrectie.

- **PAR2:** PAR2 is een verbeterde versie van het PAR-bestandsformaat. Het biedt meer geavanceerde foutcorrectiemogelijkheden en verbeterde herstelfuncties. PAR2-bestanden worden doorgaans gebruikt voor het maken van pariteitsgegevens waarmee verloren of beschadigde bestanden in een archief kunnen worden hersteld. PAR2-bestanden bieden een betere bescherming tegen gegevenscorruptie en worden veel gebruikt voor bestandsarchiveringsdoeleinden.

- **PAR3:** PAR3 is de nieuwste versie van het PAR-bestandsformaat en biedt verdere verbeteringen op het gebied van foutcorrectie en herstel. Het biedt zelfs hogere niveaus van redundantie en foutcorrectiemogelijkheden vergeleken met PAR2. PAR3-bestanden zijn ontworpen om robuustere beschermings- en herstelopties te bieden voor gegevens die in archieven zijn opgeslagen.

Zowel de PAR2- als de PAR3-bestandsindelingen worden breed ondersteund door PAR-software en bieden de mogelijkheid om de integriteit van bestanden in een archief te verifiëren en verloren of beschadigde gegevens te herstellen. PAR- en PAR2-bestanden worden nog steeds veel gebruikt, terwijl PAR3-bestanden geleidelijk aan populairder worden vanwege hun verbeterde mogelijkheden voor foutcorrectie.

## Referenties
* [Parchief](https://en.wikipedia.org/wiki/Parchive)

