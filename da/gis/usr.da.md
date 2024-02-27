{
  "date": "2023-08-03",
  "keywords": [
"usr",
"usr fil",
"hvad er en usr-fil",
"hvordan man åbner en usr fil",
"fil",
"usr filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "USR-filformat - Lowrance GPS-datafil",
  "description": "Lær om USR-format og API'er, der kan oprette og åbne USR-filer.",
  "linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr-da",
      "parent": "gis"
}
},
  "lastmod": "2023-08-03"
}

## Hvad er USR fil?

Filtypen .usr er også relateret til Lowrance GPS-enheder. Det bruges især til lagring af GPS-data i et format kendt som User Data Format (USR-format), som bruges af Lowrance GPS-enheder.

Når du bruger en Lowrance GPS-enhed, kan du gemme dine waypoints, spor og ruter som .usr-filer. Disse filer indeholder typisk information såsom breddegrad, længdegrad, højde, tidsstempel og andre data relateret til dine GPS-aktiviteter.

Her er nogle almindelige anvendelser af .usr-filer med Lowrance GPS-enheder:

- **Waypoints:** Waypoints er specifikke placeringer markeret på GPS'en, såsom vartegn, foretrukne fiskesteder eller interessepunkter. Du kan gemme disse placeringer som .usr-filer, og de kan importeres, eksporteres eller deles med andre Lowrance GPS-brugere.

- **Spor:** Spor repræsenterer den registrerede sti for dine GPS-bevægelser. Du kan gemme dine sporlogfiler som .usr-filer, så du kan gennemgå og analysere dine ruter senere eller dele dem med andre.

- **Ruter:** Ruter er foruddefinerede stier, som du kan oprette og gemme på din GPS-enhed. Disse ruter kan også gemmes som .usr-filer til fremtidig brug eller deling.

For at administrere .usr-filer på din Lowrance GPS-enhed bruger du typisk software som Lowrances Insight Planner eller Lowrance GPS Utility til at importere, eksportere og manipulere dine GPS-data.

## USR-filformat - flere oplysninger

I Lowrance iFinder GPS-enheder oprettes .usr-filerne og gemmes på det MultiMediaCard (MMC)-hukommelseskort, der er indsat i enheden. Disse filer indeholder brugerdata såsom waypoints, spor og ruter.

For at overføre .usr-filerne fra MMC'en til en computer kan du følge disse trin:

- **Fjern MMC:** Fjern forsigtigt MultiMediaCard (MMC) fra Lowrance iFinder GPS-enheden.

- **Indsæt MMC i computeren:** Brug en passende MMC-kortlæser til at indsætte hukommelseskortet i computerens kortlæserstik.

- **Find .usr-filer:** Når MMC'en er genkendt af din computer, bør du være i stand til at få adgang til de filer, der er gemt på den. Se efter .usr-filerne, som indeholder dine GPS-data.

- **Konvertering med GPSBabel:** For at konvertere .usr-filerne til et andet GPS-format kan du bruge GPSBabel, som er et gratis og open source-værktøj til at arbejde med forskellige GPS-filformater. GPSBabel understøtter en lang række input- og outputformater, så du kan konvertere .usr-filerne til formater, der er kompatible med anden GPS-software eller -enheder.

Du kan downloade GPSBabel fra det officielle websted (http://www.gpsbabel.org/) og installere det på din computer. Når den er installeret, kan du bruge softwarens kommandolinjegrænseflade eller grafiske brugergrænseflade (hvis tilgængelig) til at udføre konverteringen.

For eksempel, hvis du vil konvertere .usr-filer til GPX-format, kan du bruge en kommando som:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Ovenstående kommando instruerer GPSBabel om at læse inputfilen input.usr i Lowrance USR-format og skrive outputfilen output.gpx i GPX-format.

- **Import af/brug af konverterede filer:** Efter konverteringen vil du have dine GPS-data i det nye format (f.eks. GPX), som du kan bruge med anden GPS-software eller -enheder, der understøtter dette format.

## Hvordan åbner jeg filen USR?

Programmer, der åbner eller refererer til USR filer inkluderer

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Referencer
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)


