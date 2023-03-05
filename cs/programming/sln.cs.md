{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Další informace o formátu souboru SLN a rozhraních API, která mohou vytvářet a otevírat soubory SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor SLN?
Soubor s příponou .SLN představuje soubor řešení **Visual Studio**, který uchovává informace o organizaci projektů v souboru řešení. Obsah takového souboru řešení je zapsán jako prostý text uvnitř souboru a lze jej sledovat/upravovat otevřením souboru v libovolném textovém editoru. Informace obsažené v souboru řešení zůstávají trvalé a používají se k načtení informací spojených s řešením, jako jsou [projekty ](/cs/programming/csproj/) a jakékoli další požadované informace. Soubory projektu, na které odkazuje soubor řešení, obsahují další informace, které umožňují prostředí naplnit hierarchii položkami tohoto projektu. V souboru .sln nejsou uložena žádná data, ačkoli v případě potřeby lze do souboru .sln zapsat informace o projektu.

## **Historie verzí SLN** ##

Verze formátu řešení se postupem času vyvíjela s každým řešením Microsoft Visual Studio. Podrobnosti o nich jsou následující.


|Verze Visual Studio|Verze formátu řešení
---|---|
|2003|8.00
|2005|9.00
|2008|10:00
|2010|11:00
|2013|12.00
|2015|12.00
|2017|12.00

### **Obsah souboru řešení** ###

Soubor řešení se skládá z několika sekcí, které prostředí čte za účelem načtení projektu. Ukázkový obsah souboru .sln je uveden níže.

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

### **Prohlášení o projektu** ###

Soubor řešení může obsahovat více než jednu deklaraci projektů a také různé typy projektů. Jeden soubor řešení může například obsahovat CSharp i projekt VB.NET. Tyto typy se v řešení rozlišují pomocí [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Výše uvedené prohlášení o projektu lze pro jasné pochopení zobecnit následovně.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID je jedinečný pro různé typy projektů a používá jej čtečka řešení k identifikaci typu projektu. V tomto případě F184B08F-C81C-45F6-A57F-5ABD9991F28F ukazuje, že se jedná o projekt VB.NET.

`Project GUID:` Jedinečný GUID projektu, který jej odlišuje od ostatních projektů v řešení. Jedinečné ID projektu v řešení umožňuje přístup k němu dalším projektům v řešení.

Na základě informací obsažených v části projektu souboru .sln prostředí načte každý soubor projektu. Samotný projekt je pak zodpovědný za naplnění hierarchie projektu a načtení všech vnořených projektů. Jakékoli změny provedené v řešení se po uložení nebo zavření projektu uloží zpět do souboru řešení.

## Řešení Visual Studio VS projekt

**Projekt:** Logicky, když začnete vytvářet aplikaci nebo software pomocí sady Visual Studio, spustíte nový projekt. Projekt obsahuje všechny potřebné soubory, jako je zdrojový kód, ikony, obrázky, datové soubory a další, které budou zkompilovány do spustitelné aplikace, webové stránky nebo knihovny.

**Řešení:** Řešení obsahuje jeden nebo více projektů. Řešení je tedy jako kontejner pro projekty sady Visual Studio. Logicky můžeme říci, že někdo chce získat kompletní řešení pro své podnikání včetně webu, desktopové aplikace, odpočinkové služby a mobilní aplikace.

### **Reference** ###

* [Soubor řešení – od MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID typu projektu](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

