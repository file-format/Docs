{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Läs mer om SLN-filformat och API:er som kan skapa och öppna SLN-filer.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är SLN fil?
En fil med tillägget .SLN representerar en **Visual Studio-lösning**-fil som lagrar information om organisationen av projekt i en lösningsfil. Innehållet i en sådan lösningsfil skrivs i vanlig text inuti filen och kan observeras/redigeras genom att öppna filen i valfri textredigerare. Informationen i en lösningsfil förblir beständig och används för att ladda informationen som är associerad med lösningen, såsom [projects ](/sv/programming/csproj/) och all annan nödvändig information. Projektfilerna som hänvisas till av lösningsfilen innehåller ytterligare information för att miljön ska kunna fylla hierarkin med det projektets objekt. Ingen data lagras i .sln-filen, även om projektinformation kan skrivas till .sln-filen vid behov.

## **SLN-versionshistorik** ##

Lösningsformatversionen har utvecklats med varje Microsoft Visual Studio-lösning med tiden. Detaljerna om dessa är följande.


|Visual Studio Version|Lösningsformatversion
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Innehållet i en lösningsfil** ###

En lösningsfil består av flera sektioner som läses av miljön för att ladda projektet. Ett exempel på .sln-filinnehållet är som visas nedan.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Projektförklaring** ###

En lösningsfil kan innehålla mer än en projektdeklaration och det också av olika projekttyper. Till exempel kan en enda lösningsfil innehålla såväl ett CSharp- som ett VB.NET-projekt. Dessa typer särskiljs i en lösning som använder [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Ovanstående projektdeklaration kan generaliseras enligt följande för tydlig förståelse.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID är unikt för olika projekttyper och används av lösningsläsaren för att identifiera typen av projekt. I det här fallet visar F184B08F-C81C-45F6-A57F-5ABD9991F28F att det är ett VB.NET-projekt.

`Project GUID:` Den unika GUID för projektet som skiljer det från andra projekt i lösningen. Det unika ID:t för ett projekt i lösningen gör det möjligt för andra projekt i lösningen att komma åt det.

Baserat på informationen i projektdelen av .sln-filen, laddar miljön varje projektfil. Projektet självt ansvarar sedan för att fylla i projekthierarkin och ladda eventuella kapslade projekt. Eventuella ändringar som görs i lösningen sparas tillbaka till lösningsfilen när du sparar eller stänger projektet.

## Visual Studio-lösning VS-projekt

**Projekt:** Logiskt, när du börjar skapa en app eller programvara med hjälp av Visual Studio, startar du ett nytt projekt. Ett projekt innehåller alla nödvändiga filer som källkod, ikoner, bilder, datafiler och mer, som kommer att kompileras till en körbar app, webbplats eller ett bibliotek.

**Lösning:** En lösning innehåller ett eller flera projekt. Så lösningen är precis som en behållare för Visual Studio-projekt. Logiskt sett kan vi säga att någon vill få en komplett lösning för sin verksamhet inklusive en webbplats, stationär app, vilsam service och mobilapp.

### **Referenser** ###

* [Lösningsfil - av MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [Project Type GUIDs](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

