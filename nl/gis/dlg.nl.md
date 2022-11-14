{
  "date" : "2021-07-30",
  "keywords" :[ "dlg-bestand", "dlg-bestandsformaat", "wat is een dlg-bestand", "bestand", "dlg-voorbeeld", "dlg-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Shapefile Shape Index Format",
  "description":"Meer informatie over DLG-bestandsindelingen en API's die DLG-bestanden kunnen maken en openen.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Wat is een DLG-bestand?
Een bestand met de extensie .dlg bevat de Digital Line Graph, een cartografische kaartfunctie die wordt weergegeven in digitale vectorvorm en wordt beheerd door de US Geological Survey (USGS). De DLG-bestanden zijn beschikbaar in twee verschillende formaten:
1. **Optioneel formaat**: een eenvoudig te gebruiken formaat met een logische recordlengte van 80 bytes, het UTM-grondcoördinatensysteem en topologiekoppelingen in lijn-, knoop- en gebiedselementen.
2. **Spatial Data Transfer Standard (SDTS)-formaat**: een formaat dat de overdracht van ruimtelijke gegevens tussen verschillende computersystemen vergemakkelijkt.

## DLG-bestandsindeling
Het DLG-bestandsformaat is ontworpen voor USGS-kaarten en wordt verzonden op grote, gemiddelde en kleine schaal met maximaal negen verschillende categorieën functies. De DLG-bestanden zijn verkrijgbaar in optionele en SDTS-indelingen (Spatial Data Transfer Standard) die topologisch gestructureerd zijn voor gebruik in kaart- en GIS-toepassingen.
### Specificaties van DLG-bestandsindeling
De DLG-bestanden worden op drie verschillende schalen verdeeld:

1. **Grote schaal** - komt normaal gesproken overeen met:
- De USGS 7,5 bij 7,5 minuut
- Topografische vierhoekige kaartreeksen op schaal 1:24.000 en 1:25.000
- schaal 1:63.360 voor Alaska
- schaal 1:30.000 voor Puerto Rico
 

2. **Gemiddelde schaal** - afgeleid van de USGS:

- 30 bij 60 minuten

- Kaartseries op schaal 1:100.000
3. **Kleinschalig** - afgeleid van de USGS-doorsnedekaarten op schaal 1: 2.000.000 van de Nationale Atlas van de Verenigde Staten
### Gegevenscategorieën
Negen verschillende categorieën lagen of objecten zijn beschikbaar in DLG-bestanden:
1. Openbaar landmeetsysteem (PLSS)
2. Grenzen (BD)
3. Vervoer (TR)
4. Hydrografie (HY)
5. Hypsografie (HP)
6. Niet-vegetatieve kenmerken (NV)
7. Survey controle en markers (SM)

8. Door de mens gemaakte kenmerken (MS)

9. Vegetatieve oppervlaktebedekking (SC)

Grootschalige DLG-bestanden bieden alle negen lagen, terwijl de gemiddelde schaal de vijf lagen PLSS, BD, TR, HY en HP biedt. Kleinschalige DLG's bieden de vijf lagen PLSS, BD, TR, HY en MS.

## Referenties

* [Digitale lijngrafiek - door Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


