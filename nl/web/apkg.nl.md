{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","apkg-bestand", "apkg-bestandsformaat", "apkg-bestandstype", "bestand", "type", "Wat is een APKG-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Flashcard Deck-bestandsindeling",
  "description" :"Meer informatie over wat een APKG-bestand is en API's die ze kunnen maken en openen.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Wat is een APKG-bestand?

Een bestand met de extensie .apkg is een verzameling flashcards die is gegenereerd om te worden gebruikt in de softwaretoepassing [Anki](https://ankiweb.net/about), een op flashcards gebaseerd leerprogramma. Het bevat [HTML](/nl/web/html/) tekst die moet worden geladen en weergegeven in de Anki-toepassing en kan bovendien afbeeldingen en geluiden bevatten voor visueel en hoorbaar leren. Met Anki kunnen gebruikers hun eigen Anki-flashcard-decks maken en flashcard-decks van andere gebruikers importeren.

## APKG-bestandsindeling

Anki-kaartendecks worden gemaakt op basis van sjablonen die zijn geschreven in HTML, een bekende en veelgebruikte taal voor het maken van webpagina's. Het stylen van deck cards wordt gedaan met behulp van CSS, de taal die wordt gebruikt voor het stylen van webpagina's. De styling omvat aanpassingen aan:

* font-family - De naam van het lettertype dat op de kaart moet worden gebruikt.
* font-size - De grootte van het lettertype in pixels.
* text-align - Bepaalt of de tekst in het midden, links of rechts moet worden uitgelijnd.
* kleur - Definieert de kleur van de tekst, dit kunnen eenvoudige kleurnamen zijn zoals "blauw", "rood", enz. of HTML-kleurcodes.
* achtergrondkleur - Definieert de achtergrondkleur van de kaart

De stijlinformatie wordt door alle kaarten gedeeld, wat van invloed is op alle kaarten wanneer er een wijziging wordt aangebracht. Het volgende voorbeeld gebruikt een gele achtergrond op alle kaarten behalve de eerste:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Het formaat van afbeeldingen in een Anki-kaart kan als volgt worden beheerd.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Javascript insluiten in Anki-kaarten

Het is mogelijk om [Javascript](/nl/web/js/) in een Anki-kaart te embedden met behulp van de kaartsjablonen. Vanwege het geavanceerde niveau van Javascript wordt er echter geen ondersteuning geboden. Bovendien kunnen rendering-apparaten de implementatie-effecten van Javascript in de kaart anders laten zien, waardoor de implementatie op alle apparaten moet worden getest. Bepaalde Javascript-functies, zoals window.alert, maken het moeilijk om fouten op te sporen in de Javascript-code die u hebt geschreven.

## Referenties ##

* [Anki-documentatie](https://docs.ankiweb.net/intro.html)

