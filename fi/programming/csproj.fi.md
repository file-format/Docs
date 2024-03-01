{
  "date": "2019-10-11",
  "keywords": [
"csproj tiedosto",
"csproj",
"laajennus",
"muoto",
"Mikä on csproj-tiedosto",
"csproj tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSPROJ",
  "description": "Opi CSPROJ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CSPROJ-tiedostoja.",
  "linktitle": "CSPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cspro-fij"
}
},
  "lastmod": "2021-05-21"
}

## Mikä on CSProj-tiedosto?
CSPROJ-laajennuksella varustetut tiedostot edustavat C#-projektitiedostoa, joka sisältää luettelon projektiin sisältyvistä tiedostoista sekä viittaukset järjestelmäkokoonpanoihin. Kun uusi projekti käynnistetään Microsoft VIiual Studiossa, saat yhden .csproj-tiedoston yhdessä pääratkaisutiedoston ([.sln](/programming/sln/)) kanssa. Jos projektissa on useampi kuin yksi kokoonpano, on myös yhtä monta projektitiedostoa, jossa .sln-tiedosto liittää ne kaikki yhteen osana projektia. Tämän tiedoston sisältö määrittelee kaikki projektin rakentamiseen vaadittavat vaatimukset, kuten sisällytettävä sisältö, alustavaatimukset, versiotiedot, verkkopalvelimen tai tietokantapalvelimen asetukset ja suoritettavat tehtävät. Projektitiedoston sisältö on järjestetty XML-tiedostomuotoon ja se voidaan avata missä tahansa tekstieditorissa muokkausta ja katselua varten. Se antaa myös loogisen näkymän projektitiedostoille asianmukaista järjestelyä varten.

## CSPROJ-tiedostomuoto #

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

!{{HYPERLINKKI1}}

Seuraavissa osissa käsitellään projektitiedoston tiedostomuotoelementtejä.

### Projektielementti ###

Elementti [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) on jokaisen projektitiedoston juurielementti. Se tunnistaa projektitiedoston XML-skeeman ja voi sisältää attribuutteja koontiprosessin aloituspisteiden määrittämiseksi.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Ominaisuudet ja ehdot

Ominaisuudet edustavat projektin rakentamiseen tarvittavia tietoja. Tällaiset ominaisuudet määritellään [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx)-elementissä. Nämä ominaisuudet koostuvat avain-arvo-pareista, joissa ominaisuuselementin nimi määrittää ominaisuusavaimen ja elementin sisältö määrittää ominaisuuden arvon. Voit esimerkiksi määrittää ominaisuudet nimeltä ServerName ja ConnectionString tallentamaan staattisen palvelimen nimen ja yhteysmerkkijonon.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Elementtien kautta voidaan määritellä ehtoja elementin arvioinnin kriteerien määrittämiseksi. Tämä määritellään ehtosanalla, kun ominaisuus määritellään alla esitetyllä tavalla:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Kun MSBuild käsittelee tämän ominaisuuden määritelmän, se tarkistaa ensin, onko **$(OutputRoot)**-ominaisuusarvo käytettävissä. Jos ominaisuuden arvo on tyhjä – toisin sanoen käyttäjä ei ole antanut arvoa tälle ominaisuudelle – ehdon arvoksi tulee **true** ja ominaisuuden arvoksi asetetaan **..\Publish\Out.**

### Tuotteet ja tuoteryhmät

Projektitiedosto määrittää rakennusprosessiin syötteet, jotka ovat itse asiassa eri tiedostotyyppejä. MSBuild-nimikkeistössä nämä syötteet esitetään Item-elementeillä ja ne määritellään [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx)-elementissä. Kuten **Property**-elementeille, voit nimetä **Tuote**-elementin haluamallasi tavalla. Sinun on kuitenkin määritettävä **Sisällytä**-attribuutti tunnistaaksesi tiedoston tai jokerimerkin, jota kohde edustaa.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Tavoitteet ja tehtävät

[Task](https://msdn.microsoft.com/library/77f2hx1s.aspx)-elementti edustaa yksittäistä rakennusohjetta (tai tehtävää). MSBuild sisältää useita ennalta määritettyjä tehtäviä. Esimerkiksi:

* **Kopioi** -tehtävä kopioi tiedostot uuteen paikkaan.

* **Csc**-tehtävä kutsuu Visual C# -kääntäjän.

* **Vbc**-tehtävä kutsuu Visual Basic -kääntäjän.

* **Exec**-tehtävä suorittaa tietyn ohjelman.

* **Viesti**-tehtävä kirjoittaa viestin loggeriin.


Tehtävien on aina oltava [Target](https://msdn.microsoft.com/library/t50z2hka.aspx)-elementtien sisällä. **Target**-elementti on joukko yhtä tai useampaa tehtävää, jotka suoritetaan peräkkäin, ja projektitiedosto voi sisältää useita kohteita.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Viitteet

* [Projektitiedoston ymmärtäminen - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- tiedosto)


