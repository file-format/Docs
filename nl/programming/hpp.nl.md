{
"datum": "2023-06-08",
  "keywords": [
"hpp-bestand",
"wat is een hpp-bestand",
"wat bevat het hpp-bestand",
"hpp-bestandsvoorbeeld",
"wat is het formaat van het hpp-bestand",
"bestand",
"hpp-bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"HPP-bestandsindeling - C++ headerbestand",
  "description":"Leer meer over het HPP-formaat en API's die HPP-bestanden kunnen maken en openen.",
"linktitle":"HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
"parent":"programmeren"
}
},
"laatste mod": "2023-06-08"
}

## Wat is een HPP-bestand?

Het bestandsformaat ".hpp" wordt vaak gebruikt voor headerbestanden in de programmeertaal C++. Headerbestanden bevatten doorgaans declaraties en definities van functies, klassen, variabelen en constanten die worden gebruikt door andere broncodebestanden in het C++-project.

Het doel van het gebruik van headerbestanden is om een manier te bieden om gemeenschappelijke code over meerdere broncodebestanden te delen zonder de code zelf te dupliceren. Wanneer het C++-bronbestand toegang moet krijgen tot declaraties of definities uit het headerbestand, bevat het het headerbestand met behulp van de preprocessorrichtlijn `#include`.

De bestandsextensie ".hpp" wordt vaak gebruikt om aan te geven dat een bestand een C++ headerbestand is. Het is geen vereiste om deze specifieke extensie voor headerbestanden te gebruiken, en het kan ook voorkomen dat je headerbestanden tegenkomt met ".h" of andere extensies. De keuze voor de extensie is grotendeels een kwestie van conventie en persoonlijke voorkeur.

Wanneer een C++-bronbestand een headerbestand bevat met behulp van `#include`, combineert de compiler effectief de inhoud van het headerbestand met het bronbestand voordat het als een eenheid wordt gecompileerd. Hierdoor heeft het bronbestand toegang tot declaraties en definities in het headerbestand, waardoor de compiler de benodigde informatie krijgt om typecontrole uit te voeren en code te genereren.

## Wat bevat het HPP-bestand?

Hier zijn enkele algemene inhoud die u kunt vinden in het ".hpp"-bestand:

- **Functiedeclaraties:** Headerbestanden bevatten vaak functiedeclaraties zonder hun feitelijke implementatie. Deze declaraties bieden informatie over de naam van de functie, het retourneringstype en de parameters, waardoor andere broncodebestanden de functie kunnen gebruiken zonder dat ze de implementatiedetails hoeven te kennen.
- **Klassedeclaraties:** Headerbestanden kunnen klassedeclaraties bevatten, inclusief klassenaam, lidvariabelen, lidfuncties en toegangsspecificaties. Door klassedeclaratie in het headerbestand op te nemen, kunnen andere broncodebestanden objecten van die klasse maken en toegang krijgen tot de leden ervan.
- **Constante declaraties:** Headerbestanden kunnen constanten definiëren, zoals globale variabelen of enumwaarden die bedoeld zijn om te worden gedeeld over meerdere broncodebestanden. Deze constanten zijn toegankelijk door een headerbestand in andere bronbestanden op te nemen, waardoor ze de gedefinieerde constanten kunnen gebruiken.
- **Typedefinities:** Headerbestanden kunnen typedefinities bevatten met het trefwoord "typedef" of typealiassen met het trefwoord "using". Deze definities creëren nieuwe namen voor bestaande typen, waardoor code beter leesbaar en onderhoudbaar wordt.
- **Inline functiedefinities:** In sommige gevallen kunnen headerbestanden inline functiedefinities bevatten. Inline-functies zijn kleine functies die op de oproeplocatie worden uitgebreid in plaats van dat ze als afzonderlijke functie worden aangeroepen. Door inline functiedefinitie in het headerbestand op te nemen, kan de compiler de functieaanroep rechtstreeks vervangen door de functiebody, waardoor de prestaties mogelijk worden verbeterd.

## HPP-bestandsvoorbeeld

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Wat is het formaat van een HPP-bestand?

HPP is een tekstbestand zonder opmaak, maar volgt de algemene regels en syntaxis van de programmeertaal C++. Hier is een overzicht van het algemene formaat en de structuur van het ".hpp"-bestand:

- **Kopbeschermingen:** Meestal begint een ".hpp"-bestand met kopbeschermingen om te voorkomen dat hetzelfde bestand meerdere keren wordt opgenomen. Dit wordt bereikt met behulp van preprocessor-richtlijnen zoals `#ifndef`, `#define` en `#endif`. De headerbescherming zorgt ervoor dat de inhoud van het bestand slechts één keer wordt opgenomen tijdens het compilatieproces.
- **Include-instructies:** Na header-guards kunt u andere noodzakelijke header-bestanden opnemen met behulp van de `#include`-richtlijn. Dit kunnen standaardbibliotheekheaders zijn of andere aangepaste headers die vereist zijn voor uw code.
- **Verklaringen en definities:** De primaire inhoud van het ".hpp"-bestand zijn de declaraties en, in sommige gevallen, definities van klassen, functies, constanten, type-aliassen en andere elementen. U kunt bijvoorbeeld klassen declareren met het trefwoord 'class', functies met hun retourtype, naam en parameterlijst, en constanten met het trefwoord 'const', gevolgd door hun type en naam.
- **Inline functiedefinities:** In bepaalde gevallen kunt u inline functiedefinities rechtstreeks in het ".hpp"-bestand opnemen. Inline-functies worden meestal gedefinieerd binnen de hoofdtekst van de klasse, wat betekent dat de functiedefinitie naast de declaratie ervan is opgenomen. Dit kunt u doen door de functiedefinitie vooraf te laten gaan door het trefwoord 'inline'.
- **Naamruimtedeclaraties:** Als u naamruimten in uw code gebruikt, kunt u deze declareren in het ".hpp"-bestand. Dit wordt gedaan met behulp van het trefwoord 'namespace' gevolgd door de naam van de naamruimte en het insluiten van de relevante code in het naamruimteblok.

## Referenties
* [Headerbestanden (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

