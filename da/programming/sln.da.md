{
  "date": "2019-10-11",
  "keywords": [
"sln fil",
"hvordan man kører en sln-fil",
"sln",
"udvidelse",
"format",
"Hvad er sln fil",
"sln filformat",
"Visual Studio-løsning",
"Visual Studio løsning VS projekt"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SLN",
  "description": "Lær om SLN filformat og API'er, der kan oprette og åbne SLN filer.",
  "linktitle": "SLN",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-sl-dan"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er SLN fil?
En fil med filtypenavnet .SLN repræsenterer en **Visual Studio-løsning**-fil, der opbevarer information om organiseringen af projekter i en løsningsfil. Indholdet af en sådan løsningsfil er skrevet i almindelig tekst inde i filen og kan observeres/redigeres ved at åbne filen i en hvilken som helst teksteditor. Oplysningerne indeholdt i en løsningsfil forbliver vedvarende og bruges til at indlæse de oplysninger, der er knyttet til løsningen, såsom [projects ](/programming/csproj/)og alle andre nødvendige oplysninger. Projektfilerne, der refereres til af løsningsfilen, indeholder yderligere oplysninger for at gøre det muligt for miljøet at udfylde hierarkiet med det pågældende projekts elementer. Der gemmes ingen data i .sln-filen, selvom projektinformation kan skrives til .sln-filen, hvis det kræves.

## **SLN-versionshistorik** ##

Løsningsformatversionen har udviklet sig med hver Microsoft Visual Studio-løsning med tiden. Detaljerne om disse er som følger.


|Visual Studio-version|Løsningsformatversion
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Indhold af en løsningsfil** ###

En løsningsfil består af flere sektioner, der læses af miljøet for at indlæse projektet. Et eksempel på .sln-filindhold er som vist nedenfor.

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

### **Projekterklæring** ###

En løsningsfil kan indeholde mere end én projektdeklaration og det også af forskellige projekttyper. For eksempel kan en enkelt løsningsfil indeholde såvel et CSharp- som et VB.NET-projekt. Disse typer skelnes i en løsning, der bruger [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Ovenstående projekterklæring kan generaliseres som følger for en klar forståelse.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID er unikt for forskellige projekttyper og bruges af løsningslæseren til at identificere projekttypen. I dette tilfælde viser F184B08F-C81C-45F6-A57F-5ABD9991F28F, at det er et VB.NET-projekt.

`Projekt GUID:` Den unikke GUID for projektet, der adskiller det fra andre projekter i løsningen. Det unikke ID for et projekt i løsningen gør det muligt for andre projekter i løsningen at få adgang til det.

Baseret på informationen i projektsektionen af .sln-filen, indlæser miljøet hver projektfil. Projektet selv er derefter ansvarlig for at udfylde projekthierarkiet og indlæse eventuelle indlejrede projekter. Eventuelle ændringer i løsningen gemmes tilbage i løsningsfilen ved lagring eller lukning af projektet.

## Visual Studio løsning VS projekt

**Projekt:** Logisk, når du begynder at oprette en app eller software ved at bruge Visual Studio, starter du et nyt projekt. Et projekt indeholder alle nødvendige filer såsom kildekode, ikoner, billeder, datafiler og mere, der vil blive kompileret i en eksekverbar app, hjemmeside eller et bibliotek.

**Løsning:** En løsning indeholder et eller flere projekter. Så løsningen er ligesom en container til Visual Studio-projekter. Logisk set kan vi sige, at nogen ønsker at få en komplet løsning til sin virksomhed, herunder en hjemmeside, desktop-app, afslappende service og mobilapp.

### **Referencer** ###

* [Løsningsfil - af MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)

* [Project Type GUIDs](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)


