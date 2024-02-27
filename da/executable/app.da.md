{
  "date": "2023-02-02",
  "keywords": [
"app-fil",
"hvad er en app-fil",
"fil",
"hvordan man åbner en app-fil",
"app filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om APP-filformat og API'er, der kan oprette og åbne APP-filer.",
  "title": "APP-filformat - macOS-applikationspakke",
  "linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app-da",
      "parent": "executable"
}
},
  "lastmod": "2023-02-02"
}

## Hvad er en APP fil?

En .app-fil på macOS er en speciel type mappe, der indeholder alle de filer, der er nødvendige for at køre et specifikt program, inklusive den eksekverbare kode, ressourcer og metadata. .app-udvidelsen signalerer til operativsystemet, at denne mappe skal behandles som en enkelt enhed, snarere end en samling af separate filer, og at den kan startes direkte fra Finder eller Dock.

Finder er standard filhåndteringsapplikation på macOS. Det giver dig mulighed for at gennemse og organisere filerne og mapperne på din computer. Dock er en funktion i macOS, der giver hurtig adgang til ofte brugte programmer og dokumenter. Både Finder og Dock giver dig mulighed for at starte applikationer ved at klikke på deres .app-filer, som åbner den tilsvarende applikationspakke. Når du starter en applikation, køres den eksekverbare kode i .app-pakken, hvilket gør applikationen tilgængelig til brug. .app-filen er repræsentationen af applikationen på filsystemet og giver brugeren mulighed for at få adgang til og starte applikationen.

Når du højreklikker på en .app-fil i Finder på et macOS-system og vælger Vis pakkeindhold, vil du kunne se den interne struktur af applikationspakken. Dette er nyttigt, hvis du vil have adgang til ressourcer eller filer, der bruges af programmet, eller hvis du vil inspicere indholdet af programmet med henblik på fejlfinding. Pakkeindholdet i en .app-fil inkluderer typisk mapper til ressourcer såsom billeder og lyde, samt den eksekverbare kode til applikationen. Ved at udforske indholdet af en .app-fil kan du få dybere indsigt i, hvordan applikationen er sat sammen, og hvad den gør.

## Hvordan åbner jeg filen APP?

For at åbne en .app-fil på macOS skal du blot dobbeltklikke på filen i Finder. Dette vil starte applikationen i .app-pakken. Hvis applikationen er installeret på dit system og har været knyttet til .app-filtypen, bør applikationen startes automatisk ved at dobbeltklikke på filen. Hvis applikationen ikke er knyttet til .app-filtypen, skal du muligvis højreklikke på filen og vælge Åbn med for at vælge et passende program at åbne den med.

Du kan åbne en .app-fil på terminalen i macOS ved at bruge kommandoen åbn. For at gøre dette skal du navigere til den mappe, hvor .app-filen er placeret ved hjælp af cd-kommandoen, og derefter køre følgende kommando:

```
open <AppName>.app 
```

hvor<AppName> er navnet på den applikation, du vil starte. Dette vil starte programmet, som om du havde dobbeltklikket på det i Finder. Kommandoen åbn er et værktøj til generelle formål, der kan bruges til at åbne mange forskellige typer filer, herunder programmer, dokumenter og mapper. Når du bruger kommandoen åbn på en .app-fil, starter den applikationen i pakken.

## Referencer
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
