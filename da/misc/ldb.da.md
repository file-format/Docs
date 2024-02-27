{
  "date": "2023-04-20",
  "keywords": [
"ldb fil",
"hvad er en ldb-fil",
"hvilke oplysninger ldb indeholder",
"hvad er formålet med ldb-fil",
"ldb udvidelse",
"fil",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "LDB-filformat - Microsoft Access Lock-fil",
  "description": "Lær om LDB-format og hvilke oplysninger det indeholder.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb-da",
      "parent": "misc"
}
},
  "lastmod": "2023-04-20"
}

## Hvad er LDB fil?

En LDB-fil er en låsefil, der bruges af Microsoft Access til at forhindre flere brugere i at redigere den samme database samtidigt. Når brugeren åbner en Access-database, opretter Access en tilsvarende LDB-fil i samme mappe som databasen. Denne fil indeholder oplysninger om, hvem der i øjeblikket bruger databasen, og hvilke poster de redigerer.

LDB-filen oprettes automatisk af Microsoft Access, når databasen åbnes, og slettes, når databasen lukkes. Det er vigtigt at bemærke, at LDB-filen aldrig bør slettes manuelt, da dette kan forårsage problemer med databasen.

Hvis du støder på problemer med Microsoft Access-databasen, er en potentiel løsning at prøve at slette LDB-fil, der er knyttet til den database. Dette vil frigive eventuelle låse, der kan forhindre dig i at få adgang til databasen. Sørg dog for at lave en sikkerhedskopi af databasen, før du forsøger dette, da sletning af LDB-filen kan forårsage datatab eller korruption, hvis det gøres forkert.

## LDB-filformat - flere oplysninger

En LDB-fil i Microsoft Access indeholder oplysninger om brugere, der i øjeblikket har adgang til databasen, såsom deres brugernavn, computernavn og login-tid. LDB-filen indeholder også information om eventuelle låse, der er blevet placeret på databasen, såsom hvilke poster, der redigeres af hvilken bruger.

Her er en mere detaljeret liste over de typer information, der kan findes i en LDB-fil:

- **Brugernavn** - navnet på den bruger, der i øjeblikket har adgang til databasen
- **Computernavn** - navnet på den computer, hvorfra brugeren får adgang til databasen
- **Logintid** - det tidspunkt, hvor brugeren første gang åbnede databasen
- **Record locks** - information om hvilke poster, der i øjeblikket redigeres af hvilken bruger
- **Objektlåse** - information om, hvilke databaseobjekter (såsom tabeller, formularer eller rapporter), der i øjeblikket redigeres af hvilken bruger
- **Forbindelsesoplysninger** - oplysninger om, hvordan brugeren er forbundet til databasen (f.eks. om de bruger lokal- eller netværksforbindelse)

Oplysningerne i LDB-filen bruges af Microsoft Access til at forhindre, at flere brugere foretager modstridende ændringer i samme database på samme tid. Når brugeren forsøger at redigere en post eller et objekt, der allerede er låst af en anden bruger, viser Microsoft Access en meddelelse, der angiver, at objektet allerede er i brug. LDB-filen opdateres, når brugere åbner og lukker databasen og foretager ændringer i låste objekter.

## Referencer
* [What is an LDB File?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

