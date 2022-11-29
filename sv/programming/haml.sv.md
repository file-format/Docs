{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML-filformat - Haml-källkodsfil",
  "description":"Läs mer om HAML-filformat och API:er som kan skapa och öppna HAML-filer.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Vad är en HAML fil?

En HAML-fil är en HTML-abstraktionsmarkeringsspråkfil som innehåller källkod skriven på språket [Haml](https://haml.info/). Den kan användas som en ersättning för ERB (Ruby template scripts). HAML-filen innehåller mallkällkod för att generera HTML-koden för ett webbdokument. ERB-filer kan ersättas genom att helt enkelt ersätta dessa filer i mappen app/views till Haml genom att ändra filtillägget. HAML-filer kan öppnas med vilken textredigerare som helst som Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML filformat

HAML-filer är källfiler som sparas på skiva som vanliga textfiler. Den innehåller kod skriven i HAML-syntax. HAML ersätter **<>**-taggarna med tecknet **%** för att göra koden enklare och enklare. ERB-filer är drop-in utbytbara av HAML som visas i följande enkla exempel.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML Exempel

Följande är ett exempel på Hello World på HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
som återger till följande HTML-utdata.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Referenser

* [HAML - Github](https://github.com/haml/haml)

