{
"datum": "2023-03-01",
  "keywords": [
"chipbestand",
"wat is een chipbestand",
"bestand",
"hoe chipbestand openen",
"chip bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CHIP-bestandsindeling - Microarray-annotatiebestand",
  "description":"Leer meer over CHIP-bestandsindelingen en API's waarmee CHIP-bestanden kunnen worden gemaakt en geopend.",
"linktitle": "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip",
"parent" : "spreadsheet"
}
},
"laatste mod": "01-03-2023"
}

## Wat is een CHIP-bestand?

CHIP-bestand is een microarray-annotatiebestand en is gerelateerd aan Gene Set Enrichment Analysis (GSEA) -software. GSEA is een computationele methode die evalueert of een vooraf gedefinieerde reeks genen (een genenset) statistisch significante verschillen vertoont tussen twee biologische toestanden, zoals gezond versus ziek weefsel of met medicijnen behandelde versus onbehandelde cellen. Om GSEA uit te voeren, hebt u een genexpressiedataset en een genensetdatabase nodig. De genensetdatabase bevat informatie over de genen in de genensets, zoals hun functie, route of weefselspecifieke expressie.

Een CHIP-bestand is een specifiek type genensetdatabase dat door GSEA wordt gebruikt. Het bevat informatie over de genen en genensets die relevant zijn voor het microarrayplatform dat in het experiment wordt gebruikt. Het CHIP-bestand biedt annotaties voor elke probe op de microarray, zoals het gensymbool, de gennaam, de genbeschrijving en de chromosomale locatie. Deze informatie wordt gebruikt om de probes te matchen met de genen in de genexpressiedataset en om ze toe te wijzen aan de juiste genensets voor GSEA-analyse.

Om een CHIP-bestand in GSEA te gebruiken, moet u het in de software importeren en aan uw microarray-dataset koppelen. GSEA ondersteunt verschillende microarrayplatforms en biedt voor veel ervan kant-en-klare CHIP-bestanden. U kunt echter ook uw eigen CHIP-bestand maken met annotatiedatabases van externe bronnen, zoals NCBI of Ensembl.

## Meer informatie

Een CHIP-bestand is geen spreadsheet, maar kan worden geopend en bewerkt in een spreadsheetprogramma zoals Microsoft Excel of Google Spreadsheets. Een CHIP-bestand is een type tekstbestand dat door tabs gescheiden gegevens bevat, die eenvoudig in een spreadsheetprogramma kunnen worden geïmporteerd om te bekijken en te bewerken.

In een spreadsheetprogramma kunt u de gegevens in een CHIP-bestand manipuleren om annotaties voor de genen en genensets op de microarray toe te voegen, te verwijderen of te wijzigen. U kunt bijvoorbeeld een spreadsheetprogramma gebruiken om aangepaste annotaties toe te voegen voor de genen die niet zijn opgenomen in het originele CHIP-bestand, of om meerdere CHIP-bestanden uit verschillende bronnen samen te voegen tot één bestand.

Het is echter belangrijk op te merken dat een CHIP-bestand een specifiek formaat en een specifieke structuur heeft die moet worden gehandhaafd voor compatibiliteit met GSEA-software. Als u de inhoud van een CHIP-bestand in een spreadsheetprogramma wijzigt, moet u ervoor zorgen dat de wijzigingen het bestandsformaat of de inhoud niet op een manier wijzigen die de nauwkeurigheid of validiteit van de GSEA-analyse zou kunnen beïnvloeden.

## Hoe open je een CHIP-bestand?

Omdat het CHIP-bestand door tabs gescheiden gegevens bevat, kunt u deze dus openen in Microsoft Excel als u de spreadsheetgegevens wilt bekijken.

## Referenties
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
