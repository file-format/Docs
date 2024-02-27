{
  "date": "2021-04-22",
  "keywords": [
"aps fil",
"visual studio aps-fil",
"udvidelse",
"format",
"aps fil visual studio",
"aps filtypenavn",
"hvordan man åbner en aps fil",
"APS filformat"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "APS - Visual C++ ressourcefil",
  "description": "Lær om APS-filformat med APS-eksempel og API'er, der kan oprette og åbne APS-filer.",
  "linktitle": "APS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ap-das"
}
},
  "lastmod": "2021-04-22"
}

## Hvad er et APS-filformat?
En APS-fil er oprettet af Visual C++, et softwareudviklingsprogram fra Microsoft. Det gemmer den binære repræsentation af en ressource, der er inkorporeret i projektet, og det giver applikationen mulighed for at indlæse ressourcer hurtigere. Du kan nemt finde disse filer med filtypenavnet .aps. Faktisk læser ressourceeditorerne ikke direkte resource.h-filerne, det er derfor, ressourcekompileren kompilerer dem til .aps-filer, der forbruges af ressourceeditorerne.

## APS filformat
APS-filformatet er kun et kompileringstrin og gemmer kun symbolske data. Den ikke-symbolske information, såsom kommentarer, kasseres under kompileringsprocessen. For eksempel, når du Gem, overskriver ressourceeditoren ressourcescriptfilen og resource.h-filen. Eventuelle ændringer af selve ressourcerne forbliver inkorporeret i ressourcescriptfilen, men kommentarer vil altid gå tabt, når ressourcescriptfilen er overskrevet.


## Referencer

 * [Resource Files (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 

