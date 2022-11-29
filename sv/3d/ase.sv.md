{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","fil", "format", "filtyp", "tillägg","vad är en ASE-fil?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om ASE-filformat och API:er som kan öppna och skapa ASE-filer.",
  "title" :"ASE - Autodesk ASCII Scene Export File",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Vad är ASE fil?

En fil med filtillägget .ase är ett Autodesk ASCII Scene Export-filformat som är en ASCII-representation av en scen, som innehåller 2D- eller 3D-information samtidigt som scendata exporteras med Autodesk. Autodesk erbjuder alternativ för att inkludera scenkomponenter när scendata exporteras. Du kan inkludera Mesh-definition tillsammans med vertex- och ansiktsinformation, materialbeskrivning, transformationsanimeringsdata för objekten, fullständig meshdefinition av varje n bildrutor, animationsdata för kameror och lampor och IK-foginställningar.

## ASE-filformat - Mer information

ASE-filer är textfiler lagrade i ASCII-format som kan öppnas i vilken textredigerare som helst. En ASE-fil kan innehålla följande typer av information som tillhandahålls av Autodesk.

### Utdataalternativ

* `Mesh Definition` - Exporterar definitionen av varje mesh, inklusive vertex- och ansiktsinformation för geometriska objekt. Om du aktiverar detta aktiveras dessutom objekten i grupprutan Mesh Options, som beskrivs nedan.
* 'Material' - Inkluderar materialbeskrivningen. Om ett material inte tilldelas ett objekt, exporteras dess trådramsfärg. Alla nivåer i ett materialträd ingår, så detta kan producera mycket text.
* `Transform Animation Keys` - Inkluderar transformationsanimeringsdata för objekten. Om objektet är en målkamera eller spotlight kommer detta att inkludera målanimationsdata.
* `Animerat mesh` - Exporterar en komplett mesh-definition av varje n bildrutor. Frekvensen specificeras av Controller Output spinner, som beskrivs nedan. Varje block innehåller samma information som anges i grupprutan Mesh Options, som beskrivs nedan. Att aktivera detta kan resultera i en stor fil, även för små scener.
* `Animerad kamera/ljusinställningar` - Exporterar animationsdata för kameror och lampor, som färg, intensitet, falloff, kartbias och så vidare. Matar ut ett block var n:e bildruta, som specificerats av Controller Output-snurran.
* `Inverterade kinematiska leder` - Exporterar IK-foginställningarna i hierarkigrenen.

### Objekttyper

Objekten här låter dig specificera vilken kategori av objekt du vill inkludera i utdata. Du kan inkludera geometriska objekt, former, kameror, lampor och hjälpobjekt.

* Geometrisk
* Former
* Kameror
* Ljus
* Medhjälpare

### Mesh-alternativ

* "Mesh Normals" - Exporterar ansikts- och vertexnormalerna. Ansiktets normala listas först, följt av normalerna för de tre hörn som stöder ansiktet. Att aktivera detta resulterar i en mycket större fil.
* `Mapping Coordinates` - Exporterar en lista över mappande hörn och ansikten, enligt TVert- och TVFace-strukturerna som beskrivs i 3ds Max Software Development Kit. Om ett objekt använder ansiktskartläggning, exporteras en ansiktskartlista som innehåller UVW-koordinater för varje ansikte.
* `Vertex Colors` - Exporterar vertexfärger.

### Controllerutgång

* `Använd nycklar` - Exporterar nyckelvärden. Om styrenheten inte använder nycklar, används Force Sample-metoden. När det gäller transformkontroller fungerar alternativet Använd nycklar endast om alla transformeringskontroller är antingen linjära/TCB eller Bezier. Om ett av transformspåren använder en annan typ av styrenhet, används Force Sample-metoden för alla transformationsspår.
* `Force Samples` - Samplar styrenhetsvärden baserat på den frekvens som anges i Frames per Sample Controller.

## Referenser

* [Autodesk - Exportera till ASCII](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-98B2388D -A3A7-4096-8E81-888A3F9D6069-htm.html)

