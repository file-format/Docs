{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh", "wat is een .hh-bestand", "hoe een .hh-bestand te openen", "extensie", "bestand", ".hh-bestand", ".hh-bestandsformaat", " .hh-bestandsextensie",".HH-bestandsvoorbeeld"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - C++ Header-bestandsindeling",
  "description":"Meer informatie over HH-bestandsindeling en API's die HH-bestanden kunnen maken en openen.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Wat is een HH-bestand?

Een bestand met de extensie .hh is een C++-headerbestand dat de declaratie van variabelen, constanten en functies bevat. Deze declaraties worden gebruikt door de bijbehorende C++-implementatiebestanden, meestal opgeslagen als [.cpp](/nl/programming/cpp/)-bestanden die de daadwerkelijke implementatie van gebruikerslogica bevatten. Er wordt verwezen naar de .hh-headerbestanden in de implementatie-CPP-bestanden met behulp van de `#include`-richtlijn. U kunt zoveel mogelijk header-bestanden aan uw C++-project toevoegen om declaraties op projectniveau op te nemen.

## .HH-bestandsindeling

Een .hh-bestand is een tekstbestand zonder opmaak dat is gemaakt met inachtneming van de definitieregels voor het headerbestand. De meest voorkomende informatie die in een .hh-bestand wordt gedeclareerd, is de volgende.

**'Variabelen'** - In het geval van Object Oriented Programming (OOP), bevat een klasse-headerbestand definities van alle variabelen op klasseniveau die toegankelijk zijn via de broncodebestanden van de implementatie
**'Methods Declaration'** - Alle methodedeclaraties zijn opgenomen in de .h-headerbestanden om toegankelijk te zijn voor meerdere implementatiebestanden.
**'Niet-inline functiedefinities'** - Headerbestanden kunnen ook definities van niet-inline-methoden bevatten.
**`Message Maps`** - Een header-bestand kan ook message maps bevatten in het geval van een MFC-broncode-implementatie. In een dergelijk geval zijn de berichtenkaarten gekoppeld aan de functionaliteitsimplementatie die is gekoppeld aan UI-elementen zoals knop, selectievakje, keuzerondjes, enz.

## Verschil tussen .H- en .HH-bestanden

Blijkbaar is er geen dergelijk verschil tussen de .h- en .hh-headerbestanden, behalve de aanbevolen manier om deze te gebruiken voor de respectievelijke talen, namelijk [C](/nl/programming/c/) of C++. Door uw headerbestanden een naam te geven volgens deze talen, kunt u onderscheid maken tussen deze in een groot project dat een combinatie kan zijn van C- en C++-implementaties.

Als de kopteksten door extensie worden gescheiden, kan uw redacteur bovendien automatisch de juiste opmaak toepassen voor respectievelijk.

Over het algemeen zal de differentiatie van deze twee bestandsindelingen geen kwaad, maar wel voordelig zijn, en wordt aangemoedigd om te volgen voor het onderscheid tussen C en C++.

### Header Guards

Headerbestanden kunnen complexe fouten veroorzaken wanneer meerdere declaraties in hetzelfde bestand zijn opgenomen als gevolg van het toevoegen van andere headerbestanden. Deze dubbele definities veroorzaken compilerfouten. Deze problematische situatie kan worden vermeden via een mechanisme genaamd header guard dat voorwaardelijke compilatierichtlijnen zijn, zoals hieronder weergegeven.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Met deze header controleert de preprocessor of de `ANY_UNIQUE_NAME_HERE_HPP` al is gedefinieerd. Als de header herhaaldelijk in hetzelfde bestand wordt opgenomen, wordt de inhoud van de header genegeerd.

## Referenties

* [Header Files - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Verschil tussen .h- en .hh-bestandsindelingen](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

