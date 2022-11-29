{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om KIT-filformat och API:er som kan skapa och öppna KIT-filer.",
  "title" :"KIT-filformat - CodeKit-fil",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Vad är en KIT fil?

En fil med filtillägget .kit är en HTML-fil som skapas med programmeringsspråksapplikationen [CodeKit](https://codekitapp.com/). Den innehåller "import" och "variabler" utöver befintliga [HTML](/sv/web/html/)-filer, vilket gör den idealisk för statiska webbplatser. CodeKit kompilerar KIT-filer till HTML som lätt kan användas som statiska webbplatsfiler.

## KIT filformat

KIT-filer är HTML-filer som dessutom innehåller importer och variabler. Dessa lagras som vanliga textfiler och kan öppnas med valfri textredigerare eller webbfilredigerare.

### KIT-filimport

Nästan alla typer av filer kan importeras till en Kit-fil. Följande är importsyntaxen som används för att importera filer till en .kit-fil.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

När en import läggs till i en KIT-fil och sparas ersätts den med texten i filen som importeras. Du kan också använda @inkludera istället för @import.

### Flera importer i en KIT-fil

Du kan också importera mer än en fil åt gången genom att använda en kommaseparerad lista:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Referenser

* [Vad är Kit?](https://codekitapp.com/help/kit/)

