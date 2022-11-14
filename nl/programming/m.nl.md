{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab-broncodebestand",
  "description":"Meer informatie over Matlab .m-broncodebestanden en API's die MF-bestanden kunnen maken en openen.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Matlab-broncodebestanden

## Wat is een M (Matlab)-bestand?

Een bestand met de extensie .m is een broncodebestand dat wordt gebruikt door Matlab, een programmeer- en numeriek rekenplatform dat wordt gebruikt voor analyse, de ontwikkeling van algoritmen en simulatiemodellering. Net als andere programmeerbestandsindelingen bevat een M-bestand broncode die Matlab-opdrachten uitvoert om grafieken te plotten, simulaties uit te voeren en andere wiskundige bewerkingen. Een enkele Matlab-simulatie kan meerdere van dergelijke .m-bestanden omvatten die de toepassing kunnen classificeren in scripts, klassen, functies of declaraties. Matlab M-bestanden kunnen met elke teksteditor worden geopend.

## Matlab M-bestandsindeling - Meer informatie

Matlab .m-bestanden zijn tekstbestanden die programmeercode in Matlab-programmeertaal bevatten. Deze kunnen worden geopend en bewerkt in elke teksteditor en worden opgeslagen om te worden uitgevoerd in Matlab-software. Matlab zelf bevat een Live Editor die wordt gebruikt voor het maken van scripts die een combinatie is van code, uitvoer en opgemaakte tekst.

### Matlab-functiebestanden

Net als andere programmeertalen, kunt u een .m-bestand maken dat alleen de definitie bevat van een functie die alleen een specifieke taak uitvoert. Dergelijke bestanden worden ook opgeslagen met de extensie .m en implementeren alleen de functionaliteit met betrekking tot die functie.

### .M Bestandsvoorbeeld

Het volgende is een voorbeeld van een Matlab-functiebestand dat de tijd berekent die nodig is voor een object dat van hoogte h valt.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Om deze functie vanuit de Matlab-editor of vanuit een ander .m-bestand aan te roepen, kan de volgende code worden gebruikt.
```C++
TimeToGround(100)
```

## Referenties

* [Matlab - ondersteunde bestandsindelingen](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Matlab gebruiken](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C-implementatiebestand

## Wat is een M (Objective-C)-bestand?

Een M-bestand wordt ook wel implementatiebestand genoemd dat de broncode van een klasse bevat die is geschreven in Objective-C-taal, een programmeertaal die wordt gebruikt om softwaretoepassingen voor OS X en iOS te schrijven. Objective-C is de belangrijkste programmeertaal die wordt gebruikt door de belangrijkste API's van Apple, Cocoa en Cocoa Touch, voor deze platforms. Een enkele softwaretoepassing die in deze taal is ontwikkeld, kan meerdere .m-bestanden bevatten, die de implementatie van de programmaklassen bevatten. Deze kunnen worden geopend met Apple XCode, jEdit en andere veelgebruikte teksteditors.

## Objective-CM-bestandsindeling - Meer informatie

De M-bestanden zijn geschreven in platte tekst met behulp van de programmeersyntaxis van Objective-C. Elke methode van een klasse moet worden gedefinieerd met alle benodigde code in deze implementatiebestanden. Deze implementatie M-bestanden kunnen een of meer .h-headerbestanden importeren volgens de vereisten. Het importstatement vertelt de compiler waar het headerbestand kan worden gevonden dat bij dit implementatiebestand hoort. De importverklaring is als volgt geschreven.

```C++
#import "network.h"
```

Elke M-bestandsimplementatie begint dan met de `@implementation`-richtlijn, gevolgd door de bestandsnaam van de implementatieklasse. Dit wordt vervolgens gevolgd door alle implementatiemethoden die in het headerbestand zijn gedeclareerd.

### M Bestandsformaat Voorbeeld

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Referenties
* [Over doelstelling C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Gids voor Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

