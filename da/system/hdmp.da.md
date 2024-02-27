{
  "date": "2022-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDMP-fil - Windows Heap Dump-filformat",
  "description": "Lær om HDMP-filformater og API'er, der kan oprette og åbne HDMP-filer.",
  "linktitle": "HDMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-hdm-dap"
}
},
  "lastmod": "2022-08-19"
}

## Hvad er en HDMP fil?

HDMP-fil er et ukomprimeret hukommelsesdump, når et program eller program går ned på grund af en fejl. Det er kun oprettet af Windows XP/Vista og indeholder et dump af programmets status, da det gik ned. Da de er ukomprimerede, tager HDMP-filerne mere plads på disken sammenlignet med Minidump [MDMP](/system/mdmp/)-filerne, der er komprimeret til rapporteringsformål.

Programmer, der kan bruges til at **åbne** eller analysere HDMP-filer, omfatter Microsoft Visual Studio med fejlfindingsværktøjer til Windows.

## HDMP filformat

HDMP-filer gemmes på disken som binære filer og giver ingen fordele, hvis de åbnes uden passende programmer. Disse indeholder relevante systemdata, der er registreret, da fejlen opstod.

### Forskel mellem HDMP og MDMP filformater

HDMP er ukomprimerede hukommelsesdumpfiler. I modsætning hertil er MDMP minidumpfiler, der komprimeres for at reducere filstørrelsen og sendes til Microsoft for at rapportere problemet.

## Reference ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


