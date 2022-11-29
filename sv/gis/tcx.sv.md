{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX File Format- Training Center XML-fil",
  "description":"Läs mer om TCX-filformat och API:er som kan skapa och öppna TCX-filer.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Vad är TCX fil?

En TCX-fil (Training Center XML) är ett datautbytesformat som används för att dela data mellan träningsenheter. Den introducerades 2008 med Garmins produkt Training Center. Träningsdata som puls, löpkadens, cykelkadens, kalorier och varvtid lagras i formatet [XML](/sv/web/xml/) i TCX-filen. Dessutom ingår även sammanfattningsdata om träningsspåret i TCX-filen. TCX-filer liknar [FIT](/sv/gis/fit/)-filer som skapas med Garmins bärbara sportenheter.

## TCX-filformat - Mer information

TCX-filer sparas på skiva som XML-filer med varje post sparad som en aktivitet. En aktivitet omfattar all data från ett träningspass, såsom tid, varvtid, ID, puls, intensitet, kadens och spårinformation som innehåller positionsparen tillsammans med tidsstämpeln för den lat-långa positionen som liknar [GPX] (/sv/gis/gpx/) filer.

### TCX-filformatsversioner

Det finns två versioner av det här formatet med sina egna XML-scheman som tillhandahålls av Garmin. Följande är några av dem:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX Data Protocol

En snabbversion av TCX XML-format finns tillgänglig på Github som [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Referenser ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

