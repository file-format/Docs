{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion Markup Language File",
  "description" :"Läs mer om vad en CFML-fil och API:er är som kan skapa och öppna CFML-filer.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Vad är en CFML fil?

En fil med filändelsen .cfml är en ColdFusion Markup Language-fil som används för att skapa webbsida. Det hänvisar till en uppsättning regler som används för att definiera hur ColdFusion-applikationen kommer att utvecklas av programmeraren. ColdFusion är ett programmeringsspråk som används för att skapa webbapplikationer på serversidan snabbt och med mindre än andra teknologier som [ASP](/sv/web/asp/), [PHP](/sv/web/php/), etc. Vissa av de program som kan öppna CML-filer inkluderar Adobe ColdFusion 2018, Adobe ColdFusion Builder och Adobe Dreamweaver.

## CFML-filformat - Mer information

CFML-filer är uppmärkningsfiler och innehåller webbelement i form av taggar. Det här är textfiler som kan öppnas och redigeras i vilken textredigerare som helst. CFML-filer består av flera taggar som liknar [HTML](/sv/web/html/) och består vanligtvis av en öppnings- och en avslutande tagg. Dessa taggar kan också innehålla ett eller flera attribut.

### Taggar Syntax

Följande är den generaliserade syntaxen för CFML-taggar.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

De flesta taggar accepterar attribut och definieras enligt följande.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Vissa av dessa taggar accepterar också flera attribut med följande syntax.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Exempel på CFML-kod

Här är ett exempel som använder en faktisk CFML-tagg - "cfoutput"-taggen:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Referenser

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

