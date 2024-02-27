{
  "date" : "2021-06-29",
  "keywords" : [ "XAR", "file", "extension", "file format", "Excel Auto-Recovery File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om XAR-filformat og API'er, der kan oprette og åbne XAR-filer.",
  "title" : "XAR - Microsoft Excel Auto-Recovery File Format",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
      "identifier": "spreadsheet-xar-da",
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-06-29"
}

## Hvad er en XAR fil?

En fil med filtypen .xar er en Microsoft Excel Recvoery-fil, der genereres sammen med de vigtigste Excel-regnearksfiler. Den bruges som en gendannelsesfil, hvis applikationen fejler eller lukker uventet, hvilket resulterer i tab af data fra hovedfilen. Disse gendannelsesfiler gemmes i det samme originale filformat for hastighed og enkelhed. Excel foreslår det originale filformat og navn ved genåbning af den gendannede fil, som den gemmer i systemregistret til gendannelse.

## XAR filformat

XAR-filerne er gendannelsesfiler, der er gemt i binært filformat på disken sammen med excel-hovedfilen. Disse er gemt som skjulte filer på disk med vilkårlige navne, der linker til den primære excel-fil fra systemregistret. Alle åbne filer gemmes aktivt og periodisk i standardudvidelsen som skjulte XAR-filer, og disse gemmes på diske med navne som ~ar8EF9.xar.

## Sådan gendannes Excel-fil fra XAR-fil?

XAR-filer kan gemme alle typer Excel-filformater såsom XLS, XLSX og andre. Hvis din Excel-regnearksfil lukker uventet, kan du åbne Excel eller dobbeltklikke på din fil, og den vil automatisk bede dig om at gendanne fra den gemte gendannelsesfil, som du kan gemme med det samme filnavn som originalen til sideværts brug.

## Referencer

* [Atuo-gendannelsesfunktioner i Excel](https://learn.microsoft.com/en-us/office/troubleshoot/excel/autorecover-functions-in-excel)

* [XAR File Community Hjælp](https://answers.microsoft.com/en-us/msoffice/forum/msoffice_excel-mso_win10-mso_365hp/2016-excel-xar-files/5af5e10c-027a-4c24-a403-39e8f5)


