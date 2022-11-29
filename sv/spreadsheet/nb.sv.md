{
  "date" : "2019-12-16",
  "keywords" :[ "OBS", "fil", "tillägg", "filformat", "Mathematica", "kalkylblad" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om vad som är API:er för en NB-fil som kan skapa och öppna NB-filer.",
  "title" :"OBS - Mathematica Notebook File Format",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Vad är NB fil?

En fil med filtillägget .nb är ett Wolfram notebook-filformat som sparar instruktioner för matematiska instruktioner i en textfil. Den kan innehålla många olika typer av data som liveberäkning, godtyckliga dynamiska gränssnitt, full typinmatning, bildinmatning, automatisk kodkommentar, ett komplett programmatiskt gränssnitt på hög nivå och tusentals noggrant organiserade funktioner och alternativ. Textinstruktionerna är Mathematica-inmatning och -utgång som genereras och uppdateras när inmatningssatserna läggs i filen.

## Wolfram Notebook NB Filformat - Mer information

Wolfram Notebook NB-filer sparas i vanligt textformat som är ett filformat som kan läsas av människor. Innehållet i en anteckningsbok är ordnat i sektioner som vanlig text där var och en representeras av grupper av celler, liknande ett kalkylblad. Området för dessa grupper definieras av en parentes mot slutet av varje cell. Stilen som tilldelas en cell bestämmer dess roll i anteckningsboken enligt beskrivningen nedan.

### Anteckningsböcker som Wolfram-språk

När det är tänkt att spara anteckningsboken som består av matematiska instruktioner för exekvering av Wolfram Language Kernal, tilldelas cellerna i dokumentet automatiskt textstilen `Input`. Detta talar om för kärnan att betrakta dessa som instruktioner som exekveras när användaren utfärdar en kombination av `Skift+Retur`-tangenter. En Mathematica Notebook är som visas i följande exempel.

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram Notebook filformat" >}}

### Anteckningsböcker som dokument

Mathematica Notebooks kan vara i dokumentformat för att ge en titt på vad du ser vad är vad du får (WYSIWYG). Dessa dokument är desamma som visas på skärmen eller på ett tryckt papper och är interaktiva. För detta tilldelas `Textstilen` till cellen för att visa innehållet utan att exekvera uttalanden av kärnan.

## Exportera Mathematica-anteckningsböcker

Mathematica Notebooks kan exporteras till många olika filformat som PDF, grafik, GIS, Compressed och Spreadsheets.

## Referenser

* [Mathematica Notebook Basics](https://reference.wolfram.com/language/guide/NotebookBasics.html)

