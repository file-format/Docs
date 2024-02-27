{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ fil - Hvad er en EAZ fil, og hvordan åbner man den?",
  "description":"Lær om EAZ filformat og API'er, der kan oprette og åbne EAZ filer.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-daz"
}
},
  "lastmod" : "2023-12-23"
}

## Hvad er EAZ fil?

EAZ-filen er en tilføjelsesfil, der bruges af ArcGIS Explorer, en gratis applikation udviklet af ESRI til kortudforskning, visualisering og deling. Det indeholder et komprimeret filarkiv, der inkluderer en [XML file](/web/xml/), kompileret kode og understøttende filer, der er nødvendige for tilføjelsen. Disse filer bruges til at udvide softwarens basisfunktionalitet ved at inkorporere nye knapper, dockbare vinduer og andre udvidelser.

## EAZ-filformat - flere oplysninger

EAZ-filer oprettes ved at bruge ArcGIS Explorer SDK, et udviklingskit designet til at skabe brugerdefinerede funktioner i ArcGIS Explorer. Disse filer bruger [ZIP](/compression/zip/)-komprimering til effektivt at pakke deres indhold. I kernen af arkivet findes **Addins.xml**-filen i rodmappen og fungerer som en vital komponent, der skitserer og detaljerer de forskellige tilpasninger, der er indlejret i EAZ-filen.

Addins.xml-filen fungerer i det væsentlige som en køreplan, der giver indsigt i de specifikke forbedringer, ændringer og udvidelser, som EAZ-filen introducerer til ArcGIS Explorer. Gennem denne omfattende struktur kan udviklere indkapsle og problemfrit integrere nye funktioner, knapper og dockable vinduer, hvilket forbedrer den overordnede funktionalitet og brugeroplevelse af ArcGIS Explorer-applikationen.

## Referencer

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
