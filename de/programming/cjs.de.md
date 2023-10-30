{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS-bestand - CommonJS-codebestand",
  "description":"Wat is een .cjs-bestand en hoe open je het?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## Wat is een CJS-bestand?

Een CommonJS-bestand (CJS) is een bestand dat JavaScript-code bevat die is geschreven in de CommonJS-syntaxis. CommonJS is een modulesysteem dat is ontworpen om te werken in omgevingen die verder gaan dan frontend-webbrowsers, en wordt vaak gebruikt in JavaScript-omgevingen aan de serverzijde, zoals Node.js.

## CJS-bestandsindeling - Meer informatie

CJS-bestanden zijn geschreven in de CommonJS-syntaxis en kunnen worden bewerkt in elke teksteditor zoals Microsoft Notepad of Apple TextEdit. CommonJS-modules worden doorgaans opgeslagen in afzonderlijke bestanden en zijn bedoeld om code in te kapselen en te modulariseren voor een betere organisatie en onderhoudbaarheid. Deze modules gebruiken de functie require om afhankelijkheden te importeren en het object module.exports of exports om waarden en functies bloot te leggen die door andere delen van de code kunnen worden gebruikt.

## CJS-codevoorbeeld

CommonJS-modules hebben een specifieke syntaxis en structuur die functies bevat zoals de require-functie voor het importeren van andere modules en de module.exports of exports-objecten voor het exporteren van waarden, functies of objecten uit een module. Deze modules worden gebruikt om stukjes code in te kapselen en te scheiden, waardoor het eenvoudiger wordt om grote JavaScript-codebases te beheren en te onderhouden. Hier is een eenvoudig voorbeeld van een CommonJS-module:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## Referenties

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
