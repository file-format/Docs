{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Aflați despre formatul de fișier SLN și despre API-urile care pot crea și deschide fișiere SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este fișierul SLN?
Un fișier cu extensia .SLN reprezintă un fișier **Soluție Visual Studio** care păstrează informații despre organizarea proiectelor într-un fișier de soluție. Conținutul unui astfel de fișier de soluție este scris în text simplu în interiorul fișierului și poate fi observat/editat prin deschiderea fișierului în orice editor de text. Informațiile conținute într-un fișier de soluție rămân persistente și sunt folosite pentru a încărca informațiile asociate cu soluția, cum ar fi [projects ](/ro/programming/csproj/)și orice alte informații necesare. Fișierele de proiect la care se face referire de fișierul de soluție conțin informații suplimentare pentru a permite mediului pentru popularea ierarhiei cu elementele proiectului respectiv. Nu sunt stocate date în fișierul .sln, deși informațiile despre proiect pot fi scrise în fișierul .sln dacă este necesar.

## **Istoricul versiunilor SLN** ##

Versiunea formatului de soluție a evoluat cu fiecare soluție Microsoft Visual Studio cu trecerea timpului. Detaliile despre acestea sunt următoarele.


|Versiune Visual Studio|Versiune format soluție
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Conținutul unui fișier de soluție** ###

Un fișier de soluție constă din mai multe secțiuni care sunt citite de mediu pentru a încărca proiectul. Un exemplu de conținut de fișier .sln este prezentat mai jos.

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

### **Declarația de proiect** ###

Un fișier de soluție poate conține mai mult de o declarație de proiecte și aceea de diferite tipuri de proiecte. De exemplu, un singur fișier de soluție poate conține un proiect CSharp, precum și un proiect VB.NET. Aceste tipuri sunt distinse într-o soluție folosind [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Declarația de proiect de mai sus poate fi generalizată după cum urmează pentru o înțelegere clară.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID este unic pentru diferite tipuri de proiecte și este folosit de cititorul de soluții pentru a identifica tipul de proiect. În acest caz, F184B08F-C81C-45F6-A57F-5ABD9991F28F arată că este un proiect VB.NET.

`Project GUID:` GUID-ul unic al proiectului care îl diferențiază de alte proiecte din soluție. ID-ul unic al unui proiect din soluție face posibil ca alte proiecte din soluție să-l acceseze.

Pe baza informațiilor conținute în secțiunea de proiect a fișierului .sln, mediul încarcă fiecare fișier de proiect. Proiectul în sine este apoi responsabil pentru popularea ierarhiei proiectului și încărcarea oricăror proiecte imbricate. Orice modificări aduse soluției sunt salvate înapoi în fișierul soluției la salvarea sau închiderea proiectului.

## Soluția Visual Studio VS proiect

**Proiect:** În mod logic, când începeți să creați o aplicație sau un software utilizând Visual Studio, începeți un nou proiect. Un proiect conține toate fișierele necesare, cum ar fi codul sursă, pictograme, imagini, fișiere de date și multe altele, care vor fi compilate într-o aplicație executabilă, un site web sau o bibliotecă.

**Soluție:** O soluție conține unul sau mai multe proiecte. Deci soluția este la fel ca un container pentru proiecte Visual Studio. În mod logic, putem spune că cineva dorește să obțină o soluție completă pentru afacerea sa, inclusiv un site web, o aplicație desktop, un serviciu odihnitor și o aplicație mobilă.

### **Referințe** ###

* [Fișier de soluție - de MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID-uri tip proiect](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

