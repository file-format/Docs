{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX-bestandsindeling- Training Center XML-bestand",
  "description":"Meer informatie over TCX-bestandsindelingen en API's die TCX-bestanden kunnen maken en openen.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Wat is een TCX-bestand?

Een TCX-bestand (Training Center XML) is een formaat voor gegevensuitwisseling dat wordt gebruikt om gegevens tussen fitnessapparaten te delen. Het werd in 2008 geïntroduceerd met Garmin's Training Center-product. Trainingsgegevens zoals hartslag, hardloopcadans, fietscadans, calorieën en rondetijd worden opgeslagen in [XML](/nl/web/xml/)-indeling in het TCX-bestand. Daarnaast worden samenvattende gegevens over het trainingstraject ook opgenomen in het TCX-bestand. TCX-bestanden lijken op [FIT](/nl/gis/fit/)-bestanden die zijn gemaakt met draagbare sporttoestellen van Garmin.

## TCX-bestandsindeling - Meer informatie

TCX-bestanden worden op schijf opgeslagen als XML-bestanden, waarbij elk record als activiteit wordt opgeslagen. Een activiteit omvat alle gegevens van een training, zoals tijd, rondetijd, ID, hartslag, intensiteit, cadans en trackinformatie die de positieparen bevat samen met het tijdstempel voor die lat-long positie vergelijkbaar met de [GPX](/nl/gis/gpx/) bestanden.

### Versies van TCX-bestandsindelingen

Er zijn twee versies van dit formaat met hun eigen XML-schema's die worden gehost door Garmin. Hieronder volgen er enkele:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX-gegevensprotocol

Een snelle versie van het TCX XML-formaat is beschikbaar op Github als [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Referenties ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX-viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

