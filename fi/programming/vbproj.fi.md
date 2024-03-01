{
  "date": "2019-10-11",
  "keywords": [
"vbproj",
"tiedosto",
"laajennus",
"tiedosto muoto",
"VB-projektitiedosto",
"Ohjelmointiopas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VBPROJ",
  "description": "Opi VBPROJ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VBPROJ-tiedostoja.",
  "linktitle": "VBPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbpro-fij"
}
},
  "lastmod": "2020-09-10"
}

## Mikä on VBPROJ-tiedosto?

Tiedosto, jonka laajennus on .vbproj, on Microsoft Visual Basic -projektitiedosto, jota Microsoftin MSBuild-moottori käyttää projektien rakentamiseen Visual Studio -ratkaisussa. Se on samanlainen kuin [CSPROJ](/programming/csproj/)-tiedosto .NET-projekteille, jotka on kirjoitettu kielellä [C#](/programming/cs/). MSBuild-moottori lukee VBPROJ-tiedostoista eri ryhmiin sisältyvät tiedot ja luo tulostiedoston. VBPROJ-tiedosto voi sisältää tietoja, jotka liittyvät yleisiin tunnisteisiin, luokkiin ja ominaisuuksiin, jotka määrittävät projektin. VBPROJ-tiedostoja voidaan avata ja muokata Microsoft Visual Studiolla ja millä tahansa yleisellä tekstieditorilla, kuten Notepad Windows- ja MacOS-käyttöjärjestelmissä.

## VBPROJ-tiedostomuoto - lisätietoja

VBPROJ-tiedostot ovat tekstitiedostoja, jotka on kirjoitettu tiedostomuodossa [XML](/web/xml/), joka perustuu [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). VBPROJ-tiedosto sisältää tietoja XML-tunnisteiden muodossa, jotka määrittelevät kyseiseen asetusryhmään liittyvät tiedot. On erittäin suositeltavaa avata ja muokata nämä asetustiedostot Microsoft Visual Studio IDE:ssä.

### VBPROJ-elementit

VB-asetustiedoston osatekijät ovat seuraavan kuvan mukaiset.

{{< figure src="../vbproj.png" alt="VBPROJ tiedostomuoto" >}}

The following table gives a brief description of these elements.

|Elementti|Kuvaus|
---|---|
|Projekti| Jokaisen projektitiedoston juurielementti ja se voi sisältää attribuutteja, jotka määrittävät koontiprosessin aloituspisteet projektitiedoston XML-skeeman tunnistamisen lisäksi|
|Ominaisuudet ja ehdot| Ominaisuudet koostuvat avainarvopareista ja ne määritellään PropertyGroup-elementissä. Ominaisuuselementin nimi edustaa ominaisuusavainta ja elementin sisältö määrittää ominaisuuden arvon.|
|Items and ItemGroups|Projektitiedoston kohteet ovat koontiprosessin syötteitä, kuten tiedostot-kooditiedostot, määritystiedostot, komentotiedostot ja muut, joita tarvitaan osana koontiprosessia. Kohteet ovat ja ne on määritettävä ItemGroup-elementissä.|
|Tavoitteet ja tehtävät| Task-elementti edustaa yksittäistä rakennusohjetta (tai tehtävää). MSBuild sisältää lukuisia ennalta määritettyjä tehtäviä, kuten Copy, CSC, VBC, Exec. Tehtävien tulee aina sisältyä `Target`-elementtiin, joka koostuu yhdestä tai useammasta peräkkäin suoritettavasta tehtävästä, ja projektitiedosto voi sisältää useita kohteita.|

## Viitteet

* [Projektitiedoston ymmärtäminen](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

* [MSBuild Schema Elements](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)


