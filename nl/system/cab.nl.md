{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extensie", "bestand", "format", "systeem", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows Cabinet File",
  "description":"Meer informatie over CAB-bestandsindeling en API's die CAB-bestanden kunnen maken en openen.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Wat is een CAB-bestand? ##

Een bestand met de extensie .cab hoort bij een Windows Cabinet-bestand dat tot de categorie systeembestanden behoort. Het is een bestand dat is opgeslagen in het archiefbestandsformaat in de versies van Microsoft Windows die gecomprimeerde gegevensalgoritmen ondersteunen, zoals de [LZX](/nl/compression/lzx/), Quantum en [ZIP](/nl/compression/zip/ ). Het bestand is van vitaal belang wanneer een gebruiker of ontwikkelaar software-installatiegegevens en -bestanden wil bevatten en delen. De kenmerken van verliesvrije gegevenscompressie en de digitale certificering die in deze bestanden is opgenomen, maken dit bestand perfect voor het opslaan en delen van dergelijke bestanden. Het ondersteunt verschillende Microsoft-installatieprogramma's zoals Device Installer, SetUp API en AdvPak.

## Korte geschiedenis ##

CAB-bestand is een bestandstype voor gegevenscompressie dat is ontwikkeld door Microsoft. Het heette aanvankelijk "Diamond", maar toen werd het in de volksmond bekend als CAB-bestand, een afkorting voor het woord "Cabinet"

## Technische specificatie ##

Een CAB-bestand kan doorgaans maximaal 65535 mappen bevatten, die op hun beurt elk maximaal 65536 bestanden kunnen bevatten. Het CAB-bestandsopslagmechanisme is tijd- en ruimtebesparend omdat het elke map als een gecomprimeerd blok opslaat in plaats van elk bestand afzonderlijk te comprimeren en op te slaan. Lege mappen kunnen niet worden opgeslagen in CAB-archiefmappen. CAB-bestand werd voor het eerst ontwikkeld door Microsoft en wordt gebruikt in verschillende installatieprogramma's, zoals InstallShield met een iets ander formaat. CAB-bestanden zijn vaak verbonden met zelfuitpakkende programma's. Microsoft CAB-bestanden zijn gemakkelijk herkenbaar vanwege hun unieke markering die helpt bij het identificeren van het formaat. De unieke markering voor alle Microsoft CAB-bestanden is een prefix van vier woorden, MSCF. Door deze code te zien, kan een gebruiker gemakkelijk een Microsoft CAB-bestand onderscheiden van andere bestanden en het dienovereenkomstig gebruiken in compressoren of versies. De bestanden kunnen worden gecomprimeerd met meer software-installatiegegevens, of de huidige gegevens kunnen worden gedecomprimeerd met behulp van de juiste software.


## CAB Voorbeeld ##

Het volgende voorbeeld illustreert de relatie tussen bestanden en mappen in een CAB-bestandsstructuur:

{{< figure src="../cab.png" alt="CAB-bestandsindeling" >}}

## Referentie ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
