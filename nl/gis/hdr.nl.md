{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR-bestand - ESRI BIL Header-bestandsformaat",
  "description":"Wat is een HDR-bestand?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Wat is een HDR-bestand?

Een HDR-bestand is een GIS-headerbestand dat headerinformatie bevat voor een Band interleaved by line (.BIL)-bestand. Het beschrijft de afbeeldingsgegevens en heeft dezelfde naam als die van het afbeeldingsbestand. Een HDR-bestand bestaat uit een reeks vermeldingen, die elk een bepaald kenmerk van de afbeelding beschrijven. Het HDR-bestand beschrijft de lay-out en opmaak van het BIL-bestand voor vertaling naar coördinaten uit de echte wereld in combinatie met een afzonderlijk georeferentiebestand.

## HDR-bestandsformaat

HDR-bestanden worden opgeslagen in ASCII-tekstbestandsindeling. Het bevat een reeks vermeldingen waarbij elke vermelding een bepaald kenmerk van de afbeelding beschrijft. Elk HDR-bestand heeft het volgende formaat:

```
<keyword> <value>
```

`<keyword> ` - Het geeft het specifieke attribuut aan dat wordt ingesteld
`<value> ` - Het is de waarde waarop het attribuut wordt ingesteld

Er is geen beperking op de volgorde van de vermeldingen in de koptekst. Elke invoer moet echter op een afzonderlijke regel van de regel staan om te voldoen aan de parseermethode die door HDR-lezers wordt gebruikt.

## Samenvatting van trefwoorden die in het HDR-bestand worden gebruikt

|Trefwoord |Aanvaardbare waarde |Standaard|
---|---|---|
|nrows |elk geheel getal > 0| geen
|ncols |elk geheel getal > 0| geen
|nbands |elk geheel getal > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|bytevolgorde| I = Intel;M = Motorola |hetzelfde als hostmachine|
|indeling| bil, bip, bsq| bil|
|bytes overslaan| elk geheel getal ≥ 0| 0
|ulxmap |elk reëel getal| 0|
|ulymap |elk reëel getal |nrows - 1|
|xdim |elk reëel getal| 1
|ydim |elk reëel getal| 1
|bandrowbytes |elk geheel getal > 0| kleinste geheel getal ≥ (ncols x nbits) / 8|
|totaalrijbytes |elk geheel getal > 0| voor bil: nbands x bandrowbytes; voor bip: kleinste geheel getal ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |elk geheel getal ≥ 0| 0|

## Referenties

* [HRD-bestandsindeling - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

