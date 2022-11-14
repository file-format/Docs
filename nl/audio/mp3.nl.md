{
  "date" : "2019-12-13",
  "keywords" :[ "MP3", "bestand", "extensie", "formaat", "Audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over MP3-bestandsindelingen en API's die MP3-bestanden kunnen openen en maken.",
  "title" :"MP3 - Audiobestandsindeling",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2020-09-04"
}

## Wat is een MP3-bestand?

Bestanden met de extensie .mp3 zijn digitaal gecodeerde bestandsindelingen voor audiobestanden die formeel zijn gebaseerd op de MPEG-1 Audio Layer III of MPEG-2 Audio Layer III. Het is ontwikkeld door de Moving Picture Experts Group (MPEG) die Layer 3-audiocompressie gebruikt. De compressie die wordt bereikt door het MP3-bestandsformaat is 1/10 van de grootte van .WAV- of .AIF-bestanden. Het formaat biedt voordelen van het streamen van dergelijke audiobestanden via internet om online te luisteren, wat voorheen niet mogelijk was vanwege de grote bestandsgroottes van audiobestanden. De geluidskwaliteit van een MP3-audiobestand kan worden geregeld door parameterinstellingen zoals bitrate, sample rate, joint of normale stereo.

## Korte geschiedenis van het MP3-bestandsformaat

Het MP3-formaat is uitgevonden en ontwikkeld door een Duits bedrijf, Fraunhofer-Gesellshart. Het algoritme heeft patenten in licentie gegeven voor de compressietechnologie die het gebruikt. Hier is een handige tijdlijn van MP3:

• **1987** - Het Fraunhofer Instituut in Duitsland begon onderzoek te doen naar audiocodering van hoge kwaliteit met een lage bitsnelheid. Het heette het EUREKA-project EU147, Digital Audio Broadcasting.

• **januari 1988** - De Moving Picture Experts Group, of MPEG, werd opgericht.

• **April 1989** - Fraunhofer ontving in Duitsland een patent voor MP3.

• **1992** - Dieter Seitzer, die de Fraunhofer hielp met zijn onderzoek, integreerde zijn audiocodering met MPEG-1.

• **1993** - De MPEG-1-standaard is gepubliceerd.

• **1994** - De MPEG-2-standaard is ontwikkeld en een jaar later gepubliceerd.

• **nov. 26, 1996** - Het Amerikaanse patent voor MP3 is verleend.

• **September 1998** - Fraunhofer begon octrooirechten af te dwingen. Degene die de MP3-audiocodering gebruikte, betaalde een licentievergoeding aan Fraunhofer.

• **Februari 1999** - SubPop, een platenmaatschappij, distribueerde muziek in het MP3-formaat, het eerste bedrijf dat dit deed.

• **1999** - De eerste draagbare MP3-spelers verschijnen.

## MP3-bestandsindeling

Een MP3-bestand bestaat uit MP3-frames waarbij elk frame bestaat uit een header en een datablok. De frames zijn niet onafhankelijk en kunnen meestal niet worden geëxtraheerd op willekeurige framegrenzen. De datablokken van het bestand bevatten informatie over de audio in termen van frequenties en amplitudes. Het synchronisatiewoord in de kop identificeert het begin van een geldig frame. Dit wordt gevolgd door 3 bits waarbij het eerste bit aangeeft dat het een MPEG-standaard is en de resterende 2 bits laten zien dat laag 3 wordt gebruikt; vandaar MPEG-1 Audio Layer 3 of MP3. Hierna zullen de waarden verschillen, afhankelijk van het MP3-bestand.

[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3 definieert het waardenbereik voor elke sectie van de header samen met de specificatie van de header. De meeste MP3-bestanden bevatten tegenwoordig [ID3](https://en.wikipedia.org/wiki/ID3) [metadata](https://en.wikipedia.org/wiki/Metadata), die voorafgaan aan of volgen op de MP3-frames, zoals aangegeven in het diagram. De datastroom kan een optionele controlesom bevatten.

## Referenties ##

* [MP3 - Door Wikipedia](https://en.wikipedia.org/wiki/MP3)

