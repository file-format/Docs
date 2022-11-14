{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "bestand", "extensie", "bestandsformaat", "Mathematica", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over wat een NB-bestand-API's zijn die NB-bestanden kunnen maken en openen.",
  "title" :"NB - Mathematica Notebook-bestandsindeling",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Wat is een NB-bestand?

Een bestand met de extensie .nb is een Wolfram-notebookbestandsindeling die instructies voor wiskundige instructies opslaat in een tekstbestand. Het kan veel verschillende soorten gegevens bevatten, zoals live-berekening, willekeurige dynamische interfaces, volledig getypte invoer, beeldinvoer, automatische codeannotatie, een complete programmatische interface op hoog niveau en duizenden zorgvuldig georganiseerde functies en opties. De tekstuele instructies zijn Mathematica-invoer en -uitvoer die wordt gegenereerd en bijgewerkt wanneer de invoerinstructies in het bestand worden geplaatst.

## Wolfram Notebook NB Bestandsformaat - Meer informatie

Wolfram Notebook NB-bestanden worden opgeslagen in platte tekstindeling, een door mensen leesbare bestandsindeling. De inhoud van een notitieblok is in secties gerangschikt als platte tekst, waarbij elke sectie wordt weergegeven door groepen cellen, vergelijkbaar met een spreadsheet. Het bereik van deze groepen wordt aangegeven door een haakje aan het einde van elke cel. De stijl die aan een cel is toegewezen, bepaalt de rol ervan binnen het notitieblok, zoals hieronder beschreven.

### Notebooks als Wolfram-taal

Als het de bedoeling is om het Notebook op te slaan dat bestaat uit wiskundige instructies voor uitvoering door Wolfram Language Kernal, krijgen de cellen in het document automatisch de tekststijl 'Invoer' toegewezen. Dit vertelt de kernal om deze te beschouwen als instructies die worden uitgevoerd wanneer de gebruiker een combinatie van `Shift+Return`-toetsen uitgeeft. Een Mathematica Notebook ziet eruit zoals in het volgende voorbeeld.

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram Notebook-bestandsindeling" >}}

### Notebooks als documenten

Mathematica Notebooks kunnen in documentformaat zijn om een beeld te geven van wat u ziet, wat is wat u krijgt (WYSIWYG). Deze documenten zijn hetzelfde als weergegeven op het scherm of op een gedrukt papier, en zijn interactief. Hiervoor wordt de `Tekststijl` toegewezen aan de cel om de inhoud weer te geven zonder de instructies van de kernel uit te voeren.

## Mathematica NoteBooks exporteren

Mathematica Notebooks kunnen worden geëxporteerd naar veel verschillende bestandsindelingen, zoals PDF, afbeeldingen, GIS, gecomprimeerd en spreadsheets.

## Referenties

* [Mathematica Notebook Basics](https://reference.wolfram.com/language/guide/NotebookBasics.html)

