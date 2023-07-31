{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC – Jelentésdefiníciós nyelv ügyféloldali",
  "keywords" :[ "rdlc", "jelentésdefiníciós nyelv", "mkv formátum", "XSD", "jelentésdefiníciós nyelv ügyféloldala"],
  "description":"További információ az RDLC fájlformátumról, amely az SQL Server Reporting Services jelentésdefiníciójának XML reprezentációja.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Mi az RDLC fájl? ##

Az RDLC a Report Definition Language Client oldal rövidítése. Valójában ez a jelentésfájl kiterjesztése, amelyet a Microsoft jelentéskészítési technológiájával hoztak létre. A fájlok létrehozásához a Report Designer SQL Server 2005 verzióját használják. Az ügyféloldali **ReportViewer** vezérlő közvetlenül képes végrehajtani az RDLC jelentéseket.

## RDL VS RDLC fájlok
|.rdl fájlok |.rdlc fájlok|
---|---|
|RDL-fájlokat a Report Designer SQL Server 2005-ös verziója hozza létre|Az RDLC-fájlokat a Report Designer Visual Studio 2005-ös verziója hozza létre|
|Az SQL Server Reporting Servicesben használatos|A Visual Studio|ban használatos
|Ez egy távoli jelentés|Ez egy helyi jelentés|
|Futtatásához szükség van egy Reporting Services-példányra|Nincs szükség Reporting Services-példányra|

## Ügyféljelentés-definíciós (.rdlc) fájlok létrehozása
A ReportViewer vezérlő az ügyféljelentés-definíciós (.rdlc) fájlok futtatására szolgál a vezérlő beépített feldolgozási képességének használatával. A helyi feldolgozási módban futtatott ügyféljelentések könnyen létrehozhatók az alkalmazásprojektben. A jelentés elkészítésének módjai a következők:

- A **Jelentésvarázsló** segítségével hozzon létre egy új ügyféljelentés-definíciót (.rdlc).

- Hozzon létre egy új ügyféljelentés-definíciós (.rdlc) fájlt a Visual Studio használatával.

- Jelentésdefiníció generálása programozottan.


A jelentés előnézetét csak a **ReportViewer** vezérlőben futtatva tekintheti meg. Felhívjuk figyelmét, hogy a jelentésdefiníciót bármikor megnyithatja és szerkesztheti, majd az eredmények ellenőrzéséhez létrehozhatja vagy telepítheti az alkalmazást.

## Referenciák ##

- [Creating Client Report Definition (.rdlc) fájlok](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

