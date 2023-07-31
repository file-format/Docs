{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"További információ az SLN fájlformátumról és az SLN-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az SLN fájl?
Az .SLN kiterjesztésű fájl egy **Visual Studio megoldás** fájl, amely megoldásfájlban tárolja a projektek szervezésével kapcsolatos információkat. Egy ilyen megoldásfájl tartalma egyszerű szöveggel van írva a fájlon belül, és a fájl bármely szövegszerkesztőben történő megnyitásával megfigyelhető/szerkeszthető. A megoldásfájlban található információk állandóak maradnak, és a megoldáshoz kapcsolódó információk betöltésére szolgálnak, például [projektek ](/hu/programming/csproj/) és minden más szükséges információ. A megoldásfájl által hivatkozott projektfájlok további információkat tartalmaznak, amelyek lehetővé teszik, hogy a környezet feltöltse a hierarchiát a projekt elemeivel. Az .sln fájlban nem tárolódnak adatok, bár a projektinformációk szükség esetén írhatók az .sln fájlba.

## **SLN verzióelőzmények** ##

A megoldás formátumú verziója az idő múlásával minden Microsoft Visual Studio megoldással fejlődött. Ezekről a részletek a következők.


|Visual Studio verzió | Megoldás formátumú verziója
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Egy megoldásfájl tartalma** ###

A megoldásfájl több szakaszból áll, amelyeket a környezet beolvas a projekt betöltéséhez. Egy minta .sln fájl tartalma az alábbiak szerint látható.

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

### **Projektnyilatkozat** ###

Egy megoldásfájl egynél több projektdeklarációt tartalmazhat, és azt is, hogy különböző projekttípusok vannak. Például egyetlen megoldásfájl tartalmazhat egy CSharp- és egy VB.NET-projektet is. Ezeket a típusokat a [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) használó megoldásokban különböztetjük meg. A fenti projektnyilatkozat az alábbiak szerint általánosítható az egyértelmű megértés érdekében.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` A Project-Type-GUID egyedi a különböző projekttípusokhoz, és a megoldásolvasó használja a projekt típusának azonosítására. Ebben az esetben az F184B08F-C81C-45F6-A57F-5ABD9991F28F azt mutatja, hogy ez egy VB.NET projekt.

`Project GUID:` A projekt egyedi GUID-je, amely megkülönbözteti a megoldásban található többi projekttől. A megoldásban található projekt egyedi azonosítója lehetővé teszi, hogy a megoldásban lévő többi projekt hozzáférjen hozzá.

Az .sln fájl projektrészében található információk alapján a környezet betölti az egyes projektfájlokat. Ezután maga a projekt felelős a projekthierarchia feltöltéséért és a beágyazott projektek betöltéséért. A megoldáson végzett minden módosítás a projekt mentése vagy bezárása után visszakerül a megoldásfájlba.

## Visual Studio megoldás VS projekt

**Projekt:** Logikus, hogy amikor elkezd egy alkalmazást vagy szoftvert létrehozni a Visual Studio használatával, új projektet indít. A projekt tartalmazza az összes szükséges fájlt, például forráskódot, ikonokat, képeket, adatfájlokat és egyebeket, amelyeket végrehajtható alkalmazásba, webhelybe vagy könyvtárba fordítanak.

**Megoldás:** Egy megoldás egy vagy több projektet tartalmaz. A megoldás tehát olyan, mint egy konténer a Visual Studio projektekhez. Logikusan azt mondhatjuk, hogy valaki komplett megoldást szeretne kapni vállalkozása számára, beleértve a webhelyet, az asztali alkalmazást, a pihentető szolgáltatást és a mobilalkalmazást.

### **Referenciák** ###

* [Megoldásfájl – MSDN-től](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [Project Type GUIDs](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

