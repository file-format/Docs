{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF-bestandsindeling - Wat is een XFDF-bestand?",
  "description":"Meer informatie over XFDF-bestanden en API's die XFDF-bestanden kunnen maken en openen.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een XFDF-bestand?

Een bestand met de extensie .xfdf is een XML Forms Data Format dat wordt gegenereerd met Adobe Acrobat-software. Net als [FDF](/nl/pdf/fdf/), bevat XFDF de beschrijving van formulierelementen en hun waarden in XML-formaat. Dit kunnen de namen en waarden van tekstvelden in het PDF-formulier zijn. XFDF wordt opgeslagen in een door mensen leesbaar formaat en kan programmatisch worden gelezen met behulp van programmeertalen zoals C#.

## XFDF-bestandsindeling - Meer informatie

XFDF-bestanden worden opgeslagen in XML-bestandsindeling, een universeel formaat dat wordt gebruikt voor het importeren en exporteren van gegevens. Een XFDF-bestandsstructuur bestaat uit een kop, gevolgd door veldwaarden en elementgegevens zoals hieronder weergegeven.

|Element|Attribuut|Inhoud|
---|---|---|
|\<XFDF> ||Bovenste element|
|\<fields> ||Alle veldwaarden voor deze sjabloon|
|<field (T)> |naam |Veldnaam|
|<value (V)> |waarde |Veldwaarde|

## Referenties

* [FDF-formaatondersteuning door Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

