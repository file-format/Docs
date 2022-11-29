{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Embedded language","fil", "tillägg", "filformat", "Maya 3D", "Programmeringsguide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya Embedded Language File Format",
  "description":"Läs mer om MEL-filformat och API:er som kan skapa och öppna MEL-filer.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Vad är MEL fil?

En fil med tillägget .mel (Maya Embedded Language) är ett skriptspråk som används av Autodesk Maya för att skapa grafiska gränssnitt. Det låter dig automatisera skapandet av grafiska element med hjälp av körbara skript utöver Mayas grafiska gränssnitt. MEL ger dig möjlighet att skapa grafiska gränssnitt utan att lära dig programmering. Detta uppnås genom att skapa makron och anpassade åtgärder som påskyndar repetitiva uppgifter. Dessa procedurer och skript låter dig skapa anpassad modellering, animationer, dynamik och uppgiftsrendering. Autodesk Maya 2020 kan användas för att öppna och visa innehållet i en EML-fil.

## MEL-filformat - Mer information

En programmerares [referensmanual](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) finns tillgänglig för utvecklare i Mayas dokumentationssektion. MEL är baserat på skalskriptkommandon, liknande UINX, för att uppnå saker. De skriptbaserade kommandona gör det irrelevant för konventionell och objektorienterad programmering (OOP), vilket resulterar i ingen användning av datastrukturer, anropsfunktioner eller användning av OOP som på andra språk.

Några nyckelpunkter om MEL är följande.

`Kommentarer` - Varje påstående i MEL måste sluta med ett semikolon (;), även i slutet av ett block.

`Returnerande värden` - Att ange ett uttryck som returnerar ett värde skrivs inte automatiskt ut värdet i MEL. Istället orsakar det ett fel.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Kommandon för att skapa, redigera och ta bort` - Samma kommando används för att skapa saker, redigera saker eller fråga information om befintliga saker. Men en flagga styr vad (skapa, redigera eller fråga) kommandot gör.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Returvärde från funktion` - Funktionssyntax returnerar automatiskt ett värde. För att få ett returvärde med hjälp av kommandosyntax, måste du omge kommandot i bakåtriktade citat.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Referenser

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

