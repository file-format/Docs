{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Rapportdefinitietaal Client-side",
  "keywords" :[ "rdlc", "rapportdefinitietaal", "mkv-formaat", "XSD", "rapportdefinitietaal clientzijde"],
  "description":"Meer informatie over het RDLC-bestandsformaat dat een XML-weergave is van een SQL Server Reporting Services-rapportdefinitie.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Wat is een RDLC-bestand? ##

De RDLC staat voor Report Definition Language Client side. Het is eigenlijk een extensie van een rapportbestand dat is gemaakt met behulp van Microsoft-rapportagetechnologie. De SQL Server 2005-versie van Report Designer wordt gebruikt om deze bestanden te maken. De **ReportViewer**-besturing aan de clientzijde kan de RDLC-rapporten direct uitvoeren.

## RDL VS RDLC-bestanden
|.rdl-bestanden |.rdlc-bestanden|
---|---|
|RDL-bestanden worden gemaakt door de SQL Server 2005-versie van Report Designer|RDLC-bestanden worden gemaakt door de Visual Studio 2005-versie van Report Designer|
|Het wordt gebruikt in SQL Server Reporting Services|Het wordt gebruikt in Visual Studio|
|Het is een extern rapport|Het is een lokaal rapport|
|Je hebt een Reporting Services-exemplaar nodig om het uit te voeren|Je hebt geen Reporting Services-exemplaar nodig|

## Clientrapportdefinitiebestanden (.rdlc) maken
Het ReportViewer-besturingselement wordt gebruikt om clientrapportdefinitiebestanden (.rdlc) uit te voeren met behulp van de ingebouwde verwerkingscapaciteit van het besturingselement. De clientrapporten die u in de lokale verwerkingsmodus uitvoert, kunnen eenvoudig worden gemaakt in uw toepassingsproject. Hieronder volgen de benaderingen voor het maken van het rapport:

- Gebruik de **Report Wizard** om een nieuwe clientrapportdefinitie (.rdlc) te maken.

- Maak een nieuw clientrapportdefinitiebestand (.rdlc) met behulp van Visual Studio.

- Genereer programmatisch een rapportdefinitie.


U kunt alleen een voorbeeld van een rapport bekijken door het uit te voeren in een **ReportViewer**-besturingselement. Houd er rekening mee dat u de rapportdefinitie op elk moment kunt openen en bewerken en vervolgens de toepassing kunt bouwen of implementeren om de resultaten te controleren.

## Referenties ##

- [Creëren van clientrapportdefinitiebestanden (.rdlc)](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

