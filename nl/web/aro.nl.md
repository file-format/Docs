{
  "date" : "2021-12-09",
  "keywords" :[ "aro", ".aro-bestand", "aro-bestandsindeling", "een bestandstype", "bestand", "type", "wat is een .aro-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARO-bestandsindeling - SteelArrow-webtoepassingsbestand",
  "description" :"Meer informatie over wat een ARO-bestand is en API's die ARO-bestanden kunnen maken en openen.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Wat is een ARO-bestand?

Een ARO-bestand is een webpaginabestand aan de serverzijde dat wordt gegenereerd met SteelArrow Web Application. Het bevat [HTML](/nl/web/html/) en SteelArrow-tags en scripts. Deze worden op de server uitgevoerd om een volledige responspagina te genereren voordat deze naar de browser van de gebruiker worden verzonden. ARO-bestanden bevatten bijna 95% HTML-inhoud, terwijl de rest bestaat uit SteelArrow-code. Om ARO-bestanden voor u te laten werken, moet de SteelArrow Web Applications-server zijn geïnstalleerd en draaien op de webservermachine.

## ARO-bestandsindeling

ARO-bestanden zijn geschreven in HTML-opmaaktaalbestand met ingesloten JavaScript-code en Java-applets. [SteelArrow-tags](http://www.steelarrow.com/docs/basics1.aro) zijn de basisbouwstenen voor de ontwikkeling van webpagina's. Hoewel deze de weergave van de pagina niet veranderen, worden ze gebruikt om de pagina met gegevens te vullen. Bovendien kunnen ze ook worden gebruikt om de uitvoer te regelen met voorwaardelijke instructies.

### ARO Tag Voorbeeld

De<SAOUTPUT> Met de ARO-tag kunnen ontwikkelaars gegevenswaarden op elke plaats in een script uitvoeren. Het kan bijvoorbeeld worden gebruikt om de uitvoer van de PARAM-tabel te krijgen met:<SAOUTPUT VALUE=PARAM[]> die kan worden weergegeven in de HTML<BODY> label.

## Referenties

* [SteelArrow-tags](http://www.steelarrow.com/docs/basics.aro)

