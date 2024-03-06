{
  "date": "2019-10-11",
  "keywords": [
"sln fails",
"kā palaist sln failu",
"sln",
"pagarinājumu",
"formātā",
"Kas ir sln fails",
"sln faila formātā",
"Visual Studio risinājums",
"Visual Studio risinājums VS projekts"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SLN",
  "description": "Uzziniet par SLN faila formātu un API, kas var izveidot un atvērt SLN failus.",
  "linktitle": "SLN",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-sl-lvn"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir SLN fails?
Fails ar paplašinājumu .SLN ir **Visual Studio risinājuma** fails, kas risinājuma failā glabā informāciju par projektu organizēšanu. Šāda risinājuma faila saturs faila iekšpusē ir rakstīts vienkāršā tekstā un to var novērot/rediģēt, atverot failu jebkurā teksta redaktorā. Risinājuma failā esošā informācija paliek noturīga un tiek izmantota, lai ielādētu ar risinājumu saistīto informāciju, piemēram, [projects ](/programming/csproj/) un jebkuru citu nepieciešamo informāciju. Projekta faili, uz kuriem atsaucas risinājuma fails, satur papildu informāciju, lai nodrošinātu vidi hierarhijas aizpildīšanai ar šī projekta vienumiem. Dati netiek glabāti .sln failā, lai gan projekta informāciju var ierakstīt .sln failā, ja nepieciešams.

## **SLN versiju vēsture** ##

Risinājuma formāta versija laika gaitā ir attīstījusies ar katru Microsoft Visual Studio risinājumu. Sīkāka informācija par tiem ir šāda.


|Visual Studio versija | Risinājuma formāta versija
---|---|
|2003.|8.00
|2005|9,00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Risinājuma faila saturs** ###

Risinājuma fails sastāv no vairākām sadaļām, kuras nolasa vide, lai ielādētu projektu. Tālāk ir parādīts .sln faila satura paraugs.

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

### **Projekta deklarācija** ###

Risinājuma failā var būt vairāk nekā viena projektu deklarācija un arī dažādu projektu veidu deklarācijas. Piemēram, vienā risinājuma failā var būt gan CSharp, gan VB.NET projekts. Šie veidi tiek izšķirti risinājumā, izmantojot [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Iepriekš minēto projekta deklarāciju skaidras izpratnes labad var vispārināt šādi.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

Projekta tipa GUID: Projekta tipa GUID ir unikāls dažādiem projektu veidiem, un to izmanto risinājuma lasītājs, lai identificētu projekta veidu. Šajā gadījumā F184B08F-C81C-45F6-A57F-5ABD9991F28F parāda, ka tas ir VB.NET projekts.

Projekta GUID: unikāls projekta GUID, kas to atšķir no citiem risinājuma projektiem. Projekta unikālais ID risinājumā ļauj tam piekļūt citiem risinājuma projektiem.

Pamatojoties uz informāciju, kas ietverta .sln faila projekta sadaļā, vide ielādē katru projekta failu. Pēc tam pats projekts ir atbildīgs par projekta hierarhijas aizpildīšanu un visu ligzdoto projektu ielādi. Visas risinājumā veiktās izmaiņas tiek saglabātas atpakaļ risinājuma failā, saglabājot vai aizverot projektu.

## Visual Studio risinājums VS projekts

**Projekts:** Loģiski, ka, sākot veidot lietotni vai programmatūru, izmantojot Visual Studio, jūs sākat jaunu projektu. Projektā ir visi nepieciešamie faili, piemēram, pirmkods, ikonas, attēli, datu faili un daudz kas cits, kas tiks apkopoti izpildāmā lietotnē, vietnē vai bibliotēkā.

**Risinājums:** risinājumā ir viens vai vairāki projekti. Tātad risinājums ir gluži kā Visual Studio projektu konteiners. Loģiski, mēs varam teikt, ka kāds vēlas iegūt pilnīgu risinājumu savam biznesam, tostarp vietni, darbvirsmas lietotni, mierīgu pakalpojumu un mobilo lietotni.

### **Atsauces** ###

* [Risinājuma fails — MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)

* [Projekta tipa GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)


