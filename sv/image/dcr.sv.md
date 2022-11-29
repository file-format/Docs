{
  "date" : "2021-26-08",
  "keywords" :[ "dcr-fil", "dcr-filformat", "vad är en dcr-fil", "fil", "dcr-exempel", "dcr-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR - Digital Camera RAW Image File",
  "description":"Läs mer om DCR-filformat och API:er som kan skapa och öppna DCR-filer.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Vad är en DCR fil? ##
En fil med dcr-tillägget innehåller innehållet i ett digitalt fotografi som sparats i Kodak Digital Camera RAW-format (DCR). DCR är en förkortning för **Digital Camera Raw**; innehåller den okomprimerade och förlustfria versionen av bilddata som tagits med en Kodak digitalkamera. Professionella fotografer gillar att använda dessa filer, eftersom de lagrar bilder med högre kvalitet än komprimerade bildformat av låg kvalitet.

## DCR-filformat
DCR är ett proprietärt format utvecklat av Eastman Kodak Company; kallas helt enkelt Kodak. En Digital Camera Raw-bildfil (DCR) innehåller minimalt bearbetade data från bildsensorn en digitalkamera. Dessa filer är ännu inte bearbetade och är därför inte redo att skrivas ut eller redigeras med en bitmappsredigerare.
Vanligtvis bearbetar en råkonverterare bilden i ett brett internt färgområde där noggrannhet och förfining kan göras innan konvertering till ett rasterfilformat som TIFF eller JPEG för lagring, utskrift eller ytterligare manipulation.
### Filinnehåll
Strukturen för råfiler följer ofta ett generiskt mönster:
- En kort filhuvud som innehåller en indikator för filens byteordning.
- Kamerasensormetadata som krävs för att tolka sensorbildsdata, inklusive attributen för CFA, sensorns storlek och dess färgprofil.
- Bildmetadata som kan vara användbar för inkludering i vilken CMS-miljö eller databas som helst. Vissa råfiler innehåller en standardiserad metadatasektion med data i Exif-format.
- En bildminiatyr.
- En JPEG-konvertering i full storlek av bilden, som används för att förhandsgranska filen på kamerans LCD-panel.
- I fallet med filmfilmsskanningar, antingen tidskoden, nyckelkoden eller bildrutan i filsekvensen som representerar bildsekvensen i en skannad rulle.
- Sensorns bilddata
### Sensorbilddata
Råfilen spelar samma roll i digital fotografering som fotografisk film spelar i filmfotografering. Raw-filer innehåller alltså data i full upplösning som läses ut från var och en av kamerans bildsensorpixlar. Kamerans sensor är nästan konstant överlagd med en CFA (Color Filter Array. Den kan användas i hög dynamisk omfångsbildkonvertering när råformatdata är tillgängligt, som ett enklare alternativ till multiexponerings-HDI-metoden att ta tre separata bilder.


## Referenser ##

* [Raw bildformat - av Wikipedia](https://en.wikipedia.org/wiki/Raw_image_format)
* [Vad är en DCR-fil](https://expertphotography.com/dcr-file/)

