{
  "date": "2021-08-29",
  "keywords": [
"ade",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Microsoft Access"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om ADE-filformat og API'er, der kan oprette og åbne ADE-filer.",
  "title": "ADE - Få adgang til projektudvidelsesfil",
  "linktitle": "ADE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ad-dae"
}
},
  "lastmod": "2021-08-29"
}

## Hvad er en ADE fil?

En fil med filtypenavnet .ade er en Microsoft Access Project-fil, der indeholder det kompilerede output af oplysningerne i Microsoft Access ADP-projektfilen. Oplysninger i Access-projektfilen, bortset fra Visual Basic for Applications (VBA), er tilgængelig i kompileret form i ADE-filer. Data gemmes i komprimeret format i disse filer for at reducere filstørrelsen og forbedre ydeevnen i Access. Da ADE er det kompilerede output af Access-projektfilen, forbliver enhver VBA-kildekode, som er en del af projektet, beskyttet ved ikke at tillade den at være en del af outputtet. ADE-filer kan åbnes i Microsoft Access 365.

## ADE-filformat - flere oplysninger

ADE er kompilerede Access Database-filer, der gemmes på disken som binære filer. Den interne filstruktur af disse filer kendes ikke.

The ADE files can create issues in opening based on the version of Microsoft Access that has been used to create these files. Access databases that are using the 64-bit version of Microsoft Access 2010 and that are compiled as MDE, [ACCDE](/database/accde/), or ADE files have to be recompiled in Microsoft Access 2021 Service Pack 1 (SP1) to work correctly with Access 2010 SP1. Dette problem opstår, fordi Access 2010 SP1 bruger en nyere version af filen VBE7.dll (version 7.00.1619).

## Referencer

* [Problem med Access ADE Files](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)

* [Hvilke adgangsfilformater der skal bruges](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)


