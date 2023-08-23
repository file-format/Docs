{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Elixir-rapportsjabloonbestand",
  "description":"Meer informatie over RML-bestanden en API's die RML-bestanden kunnen maken en openen.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Wat is een RML-bestand?

Een RML-bestand is een rapportagesjabloonbestand met de rapportage-engine [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Het sjabloonbestand wordt gebruikt om rapporten te genereren met de gegevensbron die is verbonden met het Elixir FileSystem. Gegevens worden gelezen en ingevuld in het RML-sjabloonbestand en kunnen worden geëxporteerd naar een aantal verschillende bestandsindelingen zoals [PDF](/nl/pdf/), [RTF](/nl/word-processing/rtf/) en spreadsheet [XLS](/nl/spreadsheet/xls/). Elixir Repertoire-rapportage-engine kan worden aangesloten op een breed scala aan JDBC-gegevensbronnen.

## RML-bestandsindeling

De details van de interne bestandsstructuur van het RML-bestandsformaat zijn niet openbaar beschikbaar. De bestanden worden intern gegenereerd en opgeslagen door de Elixir Repertoire-toepassing om rapporten te genereren met gegevens die zijn ingevuld vanuit de aangesloten gegevensbronnen. Het RML-sjabloonbestand bevat de algemene lay-out en tijdelijke aanduidingen van het eindrapport dat op basis van de gegevens moet worden gegenereerd.

## Hoe een RML-sjabloonbestand te maken?

Om een RML-sjabloon in Elixir Repertoire te genereren, kunnen de volgende stappen worden gevolgd.

1. Sluit een JDBC-gegevensbron aan op het bestandssysteem.
1. Start de wizard Rapportsjabloon
1. Gebruik de software om het .ds-bestand van de gegevensbron te lokaliseren
1. Kies tabelrapport als exportkeuze
1. Selecteer de velden die in het rapportsjabloon moeten worden opgenomen
1. Ten slotte, door op de knop Voltooien te klikken, wordt First report.rml toegevoegd aan de repository en geopend om het tabblad Lay-out weer te geven.

## Referenties

* [Elixir-repertoire](https://elixirtech.com/repertoire-2/)

