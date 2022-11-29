{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","dhtml-fil", "dhtml-filformat", "dhtml-filtyp", "fil", "typ", "vad är en dhtml-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Dynamiskt HTML-filformat",
  "description":"Läs mer om DHTML-filformat och API:er som kan skapa och öppna DHTML-filer.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en DHTML-fil?

En fil med filtillägget .dhtml är en dynamisk [HTML](/sv/web/html/) fil som används för att skapa dynamiskt innehåll på en webbsida. Ett webbelement skapat i DHTML är händelsestyrt och behöver inte ladda om sidan. I de flesta fall används en DHTML-fil för att skapa det dynamiska innehållet på en webbsida som rullgardinsmenyer, flytande lager, överrullningsknappar och annat dynamiskt innehåll. Du stöter på dynamiska html-element nästan dagligen i ditt liv när du för musen över ett menyalternativ och det öppnar ytterligare undermenyalternativ. DHTML använder webbteknologier som [HTML](/sv/web/html/), [Javascript](/sv/web/js/), HTML DOM, HTML Events och [CSS](/sv/web/css/) för att uppnå dynamiken elements beteende.

## DHTML filformat

DHTML-filer är vanliga textfiler som innehåller DHTML-kod för att implementera webbelementens dynamiska beteende.


### DHTML DOM

DHTML Document Object Model (DOM) är baserad på HTML DOM som är en trädstruktur med element, attribut och text som visas i följande bild.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

'Dokument'-noden kan användas för att anropa flera funktioner för att implementera olika funktioner. Följande exempel använder helt enkelt JavaScript-metoden document.write() i DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Denna kod skriver texten "Hello World" för att mata ut i webbläsaren.

### DHTML-händelser

|S.No.|Händelse|Händelse|
---|---|---|
|1|onabort|Det inträffar när användaren avbryter inläsningen av sidan eller mediafilen.|
|2|onblur|Det inträffar när användaren lämnar ett HTML-objekt.|
|3|onchange|Det inträffar när användaren ändrar eller uppdaterar värdet på ett objekt.|
|4|onclick|Det inträffar eller utlöses när någon användare klickar på ett HTML-element.|
|5|ondblclick|Det inträffar när användaren klickar på ett HTML-element två gånger samtidigt.|
|6|onfocus|Det inträffar när användaren fokuserar på ett HTML-element. Denna händelsehanterare fungerar motsatsen till onblur.|
|7|onkeydown|Det utlöses när en användare trycker på en tangent på en tangentbordsenhet. Denna händelsehanterare fungerar för alla nycklar.|
|8|onkeypress|Det utlöses när användarna trycker på en tangent på ett tangentbord. Denna händelsehanterare utlöses inte för alla nycklar.|
|9|onkeyup|Det inträffar när en användare släpper en tangent från ett tangentbord efter att ha tryckt på ett objekt eller element.|
|10|onload|Det inträffar när ett objekt är fullständigt laddat.|
|11|onmousedown|Det inträffar när en användare trycker på en musknapp över ett HTML-element.|
|12|onmousemove|Det inträffar när en användare flyttar markören på ett HTML-objekt.|
|13|onmouseover|Det inträffar när en användare flyttar markören över ett HTML-objekt.|
|14|onmouseout|Det inträffar eller utlöses när muspekaren flyttas ut från ett HTML-element.|
|15|onmouseup|Det inträffar eller utlöses när musknappen släpps över ett HTML-element.|
|16|onreset|Det används av användaren för att återställa formuläret.|
|17|onselect|Det inträffar efter att ha valt innehåll eller text på en webbsida.|
|18|onsubmit|Det utlöses när användaren klickar på en knapp efter att ett formulär har skickats.|
|19|onunload|Det utlöses när användaren stänger en webbsida.|

## Referenser

* [Dynamisk HTML - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

