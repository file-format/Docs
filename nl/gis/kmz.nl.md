{
  "date" : "2019-10-11",
  "keywords" :[ "kmz-bestand", "wat is een kmz-bestand", "bestand", "kmz-voorbeeld", "kmz-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - KML gezipte bestandsindeling",
  "description":"Meer informatie over KMZ-bestandsindeling en API's die KMZ-bestanden kunnen maken en openen.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een KMZ-bestand?

KMZ-bestand (KML Zipped) is een weergave van een gecomprimeerd [KML](/nl/gis/kml/)-bestand dat geospatiale informatie bevat die kan worden bekeken in GIS-toepassingen zoals Google Earth. Informatie over plaatsmarkeringen wordt in het bestand weergegeven als lengte- en breedtegraad, samen met een aangepaste naam. Het enkelvoudig verpakte KMZ-bestand kan eenvoudig met andere gebruikers worden gedeeld. KMZ-bestanden kunnen ook 3D-modelgegevens bevatten voor geo-representatie van het model. Een KMZ-bestand kan worden geopend in Google Maps door het bestand op een online locatie op te slaan en vervolgens de URL in het zoekvak van Google Maps te typen.

## Bestandsstructuur ##

De inhoud van een MKZ-bestand bestaat uit een KML-hoofdbestand en nul of meer bijbehorende bestanden. Het kan worden geëxtraheerd met behulp van standaard decompressieprogramma's zoals WinZIP. Het KMZ-bestandsformaat wordt ook gecomprimeerd tot een archief met een compressieverhouding van 10:1. U kunt gegevens van Google Earth-achtige toepassingen rechtstreeks naar het KMZ-bestandsformaat exporteren. Het hoofd KML-bestand heet **doc.kml**. Bij het inpakken van een KMZ-bestand kunnen er meer dan één KML-bestand aan worden toegevoegd, maar dit heeft geen zin omdat Google Earth bij het openen van het KMZ-bestand naar het eerste KML-bestand zoekt en het leest. Het negeert alle verdere KML-bestanden die in het archief worden gevonden. Om er zeker van te zijn dat het gewenste KML-bestand door Google Earth wordt gelezen, wordt aanbevolen om slechts één KML-bestand in het KMZ-bestand te plaatsen.

De afbeeldingen, modellen, texturen, geluidsbestanden en andere bronnen waarnaar in het doc.kml-bestand wordt verwezen, worden in een andere submap in de hoofdmap geplaatst. Dit kan ook enige complexiteit met zich meebrengen, afhankelijk van het aantal ondersteunende bestanden. Links naar deze samenstellende bronnen kunnen relatief of via absolute verwijzingen zijn.

### Relatieve verwijzing ###

Wanneer bronnen naast het hoofddocument.kml in een submap in de hoofdmap worden geplaatst, kan de relatieve verwijzing naar deze ondersteunende bestanden verwijzen, zoals in het volgende voorbeeld wordt getoond (alleen voor pictogram).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absolute verwijzing ###

Er kan ook absoluut naar bronnen worden verwezen. Absolute verwijzingen bevatten de volledige URL voor het gekoppelde bestand. Wanneer bestanden op een centrale server worden geplaatst, zorgt absolute verwijzing ervoor dat deze ondubbelzinnig blijven in vergelijking met relatieve verwijzing. Het wordt niet aanbevolen om absoluut naar lokale bestanden te verwijzen, omdat deze koppelingen worden verbroken wanneer de bestanden naar een nieuw systeem worden verplaatst. Een voorbeeld van absolute verwijzing is als volgt:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Zie ook ##

* [GeoJSON](/nl/gis/geojson/)

## Referenties ##

* [Google Earth- en KMZ-bestanden](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

