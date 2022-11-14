{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM-bestand - Handheld Device Markup Language-bestand",
  "description":"Meer informatie over HDM-bestandsindelingen en API's die HDM-bestanden kunnen maken en openen.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Wat is een HDM-bestand?

Een HDM-bestand is een webpaginabestand met opmaaktaal dat is gemaakt in de Handheld Device Markup Language (HDML). Het bevat opmaaktags die lijken op de taal [HTML](/nl/web/html/), maar is ontworpen voor draagbare elektronische apparaten zoals smartphones en PDA's. De [specificaties van het HDML-bestandsformaat](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) werden ingediend bij W3C voor standaardisatie, maar konden geen standaard worden. HDM is gebaseerd op de [HDML](/nl/web/hdml/) bestandsformaatspecificaties die beschikbaar zijn op de W3-website.

## HDM-bestandsindeling - Meer informatie

HDM-bestand bestaat uit markup-tags die worden weergegeven op een visueel ontworpen website op handheld-apparaten. HDM-bestanden worden naar apparaten gekopieerd met behulp van het HDTP-protocol (Handheld Device Transport Protocol) in plaats van het HTTP-protocol dat wordt gebruikt voor HTML-pagina's.

## HDML-bestandselementen

Hieronder volgt een aantal elementen die een runtime-omgeving bieden voor HDML en waarnaar wordt verwezen als de user-agent.

|Element|Beschrijving|
---|---|
|Kaarten|Dit is de fundamentele bouwsteen van HDML en geeft de gebruiker de mogelijkheid om kaarten met informatie weer te geven en te gebruiken. |
|Decks|HDML-kaarten zijn gegroepeerd in decks. Een HDML-deck is vergelijkbaar met een HTML-pagina in die zin dat het wordt geïdentificeerd door URL [RFC1738] en is de inhoudseenheid die wordt opgevraagd bij een server en in het cachegeheugen wordt opgeslagen door de user-agent.|
|Acties|Acties kunnen van het type PREV, SOFT1-SOFT8 en HELP zijn. Deze zijn abstract en worden op een user-agent-specifieke manier ondersteund in de gebruikersinterface.|
|Activiteiten|Een activiteit is als een groep gerelateerde kaarten die één logische functie vervullen. Deze kunnen een of meer dekken overspannen. Het HDML-navigatie- en statusmodel is opgebouwd rond activiteiten.|
|Op geschiedenis gebaseerde navigatie|De user agent houdt een geschiedenis bij van de kaarten die aan de gebruiker worden getoond. Elke kaart die wordt geopend, wordt toegevoegd aan de kaartgeschiedenis. Met de user-agent kan de gebruiker gemakkelijk terug navigeren naar de vorige kaart in de geschiedenis.|

## Referenties

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML-specificaties - W3-scholen](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

