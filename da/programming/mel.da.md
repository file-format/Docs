{
  "date": "2019-10-11",
  "keywords": [
".mel",
"Maya Indlejret sprog",
"fil",
"udvidelse",
"filformat",
"Maya 3D",
"Programmeringsvejledning"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MEL - Maya Embedded Language File Format",
  "description": "Lær om MEL filformat og API'er, der kan oprette og åbne MEL filer.",
  "linktitle": "MEL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-me-dal"
}
},
  "lastmod": "2021-03-08"
}

## Hvad er en MEL fil?

En fil med filtypenavnet .mel (Maya Embedded Language) er et scriptsprog, der bruges af Autodesk Maya til at skabe grafiske grænseflader. Det lader dig automatisere oprettelsen af grafiske elementer ved hjælp af eksekverbare scripts ud over Mayas grafiske grænseflade. MEL giver dig mulighed for at skabe grafiske grænseflader uden at lære programmering. Dette opnås ved at oprette makroer og tilpassede handlinger, der fremskynder gentagne opgaver. Disse procedurer og scripts giver dig mulighed for at skabe tilpasset modellering, animationer, dynamik og opgavegengivelse. Autodesk Maya 2020 kan bruges til at åbne og se indholdet af en EML-fil.

## MEL-filformat - flere oplysninger

En programmørs [reference manual](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) er tilgængelig for udviklere i Mayas dokumentationssektion. MEL er baseret på shell scripting kommandoer, svarende til UINX, for at opnå ting. De scriptbaserede kommandoer gør det irrelevant for konventionel og objektorienteret programmering (OOP), hvilket resulterer i ingen brug af datastrukturer, kaldefunktioner eller brug af OOP som på andre sprog.

Nogle nøglepunkter om MEL er som følger.

`Kommentarer` - Hver sætning i MEL skal ende med et semikolon (;), selv i slutningen af en blok.

`Returnerende værdier` - Angivelse af et udtryk, der returnerer en værdi, udskriver ikke automatisk værdien i MEL. I stedet forårsager det en fejl.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Kommandoer til oprettelse, redigering og sletning` - Den samme kommando bruges til at oprette ting, redigere ting eller forespørge om oplysninger om eksisterende ting. Et flag styrer dog, hvad (opret, rediger eller forespørg) kommandoen gør.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return værdi fra funktion` - Funktionssyntaks returnerer automatisk en værdi. For at få en returværdi ved hjælp af kommandosyntaks, skal du omslutte kommandoen i backquotes.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Referencer

 * [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

