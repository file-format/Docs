{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Bestand", "Extensie", "Bestandsindeling", "Bestandsextensie", "JSON", "Archiefbestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - HTTP-archiefbestandsindeling",
  "description" :"Uw gids voor bestandsindelingen om te leren wat een HAR-bestand is en API's die een HAR-bestand kunnen maken en openen.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Wat is een HAR-bestand?

Een bestand met .har (HTTP Archive)-bestand is een HTTP-archiefbestand waarin sessiegegevens worden opgeslagen die via veel browsers (zoals Chrome, Safari, IE, Firefox, enz.) worden overgedragen in [JSON](/nl/web/json/) bestandsformaat. De gegevens die via internet worden overgedragen tussen de server en de client (in dit geval de browser van de gebruiker) bevatten HTTP-verzoek- en antwoordheaders die zijn opgeslagen in het HAR-bestand. Het bevat verder gedetailleerde informatie over prestatiegegevens over webpagina's die in de browser zijn geladen. HAR-bestanden kunnen worden geopend in elke teksteditor, zoals Kladblok op Microsoft Windows OS en TextEdit op Apple MacOS.

## HAR-bestandsindeling - Meer informatie

HAR-bestanden slaan sessie-informatie op in platte tekstbestanden met behulp van het populaire JSON-formaat. De specificaties voor het HAR-bestandsformaat zijn opgesteld door de Web Performance Group van het World Web Consortium (W3C) maar konden niet worden gepubliceerd. Het heeft echter met succes een archiefindeling voor HTTP-transacties gedefinieerd.

Naast het bewaken van de overdracht van verzoek- en antwoordinformatie, worden HAR-bestanden door ontwikkelaars gebruikt om de prestaties van de webbrowser te loggen in termen van laadsnelheid van pagina's, laadduur van inhoud, geladen inhoud, uitgevoerde query's om het antwoord van de browser te krijgen en vele andere .

## Waarom HAR-bestanden gebruiken?

HAR-bestanden kunnen nuttig zijn bij het verbeteren van de prestaties van een website door lange laadtijden, paginaweergavetijden en reactietijden te evalueren. HAR-bestanden kunnen worden geanalyseerd om dergelijke problemen te vinden en eventuele problemen met de website op te lossen om de prestaties te verbeteren.

## Hoe een HAR-bestand te genereren?

Dus, hoe een HAR-bestand te genereren? Welnu, dit hangt af van het type browser dat u gebruikt om een HAR-bestand te genereren. In deze handleiding geven we de stappen voor de Google Chrome-browser weer. Methoden voor het genereren van HAR-bestanden met Safari, Firefox, enz. kunnen eenvoudig op internet worden gezocht en gevolgd.

### Stappen om een HAR-bestand te genereren met Google Chrome

De volgende stappen kunnen worden uitgevoerd op een webpagina waar problemen worden ondervonden.

1. Open de webpagina in Google Chrome waar het probleem zich voordeed.
1. Open de ontwikkelaarstool (element inspecteren).
1. Ga naar de linkerkant van het paneel om de bestandsopname te starten. Er is een kleine ronde rode knop in dit gedeelte.
1. Klik op het pictogram om alle logboekrecords die in de browser zijn bewaard, te verwijderen.
1. Om de gewenste inhoud op te slaan zoals hierboven weergegeven, klikt u met de rechtermuisknop en klikt u op "Opslaan als HAR-bestand"

## Referenties

* [HAR-bestandsindeling - Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))

