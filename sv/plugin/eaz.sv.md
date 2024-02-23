{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ-fil - Vad är en EAZ-fil och hur öppnar man den?",
  "description":"Lär dig mer om EAZ-filformat och API:er som kan skapa och öppna EAZ-filer.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-svz"
}
},
  "lastmod" : "2023-12-23"
}

## Vad är EAZ fil?

EAZ-filen är en tilläggsfil som används av ArcGIS Explorer, en gratis applikation utvecklad av ESRI för kartutforskning, visualisering och delning. Den innehåller ett komprimerat filarkiv som innehåller en [XML file](/web/xml/), kompilerad kod och stödfiler som krävs för tillägget. Dessa filer används för att utöka basfunktionaliteten i programvaran genom att införliva nya knappar, dockningsbara fönster och andra tillägg.

## EAZ-filformat - Mer information

EAZ-filer skapas med hjälp av ArcGIS Explorer SDK, ett utvecklingskit designat för att skapa anpassade funktioner inom ArcGIS Explorer. Dessa filer använder [ZIP](/compression/zip/)-komprimering för att effektivt paketera innehållet. I kärnan av arkivet finns filen **Addins.xml** i rotkatalogen och fungerar som en viktig komponent som beskriver och beskriver de olika anpassningarna som är inbäddade i EAZ-filen.

Filen Addins.xml fungerar i huvudsak som en färdplan och ger insikter i de specifika förbättringar, modifieringar och tillägg som EAZ-filen introducerar till ArcGIS Explorer. Genom denna omfattande struktur kan utvecklare kapsla in och sömlöst integrera nya funktioner, knappar och dockningsbara fönster, vilket förbättrar den övergripande funktionaliteten och användarupplevelsen av ArcGIS Explorer-applikationen.

## Referenser

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
