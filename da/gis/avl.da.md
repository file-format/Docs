{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL - ArcView Legend-fil",
  "description":"Lær om AVL-filformater og API'er, der kan oprette og åbne AVL-filer.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-da",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## Hvad er AVL fil?

En AVL-fil er en forklaringsfil, der indeholder en nøgle til et kort, der er genereret med ESRI ArcView GIS (Geographic Information System) software. Den indeholder referencesymbologiske oplysninger, der bruges i det tilsvarende kort til adgang. En AVL-fil kan indeholde flere oplysninger såsom symbologi, skærmindstillinger, såsom gennemsigtighed, skalaafhængige visningsegenskaber, sammenføjede tabel/relaterede tabeloplysninger, definitionsforespørgsel, etiketteegenskaber for funktionslag og annotationsvisningsegenskaber for annoteringslag afhængigt af typen slags lag.

Der kan henvises til en AVL-fil fra ArcView-projektets [.APR](/gis/apr/)-fil.

## AVL-filformat - flere oplysninger

AVL-filer gemmes i almindeligt tekstfilformat. Det betyder, at du kan åbne AVL-filer i en hvilken som helst teksteditor som Notepad, Notepad++ og Apple TextEdit. Når den er åbnet, kan du ikke kun se indholdet af filen, men også ændre disse.

### Forskel mellem .LYR- og .AVL-filer

 * **Filformatforskel** - .lyr er en binær fil, mens .avl er en tekstfil
 * **Indholdsforskel** - En .lyr-fil indeholder flere oplysninger end en .avl-fil. En AVL-fil gemmer kun symbologisk information, mens en LYR-fil gemmer al den information, der er tilgængelig i dialogboksen for lagegenskaber i ArcMap.

## Referencer

* [Forskel mellem .lyr- og .avl-filer](https://support.esri.com/en/technical-article/000005936)


