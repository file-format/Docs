{
"date": "2023-06-08",
  "keywords": [
"hpp-fil",
"vad är en hpp-fil",
"vad innehåller hpp-filen",
"hpp fil exempel",
"vilket är formatet på hpp-filen",
"fil",
"hpp filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "HPP-filformat - C++ Header File",
  "description":"Läs mer om HPP-format och API:er som kan skapa och öppna HPP-filer.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## Vad är en HPP fil?

Filformatet ".hpp" används vanligtvis för rubrikfiler i programmeringsspråket C++. Rubrikfiler innehåller vanligtvis deklarationer och definitioner av funktioner, klasser, variabler och konstanter som används av andra källkodsfiler i C++-projekt.

Syftet med att använda rubrikfiler är att tillhandahålla ett sätt att dela gemensam kod över flera källkodsfiler utan att duplicera själva koden. När C++-källfilen behöver komma åt deklarationer eller definitioner från header-filen, inkluderar den header-filen med hjälp av preprocessor-direktivet `#include`.

Filtillägget ".hpp" används ofta för att indikera att en fil är en C++-huvudfil. Det är inte ett krav att använda detta specifika tillägg för rubrikfiler, och du kan även stöta på rubrikfiler med ".h" eller andra tillägg. Valet av förlängning är till stor del en fråga om konvention och personliga preferenser.

När en C++-källfil innehåller rubrikfil med hjälp av `#include`, kombinerar kompilatorn effektivt innehållet i headerfilen med källfilen innan den kompileras som en enhet. Detta tillåter källfilen att komma åt deklarationer och definitioner i header-filen, vilket ger den nödvändiga informationen för kompilatorn för att utföra typkontroll och kodgenerering.

## Vad innehåller HPP-filen?

Här är lite vanligt innehåll som du kan hitta i ".hpp"-filen:

- **Funktionsdeklarationer:** Headerfiler innehåller ofta funktionsdeklarationer utan deras faktiska implementeringar. Dessa deklarationer ger information om funktionens namn, returtyp och parametrar, vilket gör att andra källkodsfiler kan använda funktionen utan att behöva känna till implementeringsdetaljer.
- **Klassdeklarationer:** Headerfiler kan innehålla klassdeklarationer, inklusive klassnamn, medlemsvariabler, medlemsfunktioner och åtkomstspecifikationer. Genom att inkludera klassdeklaration i rubrikfilen kan andra källkodsfiler skapa objekt av den klassen och komma åt dess medlemmar.
- **Konstanta deklarationer:** Rubrikfiler kan definiera konstanter, såsom globala variabler eller enumvärden som är avsedda att delas mellan flera källkodsfiler. Dessa konstanter kan nås genom att inkludera rubrikfil i andra källfiler, så att de kan använda de definierade konstanterna.
- **Typdefinitioner:** Rubrikfiler kan innehålla typdefinitioner som använder "typedef" nyckelord eller typalias med "using" nyckelord. Dessa definitioner skapar nya namn för befintliga typer, vilket gör koden mer läsbar och underhållbar.
- **Inline funktionsdefinitioner:** I vissa fall kan rubrikfiler innehålla inline funktionsdefinitioner. Inline-funktioner är små funktioner som utökas på anropsplatsen istället för att anropas som en separat funktion. Genom att inkludera inline funktionsdefinition i rubrikfilen kan kompilatorn ersätta funktionsanrop med funktionskropp direkt, vilket potentiellt förbättrar prestandan.

## Exempel på HPP-fil

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

## Vilket är formatet på filen HPP?

HPP är en vanlig textfil men följer de allmänna reglerna och syntaxen för programmeringsspråket C++. Här är en uppdelning av det allmänna formatet och strukturen för ".hpp"-filen:

- **Rubrikskydd:** Vanligtvis börjar en ".hpp"-fil med rubrikskydd för att förhindra flera inkluderande av samma fil. Detta uppnås med hjälp av förprocessordirektiv som `#ifndef`, `#define` och `#endif`. Huvudskyddet säkerställer att innehållet i filen endast ingår en gång under kompileringsprocessen.
- **Inkludera uttalanden:** Efter header guards kan du inkludera andra nödvändiga header-filer med "#include"-direktivet. Dessa kan inkludera standardbiblioteksrubriker eller andra anpassade rubriker som krävs av din kod.
- **Deklarationer och definitioner:** Det primära innehållet i ".hpp"-filen är deklarationerna och, i vissa fall, definitioner av klasser, funktioner, konstanter, typalias och andra element. Du kan till exempel deklarera klasser med nyckelordet `class`, funktioner som använder deras returtyp, namn och parameterlista, och konstanter med nyckelordet `const` följt av deras typ och namn.
- **Inline funktionsdefinitioner:** I vissa fall kan du inkludera inline funktionsdefinitioner direkt i ".hpp"-filen. Inline-funktioner definieras vanligtvis inuti klasskroppen, vilket innebär att funktionsdefinitionen ingår tillsammans med dess deklaration. Detta kan göras genom att prefixet funktionsdefinition med nyckelordet `inline`.
- **Namnutrymmesdeklarationer:** Om du använder namnutrymmen i din kod kan du deklarera dem i ".hpp"-filen. Detta görs med hjälp av nyckelordet `namespace` följt av namnutrymmesnamn och omsluter den relevanta koden i namnutrymmesblocket.

## Referenser
* [Rubrikfiler (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

