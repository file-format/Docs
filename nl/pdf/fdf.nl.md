{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FDF-bestandsindeling - Wat is een FDF-bestand?",
  "description":"Meer informatie over FDF-bestandsindelingen en API's die FDF-bestanden kunnen maken en openen.",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een FDF-bestand?

Een FDF-bestand (**Forms Data Format**) is een tekstdocument dat wordt gegenereerd door gegevens uit de formuliervelden van een [PDF](/nl/pdf/)-bestand te exporteren. Het bevat alleen tekstveldgegevens die zijn geëxtraheerd uit de formuliervelden die beschikbaar zijn in een PDF-bestand. Dit resulteert in een relatief klein gegevensbestand omdat de geëxporteerde gegevens het formulier zelf niet bevatten. Adobe Acrobat biedt de mogelijkheid om formulierveldgegevens te exporteren met behulp van de optie `Formuliergegevens exporteren` in het toepassingsmenu.

## FDF-bestandsindeling - Meer informatie

FDF is een platte tekstindeling en maakt deel uit van de [ISO 32000-standaard](https://www.iso.org/standard/51502.html) voor Portable Document Format. Het is ontwikkeld door Adobe om het importeren en exporteren van gegevens uit Acrobat Forms of AcroForms mogelijk te maken.

Er zijn twee soorten FDF-bestanden:

• `Klassieke FDF` – Het levert gegevens om een bestaand statisch formulier in te vullen.

• `Template FDF` – Maakt een nieuwe PDF op basis van sjablonen uit gespecificeerde PDF-bestanden. Formulieren in het nieuwe document worden ingevuld door gegevens aan te leveren.

## FDF maken met Adobe Acrobat

Met de [FDF-toolkit](https://opensource.adobe.com/dc-acrobat-sdk-docs/) van Adobe kunt u FDF-bestanden maken van tekstgegevens.

## Referenties ##

* [FDF-formaatondersteuning door Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

