{
  "date": "2019-10-11",
  "keywords": [
"sln failą",
"kaip paleisti sln failą",
"sln",
"pratęsimas",
"formatu",
"Kas yra sln failas",
"sln failo formatas",
"Visual Studio sprendimas",
"Visual Studio sprendimas VS projektas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SLN",
  "description": "Sužinokite apie SLN failo formatą ir API, kurios gali kurti ir atidaryti SLN failus.",
  "linktitle": "SLN",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-sl-ltn"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra SLN failas?
Failas su .SLN plėtiniu yra **Visual Studio sprendimo** failas, kuriame informacija apie projektų organizavimą saugoma sprendimo faile. Tokio sprendimo failo turinys yra parašytas paprastu tekstu failo viduje ir gali būti stebimas/redaguojamas atidarius failą bet kuriame teksto rengyklėje. Sprendimo faile esanti informacija išlieka nuolatinė ir naudojama su sprendimu susijusiai informacijai, pvz., [projects ](/programming/csproj/), ir bet kuriai kitai reikalingai informacijai įkelti. Projekto failuose, kuriuose nurodomas sprendimo failas, yra papildomos informacijos, leidžiančios įgalinti aplinką hierarchijai užpildyti to projekto elementais. Jokie duomenys nesaugomi .sln faile, nors projekto informaciją galima įrašyti į .sln failą, jei reikia.

## **SLN versijų istorija** ##

Sprendimo formato versija bėgant laikui buvo tobulinama su kiekvienu Microsoft Visual Studio sprendimu. Išsami informacija apie juos yra tokia.


|Visual Studio versija|Sprendimo formato versija
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Sprendimo failo turinys** ###

Sprendimo failą sudaro keli skyriai, kuriuos aplinka nuskaito, kad įkeltų projektą. Pavyzdinis .sln failo turinys yra toks, kaip parodyta toliau.

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

### **Projekto deklaracija** ###

Sprendimo faile gali būti daugiau nei viena projekto deklaracija ir taip pat skirtingų projektų tipai. Pavyzdžiui, viename sprendimo faile gali būti CSharp ir VB.NET projektas. Šie tipai išskiriami sprendime naudojant [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Aukščiau pateiktą projekto deklaraciją galima apibendrinti taip, kad būtų aiškus supratimas.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

Projekto tipo GUID: Projekto tipo GUID yra unikalus skirtingiems projektų tipams ir jį naudoja sprendimo skaitytuvas, kad nustatytų projekto tipą. Šiuo atveju F184B08F-C81C-45F6-A57F-5ABD9991F28F rodo, kad tai VB.NET projektas.

Projekto GUID: unikalus projekto GUID, išskiriantis jį iš kitų projektų sprendime. Unikalus projekto ID sprendime suteikia galimybę kitiems sprendimo projektams jį pasiekti.

Remdamasi informacija, esančia .sln failo projekto skyriuje, aplinka įkelia kiekvieną projekto failą. Tada pats projektas yra atsakingas už projekto hierarchijos užpildymą ir įkeltų projektų įkėlimą. Visi sprendimo pakeitimai išsaugomi atgal į sprendimo failą išsaugant arba uždarius projektą.

## Visual Studio sprendimas VS projektas

**Projektas:** Logiškai mąstant, kai pradedate kurti programą arba programinę įrangą naudodami Visual Studio, pradedate naują projektą. Projekte yra visi reikalingi failai, tokie kaip šaltinio kodas, piktogramos, vaizdai, duomenų failai ir kt., kurie bus sukompiliuoti į vykdomąją programą, svetainę ar biblioteką.

**Sprendimas:** sprendimą sudaro vienas ar daugiau projektų. Taigi sprendimas yra kaip Visual Studio projektų konteineris. Logiškai mąstant, galime sakyti, kad kažkas nori gauti išsamų sprendimą savo verslui, įskaitant svetainę, darbalaukio programą, ramią paslaugą ir programą mobiliesiems.

### **Nuorodos** ###

* [Sprendimo failas – MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)

* [Projekto tipo GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)


