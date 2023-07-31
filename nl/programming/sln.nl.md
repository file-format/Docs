{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Meer informatie over SLN-bestandsindeling en API's die SLN-bestanden kunnen maken en openen.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een SLN-bestand?
Een bestand met de extensie .SLN vertegenwoordigt een **Visual Studio-oplossing**-bestand dat informatie over de organisatie van projecten bijhoudt in een oplossingsbestand. De inhoud van zo'n oplossingsbestand wordt in platte tekst in het bestand geschreven en kan worden bekeken/bewerkt door het bestand in een teksteditor te openen. De informatie in een oplossingsbestand blijft persistent en wordt gebruikt om de informatie te laden die bij de oplossing hoort, zoals [projecten ](/nl/programming/csproj/) en alle andere vereiste informatie. De projectbestanden waarnaar wordt verwezen door het oplossingsbestand bevatten aanvullende informatie om de omgeving in staat te stellen de hiërarchie te vullen met de items van dat project. Er worden geen gegevens opgeslagen in het .sln-bestand, hoewel indien nodig projectinformatie naar het .sln-bestand kan worden geschreven.

## **SLN versiegeschiedenis** ##

De versie van de oplossingsindeling is in de loop van de tijd met elke Microsoft Visual Studio-oplossing geëvolueerd. De details hierover zijn als volgt.


|Visual Studio-versie|Versie van oplossingsindeling
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12:00
|2015|12:00
|2017|12:00

### **Inhoud van een oplossingsbestand** ###

Een oplossingsbestand bestaat uit verschillende secties die door de omgeving worden gelezen om het project te laden. Een voorbeeld van de inhoud van een .sln-bestand is zoals hieronder weergegeven.

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

### **Projectverklaring** ###

Een oplossingsbestand kan meer dan één projectdeclaratie bevatten en ook dat van verschillende projecttypes. Een enkel oplossingsbestand kan bijvoorbeeld zowel een CSharp- als een VB.NET-project bevatten. Deze typen worden onderscheiden in een oplossing met behulp van de [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). De bovenstaande projectverklaring kan als volgt worden gegeneraliseerd voor een duidelijk begrip.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` De Project-Type-GUID is uniek voor verschillende projecttypes en wordt gebruikt door de oplossinglezer om het type project te identificeren. In dit geval laat F184B08F-C81C-45F6-A57F-5ABD9991F28F zien dat het een VB.NET-project is.

`Project GUID:` De unieke GUID van het project die het onderscheidt van andere projecten in de oplossing. De unieke ID van een project in de oplossing maakt het voor andere projecten in de oplossing mogelijk om er toegang toe te krijgen.

Op basis van de informatie in de projectsectie van het .sln-bestand laadt de omgeving elk projectbestand. Het project is dan zelf verantwoordelijk voor het vullen van de projecthiërarchie en het laden van geneste projecten. Alle wijzigingen die in de oplossing zijn aangebracht, worden weer opgeslagen in het oplossingsbestand bij het opslaan of sluiten van het project.

## Visual Studio-oplossing VS-project

**Project:** Logischerwijs, wanneer u begint met het maken van een app of software met behulp van Visual Studio, start u een nieuw project. Een project bevat alle benodigde bestanden, zoals broncode, pictogrammen, afbeeldingen, gegevensbestanden en meer, die worden gecompileerd tot een uitvoerbare app, website of bibliotheek.

**Oplossing:** Een oplossing bevat een of meer projecten. De oplossing is dus net een container voor Visual Studio-projecten. Logischerwijs kunnen we zeggen dat iemand een complete oplossing voor zijn bedrijf wil, inclusief een website, desktop-app, rustgevende service en mobiele app.

### **Referenties** ###

* [Oplossingsbestand - door MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [Guid's voor projecttype](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

