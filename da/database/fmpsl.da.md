{
  "date": "2022-05-25",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om FMPSL filformat og API'er, der kan oprette og åbne FMPSL filer.",
  "title": "FMPSL-filformat - FileMaker Pro 12 Snapshot Link-fil",
  "linktitle": "FMPSL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-fmps-dal"
}
},
  "lastmod": "2022-05-25"
}

## Hvad er en FMPSL fil?

An FMPSL file is a snapshot file of database created with FileMaker Pro 12. Den gemmer de forespurgte resultater fra databasen sammen med andre oplysninger såsom visuelt layout og synlig information. FMPSL-filen kan bruges til at gendanne alle disse data i en anden forekomst af FileMaker Pro-databasen. Dette filformat blev introduceret med lanceringen af FileMaker Pro v 12. Før denne version blev snapshot-linkene introduceret som FPSL-filformat i FileMaker Pro v 11. FMPSL-filer kan åbnes med FileMaker Pro Advanced-softwaren. Andre filformater, der understøttes af FileMaker Pro, omfatter [FP5](/database/fp5/), [FP7](/database/fp7/) og [FMP12](/database/fmp12/).

## FMPSL filformat

De interne filformatdetaljer for FMPSL-filer er ikke offentligt tilgængelige til udviklerens reference.

### Hvordan gemmer man poster som FMPSL-fil?

Data fra FileMaker Pro-databasen kan gemmes som snapshot-linkfil ved at bruge følgende trin.

 1. Søg i de poster fra databasen, der skal gemmes som en snapshot-linkfil.
 1. Brug indstillingen Send Record As Snapshot Link fra menuen, og gem filen ved at indtaste et filnavn.
 1. Brug de poster, der gennemses, for at gemme hele det fundne sæt af poster.

Den genererede snapshot-fil vil blive gemt på disken med det angivne navn.

## Referencer

 * [Konverter tidligere versioner af FileMaker Pro-filformater til FMP12-filformat](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
 * [Gem poster som en snapshot-linkfil](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

