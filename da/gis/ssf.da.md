{
  "date": "2021-08-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SSF - Trimble Standard Storage Format File",
  "description": "Lær om SSF filformat og API'er, der kan oprette og åbne SSF filer.",
  "linktitle": "SSF",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-ss-daf"
}
},
  "lastmod": "2021-08-24"
}

## Hvad er en SSF fil?

En fil med .ssf-fil er et Geospatial datalagringsfilformat, der bruges af [Trimble](https://www.trimble.com) Navigation GIS-softwareapplikationerne. Den gemmer GPS-data, der er optaget fra marken ved hjælp af Trimble-enheder. GPS-loggen importeres derefter i en af applikationerne i Trimble Applications Suite. GPS-loggen indeholdt i en SSF bruges til at oprette brugerdefinerede koordinatsystemer. SSF-filer kan åbnes med [Trimble Navigation GPS Pathfinder Office](https://geospatial.trimble.com/en/products/software/office-software), Trimble Navigation GPS Pathfinder Tools SDK og ESRI ArcGIS for Desktop med Trimble GPS Analyst plug-in.

## SSF-filformat - flere oplysninger

Når GPS-data overføres fra Trimble-enheden til computeren til efterbehandling, kombineres alle disse filer til en enkelt .ssf-fil. Denne rå ubehandlede fil bruges af efterbehandlingssoftwaren til at foretage rettelser og hjælpe med datahåndtering.

SSF-filer gemmes på disken som Trimbles proprietære filformat, og dets detaljerede specifikationer er ikke offentligt tilgængelige. Den er specifik for Trimble-enheder og repræsenterer GPS-enhedens data. Indtil dato er der ingen ikke-kommerciel gratis løsning tilgængelig til at læse eller konvertere SSF-filer.

## Referencer

* [Trimble News Release](https://www.trimble.com/news/release.aspx?id=050510b)


