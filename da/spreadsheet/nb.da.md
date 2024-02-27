{
  "date": "2019-12-16",
  "keywords": [
"NB",
"fil",
"udvidelse",
"filformat",
"Mathematica",
"Regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om, hvad en NB-fil API'er er, der kan oprette og åbne NB-filer.",
  "title": "NB - Mathematica Notebook File Format",
  "linktitle": "NB",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-n-dab"
}
},
  "lastmod": "2021-07-16"
}

## Hvad er en NB fil?

En fil med filtypenavnet .nb er et Wolfram notebook-filformat, der gemmer instruktioner til matematiske instruktioner i en tekstfil. Det kan indeholde mange forskellige typer data, såsom live-beregning, vilkårlige dynamiske grænseflader, fuld typesæt-input, billedinput, automatisk kodeannotering, en komplet programmatisk grænseflade på højt niveau og tusindvis af omhyggeligt organiserede funktioner og muligheder. Tekstinstruktionerne er Mathematica-input og -output, der genereres og opdateres, efterhånden som input-sætningerne lægges i filen.

## Wolfram Notebook NB Filformat - Mere information

Wolfram Notebook NB-filer gemmes i almindeligt tekstformat, som er et filformat, der kan læses af mennesker. Indholdet af en notesbog er arrangeret i sektioner som almindelig tekst, hvor hver er repræsenteret af grupper af celler, svarende til et regneark. Området for disse grupper er defineret af en parentes mod slutningen af hver celle. Den typografi, der er tildelt en celle, bestemmer dens rolle i notesbogen som beskrevet nedenfor.

### Notebooks som Wolfram-sprog

Når det er meningen at gemme notesbogen bestående af matematiske instruktioner til udførelse af Wolfram Language Kernal, tildeles cellerne i dokumentet automatisk tekststilen `Input`. Dette fortæller kernen om at betragte disse som instruktioner, der udføres, når brugeren udsteder en kombination af `Shift+Return`-taster. En Mathematica-notesbog er som vist i følgende eksempel.

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram Notebook-filformat" >}}

### Notesbøger som dokumenter

Mathematica Notebooks kan være i dokumentformat for at give et kig på, hvad du ser, hvad er det, du får (WYSIWYG). Disse dokumenter er de samme som vist på skærmen eller på et trykt papir og er interaktive. Til dette tildeles 'Tekststilen' til cellen for at vise indholdet uden at udføre sætningerne af kernen.

## Eksporter Mathematica-notesbøger

Mathematica Notebooks kan eksporteres til mange forskellige filformater såsom PDF, grafik, GIS, Compressed og Spreadsheets.

## Referencer

* [Mathematica Notebook Basics](https://reference.wolfram.com/language/guide/NotebookBasics.html)


