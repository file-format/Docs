{
  "date": "2019-10-11",
  "keywords": [
"sln tiedosto",
"kuinka ajaa sln-tiedosto",
"sln",
"laajennus",
"muoto",
"Mikä on sln-tiedosto",
"sln tiedostomuoto",
"Visual Studio -ratkaisu",
"Visual Studio ratkaisu VS projekti"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SLN",
  "description": "Opi SLN-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SLN-tiedostoja.",
  "linktitle": "SLN",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-sl-fin"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on SLN-tiedosto?
Tiedosto, jonka pääte on .SLN, edustaa **Visual Studio -ratkaisua** -tiedostoa, joka säilyttää tiedot projektien organisoinnista ratkaisutiedostossa. Tällaisen ratkaisutiedoston sisältö kirjoitetaan pelkkänä tekstinä tiedoston sisään ja sitä voi tarkkailla/muokata avaamalla tiedoston missä tahansa tekstieditorissa. Ratkaisutiedoston sisältämät tiedot pysyvät pysyvinä, ja niitä käytetään ratkaisuun liittyvien tietojen, kuten [projects ](/programming/csproj/)ja muiden vaadittujen tietojen lataamiseen. Ratkaisutiedoston viittaamat projektitiedostot sisältävät lisätietoja, jotka mahdollistavat ympäristön hierarkian täyttämiseksi kyseisen projektin kohteilla. .sln-tiedostoon ei tallenneta tietoja, vaikka projektitiedot voidaan kirjoittaa .sln-tiedostoon tarvittaessa.

## **SLN-versiohistoria** ##

Ratkaisumuotoversio on kehittynyt jokaisen Microsoft Visual Studio -ratkaisun kanssa ajan myötä. Yksityiskohdat näistä ovat seuraavat.


|Visual Studion versio|Ratkaisumuodon versio
---|---|
|2003|8.00
|2005|9,00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Ratkaisutiedoston sisältö** ###

Ratkaisutiedosto koostuu useista osista, jotka ympäristö lukee projektin lataamiseksi. Esimerkki .sln-tiedoston sisällöstä on alla kuvattu.

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

### **Hankeilmoitus** ###

Ratkaisutiedosto voi sisältää useamman kuin yhden projektiselvityksen ja myös erilaisia projektityyppejä. Esimerkiksi yksi ratkaisutiedosto voi sisältää CSharp-projektin sekä VB.NET-projektin. Nämä tyypit erotetaan ratkaisussa, jossa käytetään {{HYPERLINKKI}}. Yllä oleva hankeselostus voidaan yleistää seuraavasti selkeän ymmärtämisen vuoksi.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID on ainutlaatuinen eri projektityypeille, ja ratkaisun lukija käyttää sitä projektin tyypin tunnistamiseen. Tässä tapauksessa F184B08F-C81C-45F6-A57F-5ABD9991F28F osoittaa, että kyseessä on VB.NET-projekti.

`Project GUID:` Projektin ainutlaatuinen GUID, joka erottaa sen muista ratkaisun projekteista. Ratkaisussa olevan projektin yksilöllinen tunnus mahdollistaa muiden ratkaisun projektien pääsyn siihen.

Ympäristö lataa jokaisen projektitiedoston .sln-tiedoston projektiosiossa olevien tietojen perusteella. Projekti itse vastaa sitten projektihierarkian täyttämisestä ja mahdollisten sisäkkäisten projektien lataamisesta. Kaikki ratkaisuun tehdyt muutokset tallennetaan takaisin ratkaisutiedostoon projektin tallennuksen tai sulkemisen yhteydessä.

## Visual Studio ratkaisu VS projekti

**Projekti:** Loogisesti, kun aloitat sovelluksen tai ohjelmiston luomisen Visual Studion avulla, aloitat uuden projektin. Projekti sisältää kaikki tarvittavat tiedostot, kuten lähdekoodin, kuvakkeet, kuvat, datatiedostot ja paljon muuta, jotka käännetään suoritettavaksi sovellukseksi, verkkosivustoksi tai kirjastoksi.

**Ratkaisu:** Ratkaisu sisältää yhden tai useamman projektin. Joten ratkaisu on kuin kontti Visual Studio -projekteille. Loogisesti voidaan sanoa, että joku haluaa saada yritykselleen täydellisen ratkaisun, joka sisältää verkkosivuston, työpöytäsovelluksen, rentouttavan palvelun ja mobiilisovelluksen.

### **Referenssit** ###

* [Ratkaisutiedosto – MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)

* [Projektityypin GUID:t](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)


