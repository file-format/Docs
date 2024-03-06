{
  "date": "2021-08-29",
  "keywords": [
"ade",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Microsoft Access"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par ADE failu formātu un API, kas var izveidot un atvērt ADE failus.",
  "title": "ADE — piekļuve projekta paplašinājuma failam",
  "linktitle": "ADE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ad-lve"
}
},
  "lastmod": "2021-08-29"
}

## Kas ir ADE fails?

Fails ar paplašinājumu .ade ir Microsoft Access Project fails, kas satur Microsoft Access ADP projekta failā ietvertās informācijas apkopoto izvadi. Informācija Access projekta failā, kas nav Visual Basic for Applications (VBA), ir pieejama apkopotā veidā ADE failos. Dati šajos failos tiek glabāti saspiestā formātā, lai samazinātu faila lielumu un uzlabotu Access veiktspēju. Tā kā ADE ir apkopotā Access projekta faila izvade, jebkurš VBA pirmkods, kas ir daļa no projekta, paliek aizsargāts, neļaujot tam būt daļai no izvades. ADE failus var atvērt programmā Microsoft Access 365.

## ADE faila formāts — vairāk informācijas

ADE ir apkopoti Access datu bāzes faili, kas tiek saglabāti diskā kā bināri faili. Šo failu iekšējā failu struktūra nav zināma.

The ADE files can create issues in opening based on the version of Microsoft Access that has been used to create these files. Access databases that are using the 64-bit version of Microsoft Access 2010 and that are compiled as MDE, [ACCDE](/database/accde/), or ADE files have to be recompiled in Microsoft Access 2021 Service Pack 1 (SP1) to work correctly with Access 2010 SP1. Šī problēma rodas, jo Access 2010 SP1 izmanto jaunāku faila VBE7.dll versiju (versija 7.00.1619).

## Atsauces

* [Problēma ar Access ADE failiem](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)

* [Kādus piekļuves failu formātus izmantot](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)


