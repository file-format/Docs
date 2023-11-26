{
"datum": "22-06-2023",
  "keywords": [
"rmd",
"rmd-bestand",
"wat is een rmd-bestand",
"hoe maak je een rmd-bestand aan",
"hoe open ik een rmd-bestand",
"bestand",
"rmd bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"RMD-bestandsindeling - R Markdown-bestand",
  "description":"Leer meer over het RMD-formaat en API's waarmee RMD-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"RMD",
  "menu": {
    "docs": {
      "identifier": "word-processing-rmd",
"parent":"tekstverwerking"
}
},
"laatste mod": "22-06-2023"
}

## Wat is een RMD-bestand?

Een R Markdown-bestand (RMD) is een tekstbestand met de extensie ".rmd" dat Markdown-tekst combineert met ingebedde R-codebrokken. Het is een krachtig hulpmiddel voor reproduceerbaar onderzoek en data-analyse, omdat u er verhalende tekst, inclusief code, mee kunt schrijven en dynamische rapporten of documenten kunt genereren. Het bevat YAML-metagegevens, in Markdown opgemaakte platte tekst en stukjes R-code die, wanneer ze worden weergegeven met RStudio, samen een geavanceerd data-analysedocument vormen.

R Markdown-bestanden worden vaak gebruikt in RStudio IDE, maar u kunt er ook in elke teksteditor mee werken. Wanneer u een RMD-bestand rendert, worden stukjes code uitgevoerd en wordt de uitvoer (zoals tabellen, plots of tekst) in het uiteindelijke document ingevoegd. Hierdoor kunt u uw data-analyse en visualisatie naadloos integreren met uw schriftelijke toelichtingen.

## Hoe maak je een RMD-bestand?

Om een RMD-bestand te maken, kunt u elke teksteditor van uw keuze gebruiken. Begin met het openen van een nieuw bestand en sla het op met de extensie ".rmd", wat het R Markdown-formaat aangeeft. De Markdown-syntaxis dient als basis voor het schrijven van de inhoud van een document. Markdown is een lichtgewicht opmaaktaal waarmee u tekst eenvoudig kunt structureren en opmaken. Kopteksten, paragrafen, lijsten, links en afbeeldingen kunnen moeiteloos in uw document worden opgenomen, waardoor de duidelijkheid en leesbaarheid worden gewaarborgd.

Een van de belangrijkste voordelen van R Markdown is de mogelijkheid om R-codefragmenten rechtstreeks in uw document op te nemen. Deze codeblokken, omsloten door drie backticks `(```)` en de letter `"r"` tussen accolades `({ })`, stellen u in staat R-code naadloos te schrijven en uit te voeren. U kunt data-analyses uitvoeren, visualisaties genereren, statistieken berekenen en zelfs interactieve elementen toevoegen. Wanneer u een RMD-bestand rendert, worden stukjes code uitgevoerd en wordt de resulterende uitvoer automatisch ingevoegd in het definitieve document, zodat uw analyse en verhaal volledig geïntegreerd zijn.

Zodra uw RMD-bestand compleet is, kunt u het eenvoudig in verschillende formaten renderen, zoals HTML, PDF of Word. Geïntegreerde ontwikkelomgevingen (IDE's) zoals RStudio bieden een naadloze ervaring met de knop "Knit" die het document weergeeft op basis van uw specificaties. Als alternatief kunt u de functie `rmarkdown::render()` in R gebruiken om het RMD-bestand programmatisch weer te geven.

## Hoe open je een RMD-bestand?

Over het algemeen moet u het RMD-bestand openen in RStudio, omdat het de RMD-syntaxis ondersteunt en daadwerkelijk de code in het RMD-bestand kan uitvoeren. Door het RMD-bestand te openen in een compatibele teksteditor of IDE, kunt u eenvoudig met het bestand werken, de inhoud ervan wijzigen, R-codefragmenten uitvoeren en de gewenste uitvoer of rapporten genereren op basis van ingesloten code en Markdown-tekst.

Als het uw bedoeling is uitsluitend de inhoud van het RMD-bestand te bekijken, kunt u het openen met elke teksteditor.

## Referenties
* [Inleiding tot R Markdown](https://rmarkdown.rstudio.com/articles_intro.html)

