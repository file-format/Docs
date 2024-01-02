{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SSF - Trimble Standard Storage Format File",
  "description":"Läs mer om SSF-filformat och API:er som kan skapa och öppna SSF-filer.",
  "linktitle" : "SSF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-24"
}

## Vad är en SSF fil?

En fil med .ssf-fil är ett filformat för geospatial datalagring som används av programvaran [Trimble](https://www.trimble.com) Navigation GIS. Den lagrar GPS-data inspelad från fält med hjälp av Trimble-enheter. GPS-loggen importeras sedan till en av applikationerna i Trimble Applications Suite. GPS-loggen som finns i en SSF används för att skapa anpassade koordinatsystem. SSF-filer kan öppnas med [Trimble Navigation GPS Pathfinder Office](https://geospatial.trimble.com/en/products/software/office-software), Trimble Navigation GPS Pathfinder Tools SDK och ESRI ArcGIS for Desktop med Trimble GPS Analyst plug-in.

## SSF-filformat - Mer information

När GPS-data överförs från Trimble-enhet till dator för efterbearbetning, kombineras alla dessa filer till en enda .ssf-fil. Denna obearbetade obearbetade fil används av efterbehandlingsprogrammet för att göra korrigeringar och hjälpmedel vid datahantering.

SSF-filer lagras på skiva som Trimbles proprietära filformat och dess detaljerade specifikationer är inte tillgängliga offentligt. Den är specifik för Trimble-enheter och representerar data från GPS-enheten. Hittills finns ingen icke-kommersiell gratislösning tillgänglig för att läsa eller konvertera SSF-filer.

## Referenser

* [Trimble News Release](https://www.trimble.com/news/release.aspx?id=050510b)

