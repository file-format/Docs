{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FIT-bestandsindeling - Garmin-activiteitenbestand",
  "description":"Meer informatie over FIT-bestandsindelingen en API's die FIT-bestanden kunnen maken en openen.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Wat is een FIT-bestand?

Een FIT-bestand is een GIS-bestand dat is gemaakt door draagbare sportapparaten van Garmin. Het wordt gebruikt om de activiteiten van de persoon vast te leggen wanneer hij/zij beweegt met deze apparaten. De activiteitsgegevens omvatten locatie en tijd zoals vastgelegd door het GPS-apparaat. FIT-bestanden worden ook gebruikt om de geregistreerde activiteitsgegevens over te dragen met behulp van web-API's. Dat is de reden waarom FIT-bestanden het meest gebruikte bestandsformaat zijn voor het delen van fitnessgegevens met andere fitnessplatforms. Andere veelgebruikte bestandsindelingen zijn [GPX](/nl/gis/gpx/), TCX en [KML](/nl/gis/kml/).

## FIT-bestandsindeling - Meer informatie

FIT-bestanden worden op schijf opgeslagen als binaire bestanden met de informatie die door de Garmin-toestellen voor de activiteit is vastgelegd. Informatie die is opgeslagen in een FIT-bestand omvat:

* Datum Tijd
* Sporttypes
* Ronde- en gesplitste gegevens
* GPS-track
* Sensorgegevens
* Evenementen voor actieve sessie

Activiteitsgegevens kunnen in realtime in het bestand worden opgenomen of worden geëxporteerd zodra de activiteitsregistratie is voltooid.

### FIT-activiteitsberichten

Een FIT-activiteitenbestand kan enkele vereiste berichttypen bevatten. Hieronder volgen de vereiste berichten voor een activiteitenbestand.

|Bericht|Doel|
---|---|
|Bestands-ID| Het File Id-bericht is vereist voor alle FIT-bestandstypen en zal naar verwachting het eerste bericht in het bestand zijn. Voor activiteitenbestanden moet de eigenschap Type worden ingesteld op 4.|
|Activiteit| Een enkel activiteitsbericht is vereist in een FIT-activiteitenbestand. In het activiteitsbericht zijn de eigenschappen Local Timestamp en Session Count inbegrepen. De lokale tijdstempel wordt gebruikt om de tijdzoneverschuiving te bepalen die op alle tijdstempels in het bestand kan worden toegepast. De meeste apparaten nemen FIT-bestanden in realtime op en het aantal sessies is tot het einde van de opname onbekend. Hierdoor is het activiteitsbericht vaak het laatste bericht in het bestand.|
|Sessie| Activiteitsbestanden zullen een of meer Sessieberichten bevatten. Een Sessiebericht is een Samenvatting berichttype. Starttijd, Totale verstreken tijd, Totale timertijd en Tijdstempel zijn verplichte velden voor alle samenvattingsberichten.|
|Ronde| Rondeberichten vertegenwoordigen ronden of intervallen binnen de sessie. Een Lap-bericht is een bericht van het type Samenvatting. Starttijd, Totale verstreken tijd, Totale timertijd en Tijdstempel zijn verplichte velden voor alle samenvattingsberichten.|
|Opnemen| Opgenomen berichten omvatten GPS-coördinaat, snelheid, afstand, hartslag, vermogen, enz.|

## FIT Bestand Nuttige bronnen

* [Decoding FIT-activiteitsbestanden](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Fit-activiteitsbestanden coderen](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Referenties ##

* [FIT-activiteitenbestand](https://developer.garmin.com/fit/file-types/activity/)

