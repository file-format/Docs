{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","dhtml-bestand", "dhtml-bestandsformaat", "dhtml-bestandstype", "bestand", "type", "wat is een dhtml-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Dynamisch HTML-bestandsformaat",
  "description":"Meer informatie over DHTML-bestandsindeling en API's die DHTML-bestanden kunnen maken en openen.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een DHTML-bestand?

Een bestand met de extensie .dhtml is een dynamisch [HTML](/nl/web/html/)-bestand dat wordt gebruikt om dynamische inhoud van een webpagina te maken. Een webelement dat in DHTML is gemaakt, is gebeurtenisgestuurd en hoeft de pagina niet opnieuw te laden. In de meeste gevallen wordt een DHTML-bestand gebruikt om de dynamische inhoud van een webpagina te maken, zoals vervolgkeuzemenu's, zwevende lagen, rollover-knoppen en andere dynamische inhoud. Je komt bijna dagelijks dynamische html-elementen tegen wanneer je met de muis over een menu-item beweegt en het opent verdere submenu-opties. DHTML maakt gebruik van webtechnologieën zoals [HTML](/nl/web/html/), [Javascript](/nl/web/js/), HTML DOM, HTML Events en [CSS](/nl/web/css/) om de dynamische gedrag van elementen.

## DHTML-bestandsindeling

DHTML-bestanden zijn platte tekstbestanden die DHTML-code bevatten om het dynamische gedrag van de webelementen te implementeren.


### DHTML DOM

Het DHTML Document Object Model (DOM) is gebaseerd op de HTML DOM die een boomstructuur is met elementen, attributen en tekst zoals getoond in de volgende afbeelding.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Het knooppunt `Document` kan worden gebruikt om verschillende functies aan te roepen om verschillende functionaliteit te implementeren. In het volgende voorbeeld wordt eenvoudig de methode document.write() van JavaScript in de DHTML gebruikt.

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

Deze code schrijft de tekst "Hello World" om in de browser uit te voeren.

### DHTML-evenementen

|S.No.|Gebeurtenis|Gebeurtenis|
---|---|---|
|1|onabort|Dit gebeurt wanneer de gebruiker het laden van de pagina of het mediabestand afbreekt.|
|2|onblur|Het treedt op wanneer de gebruiker een HTML-object verlaat.|
|3|onchange|Het treedt op wanneer de gebruiker de waarde van een object wijzigt of bijwerkt.|
|4|onclick|Het treedt op of wordt geactiveerd wanneer een gebruiker op een HTML-element klikt.|
|5|ondblclick|Het komt voor wanneer de gebruiker twee keer tegelijk op een HTML-element klikt.|
|6|onfocus|Het komt voor wanneer de gebruiker zich concentreert op een HTML-element. Deze gebeurtenis-handler werkt tegengesteld aan onblur.|
|7|onkeydown|Het wordt geactiveerd wanneer een gebruiker op een toets op een toetsenbord drukt. Deze gebeurtenis-handler werkt voor alle sleutels.|
|8|onkeypress|Het wordt geactiveerd wanneer de gebruikers op een toets op een toetsenbord drukken. Deze gebeurtenishandler wordt niet voor alle sleutels geactiveerd.|
|9|onkeyup|Het komt voor wanneer een gebruiker een toets van een toetsenbord loslaat nadat hij op een object of element heeft gedrukt.|
|10|onload|Het treedt op wanneer een object volledig is geladen.|
|11|onmousedown|Het komt voor wanneer een gebruiker de muisknop over een HTML-element drukt.|
|12|onmousemove|Het komt voor wanneer een gebruiker de cursor op een HTML-object beweegt.|
|13|onmouseover|Het komt voor wanneer een gebruiker de cursor over een HTML-object beweegt.|
|14|onmouseout|Het treedt op of wordt geactiveerd wanneer de muisaanwijzer uit een HTML-element wordt verplaatst.|
|15|onmouseup|Het treedt op of wordt geactiveerd wanneer de muisknop wordt losgelaten boven een HTML-element.|
|16|onreset|Het wordt door de gebruiker gebruikt om het formulier te resetten.|
|17|onselect|Het gebeurt na het selecteren van de inhoud of tekst op een webpagina.|
|18|onsubmit|Het wordt geactiveerd wanneer de gebruiker op een knop klikt na het indienen van een formulier.|
|19|onunload|Het wordt geactiveerd wanneer de gebruiker een webpagina sluit.|

## Referenties

* [Dynamische HTML - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

