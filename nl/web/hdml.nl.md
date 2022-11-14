{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Handheld Device Markup Language File",
  "description":"Meer informatie over de HDML-bestandsindeling en API's die HDML-bestanden kunnen maken en openen.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Wat is een HDML-bestand?

Een bestand met de extensie .hdml (Handheld Device Markup Language) is een opmaaktaal voor het maken van webpagina's voor draagbare elektronische apparaten zoals draagbare computers, smartphones en apparaten voor informatieweergave. HDML zou een uitbreiding zijn van de taal [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML is vergelijkbaar met HTML, maar voor draadloze en draagbare apparaten met kleine schermen zoals PDA, mobiele telefoons enzovoort. Het werd vervangen door WML waarvoor het een belangrijke invloed had.

## HDML-bestandsindeling - Meer informatie

HDML is een opmaaktaal voor draagbare apparaten die is gebaseerd op opmaaktags die vergelijkbaar zijn met HTML. HDML werd ter standaardisatie voorgelegd aan W3C, maar het werd nooit een standaard. De specificaties van het bestandsformaat zijn echter beschikbaar op [W3-website](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) ter referentie. De [syntaxis voor HDML-taal](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) is beschikbaar als referentie voor ontwikkelaars en kan worden gebruikt voor voorbeeldtoepassingsontwikkeling.

## HDML-elementen

Hieronder volgt een aantal elementen die een runtime-omgeving bieden voor HDML en waarnaar wordt verwezen als de user-agent.

|Element|Beschrijving|
---|---|
|Kaarten|Dit is de fundamentele bouwsteen van HDML en geeft de gebruiker de mogelijkheid om kaarten met informatie weer te geven en te gebruiken. |
|Decks|HDML-kaarten zijn gegroepeerd in decks. Een HDML-deck is vergelijkbaar met een HTML-pagina in die zin dat het wordt geïdentificeerd door URL [RFC1738] en de inhoudseenheid is die wordt aangevraagd bij een server en in het cachegeheugen wordt opgeslagen door de user-agent.|
|Acties|Acties kunnen van het type PREV, SOFT1-SOFT8 en HELP zijn. Deze zijn abstract en worden op een user-agent-specifieke manier ondersteund in de gebruikersinterface.|
|Activiteiten|Een activiteit is als een groep gerelateerde kaarten die één logische functie vervullen. Deze kunnen een of meer dekken overspannen. Het HDML-navigatie- en statusmodel is opgebouwd rond activiteiten.|
|Op geschiedenis gebaseerde navigatie|De user-agent houdt een geschiedenis bij van de kaarten die aan de gebruiker worden getoond. Elke kaart die wordt geopend, wordt toegevoegd aan de kaartgeschiedenis. Met de user-agent kan de gebruiker gemakkelijk terug navigeren naar de vorige kaart in de geschiedenis.|

## Referenties

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML-specificaties - W3-scholen](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

