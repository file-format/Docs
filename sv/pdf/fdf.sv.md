{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FDF-filformat - Vad är en FDF-fil?",
  "description":"Läs mer om FDF-filformat och API:er som kan skapa och öppna FDF-filer.",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en FDF fil?

En FDF-fil (**Forms Data Format**) är ett textdokument som genereras genom att exportera data från formulärfälten i en [PDF](/sv/pdf/)-fil. Den innehåller endast textfältdata som extraheras från formulärfälten som är tillgängliga i en PDF-fil. Detta resulterar i en jämförelsevis liten datafil eftersom den exporterade informationen inte innehåller själva formuläret. Adobe Acrobat tillhandahåller funktionen att exportera formulärfältdata genom att använda alternativet "Exportera formulärdata" från programmenyn.

## FDF-filformat - Mer information

FDF är vanligt textformat och ingår som en del av [ISO 32000-standarden](https://www.iso.org/standard/51502.html) för Portable Document Format. Det utvecklades av Adobe för att tillåta import och export av data från Acrobat Forms eller AcroForms.

Det finns två typer av FDF-filer:

• `Klassisk FDF` – Den tillhandahåller data för att fylla i ett befintligt statiskt formulär.

• `Mall FDF` – Konstruerar en ny PDF baserad på mallar inifrån specificerade PDF-filer. Blanketter i det nya dokumentet fylls i genom att tillhandahålla data.

## Skapa FDF med Adobe Acrobat

[FDF-verktygslådan](https://opensource.adobe.com/dc-acrobat-sdk-docs/) från Adobe låter dig skapa FDF-filer från textdata.

## Referenser ##

* [FDF Format Support by Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

