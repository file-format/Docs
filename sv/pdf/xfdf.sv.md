{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF-filformat - Vad är en XFDF-fil?",
  "description":"Läs mer om XFDF-filer och API:er som kan skapa och öppna XFDF-filer.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en XFDF fil?

En fil med filtillägget .xfdf är ett XML Forms Data Format som genereras med Adobe Acrobat. Precis som [FDF](/sv/pdf/fdf/), innehåller XFDF beskrivning av formulärelement och deras värden i XML-format. Detta kan inkludera namn och värden för textfält i PDF-formuläret. XFDF sparas i mänskligt läsbart format och kan läsas programmässigt läsas med hjälp av programmeringsspråk som C#.

## XFDF-filformat - Mer information

XFDF-filer sparas i XML-filformat som är ett universellt format som används för import och export av data. En XFDF-filstruktur består av en rubrik, följt av fältvärden, och elementdata som visas nedan.

|Element|Attribut|Innehåll|
---|---|---|
|\<XFDF> ||Översta elementet|
|\<fields> ||Alla fältvärden för denna mall|
|<field (T)> |namn |Fältnamn|
|<value (V)> |värde |Fältvärde|

## Referenser

* [FDF Format Support by Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

