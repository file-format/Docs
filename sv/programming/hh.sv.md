{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh","vad är en .hh-fil","hur man öppnar .hh-fil", "tillägg", "fil", ".hh-fil",".hh filformat", " .hh filtillägg",".HH filexempel"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - C++ Header File Format",
  "description":"Läs mer om HH-filformat och API:er som kan skapa och öppna HH-fil.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Vad är HH fil?

En fil med filändelsen .hh är en C++-huvudfil som innehåller deklarationen av variabler, konstanter och funktioner. Dessa deklarationer används av motsvarande C++-implementeringsfiler, vanligtvis sparade som [.cpp](/sv/programming/cpp/)-filer som innehåller den faktiska implementeringen av användarlogik. .hh-huvudfilerna hänvisas till i implementerings-CPP-filerna med hjälp av `#include`-direktivet. Du kan lägga till så många rubrikfiler som möjligt i ditt C++-projekt för att inkludera projektnivådeklarationer.

## .HH Filformat

En .hh-fil är en vanlig textfil som skapas med hänsyn till reglerna för rubrikfilens definition. Den vanligaste informationen som deklareras i en .hh-fil inkluderar följande.

**`Variables`** - När det gäller objektorienterad programmering (OOP), innehåller en klasshuvudfil definitioner av alla klassnivåvariabler som är tillgängliga över implementeringens källkodsfiler
**`Methods Declaration`** - Alla metoddeklarationer ingår i .h-huvudfilerna för att vara tillgängliga över flera implementeringsfiler.
**`Non-Inline Function Definitions`** - Header-filer kan också innehålla definitioner av icke-inline-metoder.
**`Message Maps`** - En rubrikfil kan också innehålla meddelandekartor vid implementering av en MFC-källkod. I sådana fall är meddelandekartorna länkade till funktionalitetsimplementeringen som är länkad till UI-element som knapp, kryssruta, radioknappar, etc.

## Skillnaden mellan .H och .HH-filer

Tydligen finns det ingen sådan skillnad mellan .h- och .hh-huvudfilerna förutom det rekommenderade sättet att använda dessa för respektive språk, dvs [C](/sv/programming/c/) eller C++. Att namnge dina rubrikfiler enligt dessa språk hjälper dig att skilja mellan dessa i ett stort projekt som kan vara en blandning av C- och C++-implementationer.

Dessutom, om rubrikerna är åtskilda av förlängning, kan din redaktör tillämpa lämplig formatering automatiskt för respektive.

Sammantaget kommer differentieringen av dessa två filformat inte att göra någon skada, men kommer att vara fördelaktig och uppmuntras att följa för C och C++ distinktion.

### Header Guards

Header-filer kan leda till komplexa fel där flera deklarationer ingår i samma fil som ett resultat av att andra header-filer läggs till. Dessa dubbletter av definitioner ger upphov till kompilatorfel. Denna problematiska situation kan undvikas via en mekanism som kallas header guard som är villkorliga kompileringsdirektiv som visas nedan.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Med denna rubrik kontrollerar förprocessorn om `ANY_UNIQUE_NAME_HERE_HPP` redan har definierats. Om rubriken upprepas inkluderas i samma fil, kommer innehållet i rubriken att ignoreras.

## Referenser

* [Header Filers - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Skillnaden mellan .h och .hh filformat](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

