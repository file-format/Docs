{
  "date" : "2021-05-24",
  "keywords" :["xht", "Fil", "Tillägg", "Filformat", "Filtillägg", "utökat uppmärkningsspråk för hypertext"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHT",
  "description":"Läs mer om XHT-filformat och API:er som kan skapa och öppna XHT-filer.",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Vad är en XHT fil?

En fil med filtillägget .xht är en webbfil som är associerad med filtypen [XHTML](/sv/web/xhtml/) (Extended Hypertext Markup Language), som i sig är en [XML](/sv/web/xml/)-baserad uppmärkningsfil. Båda dessa filer liknar HTML men har en strängare XML-liknande syntax. XHT-filer är utformade på ett sätt för att vara mer strukturerade, involverar mindre skript och är generiska förutom att använda de befintliga faciliteterna för XML.

## XHT filformat

En XHT-fil skapas och lagras som en vanlig textfil med UTF-8-kodning som standard. Den innehåller den fullständiga källkoden för ett XHTML-dokument som kan öppnas och redigeras med vilken textredigerare som helst som stöder Unicode-kodning. Förutom textredigerare är XHT-filformat förståeligt av de flesta moderna webbläsare och kan öppnas med dessa.

## XHT-exempel

Följande exempel på ett XHT-dokument definierar XML-deklarationerna.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## Referenser ##

* [A History of XHTML: From the 1990s to Today](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

