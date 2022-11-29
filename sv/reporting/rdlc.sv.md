{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Report Definition Language Client-side",
  "keywords" :[ "rdlc", "rapportdefinitionsspråk", "mkv-format", "XSD", "rapportdefinitionsspråk klientsida"],
  "description":"Läs mer om RDLC-filformat som är en XML-representation av en rapportdefinition för SQL Server Reporting Services.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Vad är en RDLC fil? ##

RDLC står för Report Definition Language Client side. Egentligen är det en förlängning av rapportfilen skapad med hjälp av Microsofts rapportteknik. SQL Server 2005-versionen av Report Designer används för att skapa dessa filer. **ReportViewer**-kontrollen på klientsidan kan exekvera RDLC-rapporterna direkt.

## RDL VS RDLC-filer
|.rdl-filer |.rdlc-filer|
---|---|
|RDL-filer skapas av SQL Server 2005-versionen av Report Designer|RDLC-filer skapas av Visual Studio 2005-versionen av Report Designer|
|Det används i SQL Server Reporting Services|Det används i Visual Studio|
|Det är en fjärrrapport|Det är en lokal rapport|
|Behöver en Reporting Services-instans för att köra den|Ingen Reporting Services-instans behövs|

## Skapa klientrapportdefinitionsfiler (.rdlc).
ReportViewer-kontrollen används för att köra klientrapportdefinitionsfiler (.rdlc) med hjälp av kontrollens inbyggda bearbetningskapacitet. Klientrapporter som du kör i lokalt bearbetningsläge kan enkelt skapas i ditt applikationsprojekt. Följande är metoderna för att skapa rapporten:

- Använd **Rapportguiden** för att skapa en ny klientrapportdefinition (.rdlc).

- Skapa en ny klientrapportdefinitionsfil (.rdlc) med hjälp av Visual Studio.

- Skapa en rapportdefinition programmatiskt.


Du kan bara förhandsgranska en rapport genom att köra den i en **ReportViewer**-kontroll. Observera att du kan öppna och redigera rapportdefinitionen när som helst och sedan bygga eller distribuera programmet för att kontrollera resultaten.

## Referenser ##

- [Skapa klientrapportdefinitionsfiler (.rdlc)](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

