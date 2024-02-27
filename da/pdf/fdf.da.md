{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FDF-filformat - Hvad er en FDF-fil?",
  "description": "Lær om FDF-filformat og API'er, der kan oprette og åbne FDF-filer.",
  "linktitle": "FDF",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-fd-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en FDF fil?

En FDF-fil (**Forms Data Format**) er et tekstdokument, der genereres ved at eksportere data fra formularfelterne i en [PDF](/pdf/)-fil. Det inkluderer kun tekstfeltdata, der er udtrukket fra formularfelterne, der er tilgængelige i en PDF-fil. Dette resulterer i en forholdsvis lille datafil, da de eksporterede data ikke indeholder selve formularen. Adobe Acrobat tilbyder funktionen til at eksportere formularfeltdata ved at bruge muligheden for Eksporter formulardata fra programmenuen.

## FDF-filformat - flere oplysninger

FDF er almindeligt tekstformat og er inkluderet som en del af [ISO 32000 standard](https://www.iso.org/standard/51502.html) for Portable Document Format. Det blev udviklet af Adobe for at tillade import og eksport af data fra Acrobat Forms eller AcroForms.

Der er to typer FDF-filer:

• `Klassisk FDF` – Det giver data til at udfylde en eksisterende statisk formular.

• `Skabelon FDF` – Konstruerer en ny PDF baseret på skabeloner inde fra specificerede PDF-filer. Formularer i det nye dokument udfyldes ved at levere data.

## Oprettelse af FDF ved hjælp af Adobe Acrobat

The [FDF toolkit](https://opensource.adobe.com/dc-acrobat-sdk-docs/) from Adobe lets you create FDF files from text data.

## Referencer

* [FDF Format Support by Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)

* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

