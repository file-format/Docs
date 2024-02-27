{
   "date":"2023-09-21",
   "keywords":[
"ips",
"ips fil",
"ips intern patching system patch-fil",
"hvad er en ips fil",
"hvordan man åbner en ips fil",
"ips filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"IPS-filformat - Intern patching-system-patchfil",
   "description":"Lær om IPS Internal Patching System Patch-filformat og API'er, der kan oprette og åbne IPS-filer.",
   "linktitle":"IPS",
   "menu":{
      "docs":{
         "identifier":"game-ips-da",
         "parent":"game"
}
},
   "lastmod":"2023-09-21"
}

## Hvad er en IPS fil?

En IPS-fil refererer typisk til en Internal Patching System Patch File. IPS er en forkortelse for International Patching System, og det er et filformat, der bruges til at oprette og anvende patches til ROM-filer (Read-Only Memory), ofte i forbindelse med videospilsemulering og ROM-hacking.

Sådan fungerer det:

- **Original ROM:** Du starter med en original ROM-fil, som i det væsentlige er en kopi af et videospil eller software gemt i et ROM-format. Denne fil er typisk skrivebeskyttet, hvilket betyder, at du ikke kan ændre den direkte.

- **IPS-patchfil:** En IPS-patchfil indeholder de ændringer, du vil anvende på den originale ROM. Disse ændringer kan være fejlrettelser, oversættelser eller andre ændringer.

- **Patch-applikation:** For at anvende ændringerne skal du bruge et hjælpeprogram eller et program, der kan læse IPS-patchfilen og anvende den på den originale ROM. Denne proces retter i det væsentlige den originale ROM-fil med de ændringer, der er angivet i IPS-filen, hvilket skaber en modificeret ROM-fil.

- **Modificeret ROM:** Resultatet er en modificeret ROM, der inkorporerer ændringerne fra IPS-patchfilen. Denne modificerede ROM kan derefter bruges i en emulator eller på kompatibel hardware til at spille spillet med de ønskede modifikationer.

Disse patches bruges typisk til at lave ændringer eller forbedringer af spil, og de kan omfatte forskellige ændringer, herunder ændringer af grafik, modeller og andre spildata. IPS-filer er særligt velegnede til relativt små patches, typisk mindre end 16 megabyte i størrelse.

I det følgende afsnit vil vi udforske de softwareprogrammer, der er forbundet med IPS-filer.

## Lunar IPS

Lunar IPS er et populært og brugervenligt værktøj, der bruges til at oprette og anvende IPS (Internal Patching System) patches til ROM-filer. Her er nogle nøglefunktioner og oplysninger om Lunar IPS:

- **Oprettelse af patch:** Lunar IPS giver brugere mulighed for at oprette IPS-patches ved at angive de ændringer, de vil foretage i en original ROM-fil. Du kan vælge den originale ROM og den ændrede version, og Lunar IPS vil generere en IPS patch-fil baseret på forskellene mellem de to filer.

- **Patch-applikation:** Når du har en IPS-patch-fil, lader Lunar IPS dig anvende den på en original ROM. Denne proces retter i det væsentlige ROM'en med de ændringer, der er angivet i IPS-filen, hvilket skaber en modificeret ROM.

- **Letvægt:** Lunar IPS er et lille og let program, hvilket betyder, at det ikke bruger mange systemressourcer og er hurtigt at downloade og køre.

## IPSWin

IPSWin er et værktøj primært designet til Windows-brugere, der letter oprettelsen og anvendelsen af IPS (Internal Patching System) patches til ROM-filer. Det er et ligetil og brugervenligt værktøj, velegnet til dem, der ønsker at patche ROM'er nemt. Her er nogle oplysninger om IPSWin:

- **Oprettelse af patch:** IPSWin giver brugerne mulighed for at oprette IPS-patches ved at sammenligne to ROM-filer: den originale ROM og den modificerede ROM. Den identificerer forskellene mellem de to filer og genererer en IPS-patch-fil, der indeholder disse ændringer.

- **Patch Application:** Dette værktøj gør det også muligt for brugere at anvende eksisterende IPS patch-filer til originale ROM'er. Ved at vælge den passende IPS-patch og den originale ROM, vil IPSWin flette ændringerne til en ny ROM-fil og skabe en patchet version.

## Hvordan åbner jeg filen IPS?

Programmer, der åbner IPS filer inkluderer

- Lunar IPS
- IPSWin
- MultiPatch

## Andre IPS-filer

Her er andre filtyper, der bruger filtypen **.ips**.

- [IPS - PlayStation 2 In-Game Video](/game/ips-ps2/)
- [IPS - iOS Analytics Data](/misc/ips/)

## Referencer
* [Lunar IPS](https://www.romhacking.net/utilities/240/)
