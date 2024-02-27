{
  "date": "2023-06-14",
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om 4DL-filformat og API'er, der kan oprette og åbne 4DL-filer.",
  "title": "4DL - 4th Dimension Database Log File",
  "linktitle": "4DL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-4d-dal"
}
},
  "lastmod": "2023-06-14"
}

## Hvad er en 4DL fil?

En 4DL-logfil bruges til at registrere ændringer foretaget i en 4D-databasefil (.4DD). Denne fil gemmes sammen med databasefilen og deler et lignende filnavn. Dens formål er nøjagtigt at spore og vedligeholde en omfattende registrering af de opdateringer, der er implementeret i databasen. En [4DD file](/database/4dd/), sammenlignet med 4DL-filen, er hovedsageligt forbundet med 4. dimensioner af 4D Inc.

## 4DL filformat - flere oplysninger

Typisk gemmes flere 4DL-filer sammen med en 4DD-fil. Således kan den første version af logfilen blive navngivet som 0001.4dl, men de laterale versioner af logfilerne vil blive gemt som 0002.4dl, 0003.4dl, og så videre. Nu, hvis selve logfilen gennemgår 3 efterfølgende lagringer, vil den blive mærket som db1[0005-0003].4dl.

## Referencer

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
