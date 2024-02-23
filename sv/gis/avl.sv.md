{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL - ArcView Legend-fil",
  "description":"Lär dig om AVL-filformat och API:er som kan skapa och öppna AVL-filer.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-sv",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## Vad är AVL fil?

En AVL-fil är en förklaringsfil som innehåller en nyckel för en karta genererad med ESRI ArcView GIS (Geographic Information System) programvara. Den innehåller referenssymbolikinformation som används i motsvarande karta för åtkomst. En AVL-fil kan innehålla mer information som symbolik, visningsinställningar, såsom transparens, skalberoende visningsegenskaper, sammanfogad tabell/relaterad tabellinformation, definitionsfråga, etikettegenskaper för funktionslager och anteckningsvisningsegenskaper för anteckningsskikt beroende på typ typ av lager.

En AVL-fil kan refereras från ArcView-projektets [.APR](/gis/apr/)-fil.

## AVL-filformat - Mer information

AVL-filer sparas i vanlig textfilformat. Det betyder att du kan öppna AVL-filer i vilken textredigerare som helst som Notepad, Notepad++ och Apple TextEdit. När den väl har öppnats kan du inte bara se innehållet i filen utan även ändra dessa.

### Skillnad mellan .LYR- och .AVL-filer

 * **Skillnad mellan filformat** - .lyr är en binär fil medan .avl är en textfil
 * **Innehållsskillnad** - En .lyr-fil innehåller mer information än en .avl-fil. En AVL-fil lagrar bara symbolikinformation, medan en LYR-fil lagrar all information som finns tillgänglig i dialogrutan för lageregenskaper i ArcMap.

## Referenser

* [Skillnaden mellan .lyr- och .avl-filer](https://support.esri.com/en/technical-article/000005936)


