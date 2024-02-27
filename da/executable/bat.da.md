{
  "date": "2021-06-24",
  "keywords": [
"bat-fil",
"hvad er en bat-fil",
"fil",
"bat fil eksempel",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om BAT filformat og API'er, der kan oprette og åbne BAT filer.",
  "title": "BAT - Batch filformat",
  "linktitle": "BAT",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ba-dat"
}
},
  "lastmod": "2021-06-24"
}

## Hvad er en BAT fil?
En BAT-fil er kendt som en batch-fil, der kører med DOS og alle versioner af Windows, under cmd.exe. Den består af en række linjekommandoer i almindelig tekst, der skal udføres af kommandolinjefortolkeren for at udføre forskellige opgaver, såsom at køre vedligeholdelsesværktøjer i Windows eller starte typiske programmer. En batchfil kan indeholde enhver kommando, der kan accepteres af fortolkeren interaktivt og bruge kodestrukturen, der muliggør betinget forgrening og looping som skrevet i batchfilen.
## BAT filformat
Et BAT-filformat er simpelthen et script indbygget for at automatisere kommandosekvenser, som er gentagne. Udtrykket batch bruges til batchbehandling. Det kan betragtes som ikke-interaktiv eksekvering. Derfor behandler en batchfil muligvis ikke en batch af flere data. I det gamle Disk Operating System (DOS) blev batchfilen kørt under kommandolinjegrænsefladen ved at indtaste filnavnet og filtypenavnet .bat. Det tidligere Microsoft-operativsystem baseret på grafisk interface, såsom Microsoft Windows, var afhængigt af DOS. Brugerne skulle bruge DOS til at udføre typiske operationer som at reparere, optimere eller geninstallere Windows. Senere introducerede Microsoft Windows NT, som ikke var afhængigt af DOS-operativsystemet. Derfor kan batchfilerne køres ved at bruge kommandoprompt eller **cmd.exe** i moderne Microsoft-operativsystemer.
### Batchfilparametre
Kommandoprompten understøtter en række specielle variabler såsom **%0, %1 til %9** for at referere til batchjobbets navn og sti og de ni kaldende parametre fra batchjobbet. Ikke-eksisterende parametre erstattes af en streng med nul-længde. Selvom de kan bruges på samme måde som miljøvariabler, men gemmes ikke i miljøet. Microsoft og IBM omtaler disse variabler som erstatningsparametre, mens Novell, Digital Research og Caldera introducerede begrebet erstatningsvariabler for dem.

Her er nogle nyttige batch-filkommandoer:
| Kommando | Beskrivelse |
------|------------|
| VER | Denne batch-kommando viser den version af MS-DOS, du bruger. |
|ASSOC| Dette er en batch-kommando, der forbinder en udvidelse med en filtype (FTYPE), viser eksisterende tilknytninger eller sletter en tilknytning. |
|CD| Denne batch-kommando hjælper med at foretage ændringer i en anden mappe eller viser den aktuelle mappe. |
|CLS| Denne batch-kommando rydder skærmen. |
|KOPI| Denne batch-kommando bruges til at kopiere filer fra den ene placering til den anden. |
|DEL| Denne batch-kommando sletter filer og ikke mapper. |
|DIR| Denne batch-kommando viser indholdet af en mappe. |
|DATO| Denne batch-kommando hjælper med at finde systemdatoen. |
|EKKO| Denne batch-kommando viser meddelelser eller slår kommandoekko til eller fra. |
|EXIT| Denne batch-kommando afslutter DOS-konsollen. |
|MD| Denne batch-kommando opretter en ny mappe på den aktuelle placering. |
|FLYT| Denne batch-kommando flytter filer eller mapper mellem mapper. |
|STI| Denne batch-kommando viser eller indstiller stivariablen. |
|PAUSE| Denne batch-kommando beder brugeren og venter på, at en linje med input indtastes. |
|SPRING| Denne batch-kommando kan bruges til at ændre eller nulstille cmd.exe-prompten. |
|RD| Denne batch-kommando fjerner mapper, men mapperne skal være tomme, før de kan fjernes. |
|REN| Omdøber filer og mapper |
|REM| Denne batchkommando bruges til bemærkninger i batchfiler, hvilket forhindrer indholdet af bemærkningen i at blive udført. |
|START| Denne batch-kommando starter et program i et nyt vindue eller åbner et dokument. |
|TID| Denne batch-kommando indstiller eller viser tiden. |
|TYPE| Denne batch-kommando udskriver indholdet af en fil eller filer til outputtet. |
|VOL| Denne batch-kommando viser volumenetiketterne. |
|ATTRIB| Viser eller indstiller attributterne for filerne i den aktuelle mappe |
|CHKDSK| Denne batch-kommando tjekker disken for eventuelle problemer. |
|VALG| Denne batch-kommando giver brugeren en liste over muligheder. |
|CMD| Denne batch-kommando påkalder en anden forekomst af kommandoprompt. |
|KOMP| Denne batch-kommando sammenligner 2 filer baseret på filstørrelsen. |
|KONVERT| Denne batch-kommando konverterer en volumen fra FAT16- eller FAT32-filsystem til NTFS-filsystem. |
|DRIVERQUERY| Denne batch-kommando viser alle installerede enhedsdrivere og deres egenskaber. |
|UDVID| Denne batchkommando udtrækker filer fra komprimerede .cab kabinetfiler. |
|FIND| Denne batch-kommando søger efter en streng i filer eller input og udsender matchende linjer. |
|FORMAT| Denne batchkommando formaterer en disk til at bruge Windows-understøttet filsystem såsom FAT, FAT32 eller NTFS, og overskriver derved det tidligere indhold på disken. |
|HJÆLP| Denne batch-kommando viser listen over Windows-leverede kommandoer. |
|IPCONFIG| Denne batch-kommando viser Windows IP-konfiguration. Viser konfiguration efter forbindelse og navnet på den forbindelse. |
|LABEL| Denne batch-kommando tilføjer, indstiller eller fjerner en disketiket. |
|MERE| Denne batch-kommando viser indholdet af en fil eller filer, én skærm ad gangen. |
|NET| Tilbyder forskellige netværkstjenester, afhængigt af den anvendte kommando. |
|PING| Denne batch-kommando sender ICMP/IP ekko-pakker over netværket til den angivne adresse. |
|SLUKNING| Denne batch-kommando lukker en computer ned eller logger den aktuelle bruger af. |
|SORTERING| Denne batch-kommando tager input fra en kildefil og sorterer dens indhold alfabetisk, fra A til Z eller Z til A. Den udskriver outputtet på konsollen. |
|SUBST| Denne batchkommando tildeler et drevbogstav til en lokal mappe, viser aktuelle tildelinger eller fjerner en tildeling. |
|SYSTEMINFO| Denne batch-kommando viser konfigurationen af en computer og dens operativsystem. |
|TASKKILL| Denne batch-kommando afslutter en eller flere opgaver. |
|OPGAVELISTE| Denne batch-kommando viser opgaver, herunder opgavenavn og proces-id (PID). |
|XCOPY| Denne batch-kommando kopierer filer og mapper på en mere avanceret måde. |
|TRÆ| Denne batch-kommando viser et træ med alle undermapper i den aktuelle mappe til et hvilket som helst niveau af rekursion eller dybde. |
|FC |Denne batch-kommando viser de faktiske forskelle mellem to filer. |
|DISKPART |Denne batch-kommando viser og konfigurerer egenskaberne for diskpartitioner. |
|TITLE |Denne batch-kommando indstiller titlen, der vises i konsolvinduet. |
|SET | Viser listen over miljøvariabler på det aktuelle system. |

## Eksempel på BAT-fil
Batch-scripts gemmes normalt som simple tekstfiler; indeholdende kommandoer, der bliver udført i en sekvens. Disse filer gemmes med filtypenavnet .bat; genkendes og udføres ved hjælp af **Command Interpreter** software. Denne software er oprindeligt tilgængelig i Microsoft Windows med navnet **cmd.exe**.

Her er et eksempel på et batchscript, som sletter alle filer i den aktuelle mappe:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Referencer 

* [Batch Script - Quick Guide](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)

* [Batch-fil - af Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


