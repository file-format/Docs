{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML-bestandsindeling - Haml-broncodebestand",
  "description":"Meer informatie over HAML-bestandsindeling en API's die HAML-bestanden kunnen maken en openen.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Wat is een HAML-bestand?

Een HAML-bestand is een HTML-abstractie opmaaktaalbestand dat de broncode bevat die is geschreven in de taal [Haml](https://haml.info/). Het kan worden gebruikt als vervanging voor de ERB (Ruby-sjabloonscripts). HAML-bestand bevat sjabloonbroncode die voor het genereren van de HTML van een webdocument. ERB-bestanden kunnen worden vervangen door deze bestanden eenvoudig in de map app/views te vervangen door Haml door de extensie van het bestand te wijzigen. HAML-bestanden kunnen worden geopend met elke teksteditor zoals Microsoft Notepad, Notepad ++, Apple TextEdit,

## HAML-bestandsindeling

HAML-bestanden zijn bronbestanden die op schijf zijn opgeslagen als platte tekstbestanden. Het bevat code geschreven in HAML-syntaxis. HAML vervangt de **<>** tags door het **%** teken om code eenvoudiger en gemakkelijker te maken. ERB-bestanden kunnen door HAML worden vervangen, zoals in het volgende eenvoudige voorbeeld wordt getoond.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML Voorbeeld

Het volgende is een voorbeeld Hello World-voorbeeld van HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
die wordt weergegeven in de volgende HTML-uitvoer.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Referenties

* [HAML - Github](https://github.com/haml/haml)

