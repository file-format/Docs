{
  "date": "2022-07-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "INC filudvidelse - Hvad er en INC fil?",
  "description": "Lær om INC Inkluder filformat og API'er, der kan oprette og åbne INC filer.",
  "linktitle": "INC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-in-dac"
}
},
  "lastmod": "2022-07-14"
}

## Hvad er INC fil?

En INC-fil er en include-fil, der bruges af softwareprogrammets kildekode til at referere til header-information. Det ligner [.h file format](/programming/h/) og indeholder erklæringer, funktioner, overskrifter eller makroer, der kan genbruges af kildekodefiler såsom C++. INC-filer bruges af en række programmeringssprog som C, [C++](/programming/cpp/), Pascal, [PHP](/programming/php/) og [Java](/programming/java/). Teksteditorer som Microsoft Notepad, Notepad++ og TextEdit kan bruges til at åbne INC-filer.

## INC-filformat - flere oplysninger

En INC-fil gemmes som almindelig tekstfil med alle erklæringerne inkluderet i henhold til erklæringens syntaks. En INC-fil kan også referere til andre INC-filer. Når den er oprettet, bliver INC-filen en del af projektet og kan refereres fra kildefiler såsom C++. Det kan refereres til af flere kildefiler for at undgå duplikering.

## INC Filindhold

INC filer kan indeholde følgende oplysninger.

**`Variables`** - I tilfælde af objektorienteret programmering (OOP) indeholder en klasseheader-fil definitioner af alle klasseniveauvariabler, der er tilgængelige på tværs af implementeringskildekodefilerne

**`Methods Declaration`** - Alle metodedeklarationerne er inkluderet i .h header-filerne for at være tilgængelige på tværs af flere implementeringsfiler.

**`Non-inline funktionsdefinitioner`** - Header-filer kan også indeholde definitioner af en ikke-inline-metode.

## Ulempe ved at bruge INC-fil i PHP

PHP er serversidescripts, der kører på serveren og returnerer resultaterne til de kaldende websider. Hvis en PHP-fil refererer til en INC-fil, og serveren ikke er konfigureret til at parse .inc-filer (hvilket er meget almindeligt), kan en bruger se php-kildekoden i .inc-filen ved at besøge URL-mappen. Så man skal være forsigtig, mens man bruger INC-filer som inkluderende filer i PHP.

## Referencer

* [Bruger INC i PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)


