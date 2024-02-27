{
  "date": "2019-10-11",
  "keywords": [
"dhtml",
"dhtml fil",
"dhtml filformat",
"dhtml filtype",
"fil",
"type",
"hvad er en dhtml fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DHTML - Dynamisk HTML-filformat",
  "description": "Lær om DHTML-filformat og API'er, der kan oprette og åbne DHTML-filer.",
  "linktitle": "DHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dhtm-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en DHTML fil?

En fil med filtypen .dhtml er en dynamisk [HTML](/web/html/) fil, der bruges til at skabe dynamisk indhold på en webside. Et webelement oprettet i DHTML er hændelsesdrevet og kræver ikke genindlæsning af siden. I de fleste tilfælde bruges en DHTML-fil til at skabe det dynamiske indhold på en webside, såsom rullemenuer, flydende lag, rollover-knapper og andet dynamisk indhold. Du støder næsten dagligt på dynamiske html-elementer i dit liv, når du holder musen over et menupunkt, og det åbner yderligere undermenumuligheder. DHTML gør brug af webteknologier såsom [HTML](/web/html/), [Javascript](/web/js/), HTML DOM, HTML Events og [CSS](/web/css/) for at opnå den dynamiske adfærd af elementer.

## DHTML filformat

DHTML-filer er almindelige tekstfiler, der indeholder DHTML-kode for at implementere webelementernes dynamiske adfærd.


### DHTML DOM

DHTML Document Object Model (DOM) er baseret på HTML DOM, der er en træstruktur med elementer, attributter og tekst som vist i det følgende billede.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Dokument'-noden kan bruges til at kalde flere funktioner for at implementere forskellig funktionalitet. Det følgende eksempel bruger blot JavaScript-metoden document.write() i DHTML.

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

Denne kode skriver teksten Hello World til output i browseren.

### DHTML-begivenheder

|S.No.|Begivenhed|Begivenhed|
---|---|---|
|1|onabort|Det opstår, når brugeren afbryder indlæsningen af siden eller mediefilen.|
|2|onblur|Det opstår, når brugeren forlader et HTML-objekt.|
|3|onchange|Det opstår, når brugeren ændrer eller opdaterer værdien af et objekt.|
|4|onclick|Det opstår eller udløses, når en bruger klikker på et HTML-element.|
|5|ondblclick|Det opstår, når brugeren klikker på et HTML-element to gange samtidig.|
|6|onfocus|Det opstår, når brugeren fokuserer på et HTML-element. Denne hændelseshandler virker modsat onblur.|
|7|onkeydown|Den udløses, når en bruger trykker på en tast på en tastaturenhed. Denne hændelseshandler virker for alle nøglerne.|
|8|onkeypress|Det udløses, når brugerne trykker på en tast på et tastatur. Denne hændelseshandler udløses ikke for alle nøglerne.|
|9|onkeyup|Det opstår, når en bruger slipper en tast fra et tastatur efter at have trykket på et objekt eller et element.|
|10|onload|Det sker, når et objekt er fuldstændig indlæst.|
|11|onmousedown|Det opstår, når en bruger trykker på en museknap over et HTML-element.|
|12|onmousemove|Det sker, når en bruger flytter markøren på et HTML-objekt.|
|13|onmouseover|Det sker, når en bruger flytter markøren over et HTML-objekt.|
|14|onmouseout|Det opstår eller udløses, når musemarkøren flyttes ud af et HTML-element.|
|15|onmouseup|Det opstår eller udløses, når museknappen slippes over et HTML-element.|
|16|onreset|Det bruges af brugeren til at nulstille formularen.|
|17|onselect|Det sker efter valg af indhold eller tekst på en webside.|
|18|onsubmit|Den udløses, når brugeren klikker på en knap efter indsendelse af en formular.|
|19|onunload|Den udløses, når brugeren lukker en webside.|

## Referencer

* [Dynamisk HTML - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)


