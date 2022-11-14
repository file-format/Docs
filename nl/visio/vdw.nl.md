{
  "date" : "2019-10-11",
  "keywords" :[ "vdw", "vdw-bestand", "vdw-bestandsindeling", "vdw-bestandstype", "bestand", "type", "wat is een vdw-bestand" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Visio Graphics Service-bestandsindeling",
  "description":"Meer informatie over VDW-bestandsindelingen en API's die VDW-bestanden kunnen maken en openen.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Wat is een VDW-bestand?

VDW is de Visio Graphics Service-bestandsindeling die de streams en opslag specificeert die nodig zijn voor het renderen van een webtekening. Een webtekening is een verzameling tekenpagina's, vormen, lettertypen, afbeeldingen, gegevensverbindingen en informatie over diagramupdates die als vector- of rastertekening kan worden weergegeven. VDW-bestanden kunnen ook in Microsoft Visio worden geopend, maar worden voornamelijk opgeslagen voor gebruik op internet. Microsoft Visio biedt de mogelijkheid om Visio-bestanden te converteren naar een aantal verschillende bestandsindelingen, waaronder [PNG](/nl/Image/PNG/), [BMP](/nl/Image/BMP/), [PDF](/nl/pdf/) en andere.

## **VDW** Bestandsformaat

De technische specificaties van het VDW-bestandsformaat zijn online beschikbaar door [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) en kunnen door ontwikkelaars worden geraadpleegd voor het maken van toepassingen. Het technische document beschrijft gegevens in een samengesteld bestand dat storages en streams bevat. De weergave van een webtekening wordt mogelijk gemaakt via een stroom, genaamd VisioServerData, via een ZIP-archief. Een ShapGraphic XML Part in het archief beschrijft de grafische elementen die in de webtekening worden weergegeven en worden uitgedrukt in Extensible Application Markup Language (XAML). Een verzameling XML-onderdelen in het ZIP-archief beschrijft de gegevensverbinding van de webtekening, informatie over de vorm en de logica voor het bijwerken van het diagram. Deze delen worden uitgedrukt als XML. Het DataGraphic XML-gedeelte beschrijft herberekende eigenschappen die moeten worden geëvalueerd nadat de gegevens in de webtekening zijn vernieuwd vanuit de gegevensbron. Aanvullende items in het ZIP-archief bevatten informatie over de lettertypen en afbeeldingen die in de webtekening worden gebruikt.

|![Mogelijke implementatie van een bestand](/nl/web/vdw.png "Mogelijke implementatie van een bestand")

## Referenties

* [[MS-VGSFF]: Visio Graphics Service (.vdw) bestandsindeling](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

