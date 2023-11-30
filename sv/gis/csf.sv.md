{
  "date" : "2023-01-27",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSF File - GeoMedia Coordinate System File Format",
  "description":"Läs mer om CSF-filformat och API:er som kan skapa och öppna CSF-filer.",
  "linktitle" : "CSF",
  "menu" : {
    "docs" : {
      "identifier":"gis-csf",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-27"
}

## Vad är en CSF fil?

En CSF-fil är en koordinatsystemfil som innehåller information om koordinatsystemet för en GIS-fil. Den används av Intergraphs GeoMedia-mjukvara för att definiera parametrarna för ett visst koordinatsystem. Dessa inkluderar informationsparametrar som datum, projektion och måttenheter. Denna information används för att producera kartor för utdata som inte har ett koordinatsystem på plats. Denna information används av GeoMedia för att korrekt visa och manipulera geografiska data i rätt koordinatsystem.

## CSF filformat

CSF-filer lagras som textfiler med detaljer om det geografiska koordinatsystemet. GeoMedia tillåter import av geografiska informationsfiler från indata som inte har några definierade koordinatsystem. Med hjälp av projektions- och koordinatsystemet visar GIS-system kartfilen med exakta värden. En CSF-fil skapas på samma plats som utdatafilen.

## Referenser

* [Hur visar eller serverar du shapefile-data korrekt i GeoMedia?
](https://supportsi.hexagon.com/help/s/article/How-do-you-correctly-display-or-serve-shapefile-data-into?language=en_US)

