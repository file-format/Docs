{
  "date": "2019-10-11",
  "keywords": [
"h",
".hh",
"hvad er en .hh-fil",
"hvordan man åbner .hh fil",
"udvidelse",
"fil",
".hh fil",
".hh filformat",
".hh filtypenavn",
".HH fil eksempel"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HH - C++ Header-filformat",
  "description": "Lær om HH filformat og API'er, der kan oprette og åbne HH fil.",
  "linktitle": "HH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-dah"
}
},
  "lastmod": "2021-06-20"
}

## Hvad er en HH fil?

En fil med filtypenavnet .hh er en C++ header-fil, der inkluderer erklæringen af variabler, konstanter og funktioner. Disse erklæringer bruges af de tilsvarende C++ implementeringsfiler, normalt gemt som [.cpp](/programming/cpp/) filer, der indeholder den faktiske implementering af brugerlogik. Der henvises til .hh-headerfilerne i implementerings-CPP-filerne ved hjælp af `#include`-direktivet. Du kan tilføje så mange som muligt header-filer til dit C++-projekt for at inkludere projektniveaudeklarationer.

## .HH Filformat

En .hh-fil er en almindelig tekstfil, der er oprettet under hensyntagen til reglerne for header-fildefinition. De mest almindelige oplysninger, der er angivet i en .hh-fil, omfatter følgende.

**`Variables`** - I tilfælde af objektorienteret programmering (OOP) indeholder en klasseheader-fil definitioner af alle klasseniveauvariabler, der er tilgængelige på tværs af implementeringskildekodefilerne
**`Methods Declaration`** - Alle metodedeklarationerne er inkluderet i .h header-filerne for at være tilgængelige på tværs af flere implementeringsfiler.
**`Non-inline funktionsdefinitioner`** - Header-filer kan også indeholde definitioner af en ikke-inline-metode.
**`Message Maps`** - En header-fil kan også indeholde meddelelseskort i tilfælde af en MFC-kildekodeimplementering. I sådanne tilfælde er meddelelseskortene knyttet til funktionalitetsimplementeringen, som er knyttet til UI-elementer såsom knap, afkrydsningsfelt, radioknapper osv.

## Forskellen mellem .H og .HH filer

Tilsyneladende er der ingen sådan forskel mellem .h- og .hh-header-filerne udover den anbefalede måde at bruge disse på til respektive sprog, dvs. [C](/programming/c/) eller C++. At navngive dine header-filer i henhold til disse sprog hjælper dig med at skelne mellem disse i et stort projekt, der kan være en blanding af C- og C++-implementeringer.

Derudover, hvis overskrifterne er adskilt af forlængelse, kan din editor anvende den passende formatering automatisk for hhv.

Samlet set vil differentieringen af disse to filformater ikke gøre nogen skade, men vil være fordelagtig og opfordres til at følge for C og C++ skelnen.

### Hovedbeskyttere

Header-filer kan føre til komplekse fejl, hvor flere erklæringer er inkluderet i den samme fil som et resultat af tilføjelse af andre header-filer. Disse dublerede definitioner rejser compilerfejl. Denne problematiske situation kan undgås via en mekanisme kaldet header guard, som er betingede kompileringsdirektiver som vist nedenfor.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Med denne header kontrollerer præprocessoren om `ANY_UNIQUE_NAME_HERE_HPP` allerede er defineret. Hvis headeren gentagne gange inkluderes i den samme fil, vil indholdet af headeren blive ignoreret.

## Referencer

* [Header Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

* [Forskellen mellem .h og .hh filformater](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)


