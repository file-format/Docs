{
  "date" : "2021-07-28",
  "keywords" :[ "ntf-bestand", "ntf-bestandsformaat", "wat is een ntf-bestand", "bestand", "ntf-voorbeeld", "ntf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - National Transfer Format-bestanden",
  "description":"Meer informatie over NTF-bestandsindelingen en API's die NTF-bestanden kunnen maken en openen.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Wat is een NTF-bestand?
De bestanden met de extensie .ntf worden de **National Transfer Format (NTF)**-bestanden genoemd; meestal gebruikt door de UK Ordnance Survey (OS); specifiek voor de overdracht van geospatiale gegevens. Het wordt beheerd door de British Standards Institution. Het is het standaard overdrachtsformaat geworden voor digitale gegevens van Ordnance Survey. De National Grid-projectie van het VK, een soort Transverse Mercator, bevat alle georeferentie-informatie voor NTF-bestanden.

## NTF-bestandsindeling
Het NTF-bestandsformaat is eigendom van Ordnance Survey in het Verenigd Koninkrijk; ondersteund door de GDB-bibliotheek voor import. De huidige versie van het NTF-bestandsformaat is 2.0. Deze bestandsindeling is geïntroduceerd om een beperking van het **PCIDSK**-vectorsegment aan te pakken, dat slechts één attribuutveld per structuur heeft, maar er zijn verschillende attributen die kunnen worden geëxtraheerd met vectorgegevens. Om het NTF-bestandsformaat te omzeilen, bestaat het uit twee segmenten. Elk segment bestaat uit dezelfde vectoren, maar met verschillende attributen. Het eerste segment van een NTF-vectorbestand bevat de vectoren met het kenmerkcodenummer als attribuut. Het tweede segment bevat de vectoren met de waarde als attribuut.

### Coördinatenreferentiesysteem
De GDB-bibliotheek vertegenwoordigt raster- en vectorgegevens met de juiste TM-projectiekenmerken:

- Referentielengte: 49.0
- Referentiebreedte: 2.0
- Valse Easting: 400000
- Valse noorden: -100000
- Schaal: 0,9996012717
- Ellipsoïde: Luchtig 1830 (E009)
Er is geen ondersteuning beschikbaar voor het updaten of schrijven van NTF-bestanden, noch kunnen de DTM-bestanden worden gekoppeld.

### Ogrinfo voorbeeld
Het volgende voorbeeld gebruikt **ogrinfo** op een NTF-bestand om laagnummers op te halen:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Referenties

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Webmapping - geïllustreerd door Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

