{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "file", "extension", "file format", "VB Project File", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"További információ a VBPROJ fájlformátumról és az API-król, amelyek VBPROJ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az a VBPROJ fájl?

A .vbproj kiterjesztésű fájl egy Microsoft Visual Basic projektfájl, amelyet a Microsoft MSBuild motorja használ a projektek Visual Studio megoldáson belüli felépítéséhez. Hasonló a [CSPROJ](/hu/programming/csproj/) fájlhoz a [C#](/hu/programming/cs/) nyelven írt .NET projektekhez. Az MSBuild motor kiolvassa a különböző csoportokban lévő információkat a VBPROJ fájlokból, és létrehozza a kimeneti fájlt. A VBPROJ fájl a projektet meghatározó globális azonosítókkal, osztályokkal és tulajdonságokkal kapcsolatos információkat tartalmazhat. A VBPROJ fájlok megnyithatók és szerkeszthetők a Microsoft Visual Studio és bármely általános szövegszerkesztő, például a Windows és MacOS operációs rendszeren futó Notepad segítségével.

## VBPROJ fájlformátum - További információ

A VBPROJ fájlok olyan szöveges fájlok, amelyeket [XML](/hu/web/xml/) fájlformátumban írtak az [MSBuild XML séma] alapján (https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild- project-file-schema-reference?view=vs-2019). A VBPROJ fájl XML-címkék formájában tartalmaz információkat, amelyek az adott beállításcsoporthoz kapcsolódó információkat határoznak meg. Erősen ajánlott ezeket a beállításokat a Microsoft Visual Studio IDE-ben megnyitni és szerkeszteni.

### VBPROJ elemek

A VB Settings fájl alkotóelemei a következő képen láthatók.

{{< figure src="../vbproj.png" alt="VBPROJ fájlformátum" >}}

Az alábbi táblázat röviden ismerteti ezeket az elemeket.

|Elem|Leírás|
---|---|
|Projekt| Minden projektfájl gyökéreleme, és attribútumokat is tartalmazhat a felépítési folyamat belépési pontjainak megadásához, valamint a projektfájl XML-sémájának azonosításához|
|Tulajdonságok és feltételek| A tulajdonságok kulcs-érték párokból állnak, és egy PropertyGroup elemben vannak meghatározva. A tulajdonságelem neve a tulajdonságkulcsot jelöli, az elem tartalma pedig a tulajdonság értékét határozza meg.|
|Elemek és ItemGroups|A projektfájlban lévő elemek a felépítési folyamat bemenetei, például fájl-kód fájlok, konfigurációs fájlok, parancsfájlok és a felépítési folyamat részeként szükséges egyéb elemek. Az elemeket egy ItemGroup elemen belül kell meghatározni.|
|Célok és feladatok| A Task elem egy egyedi felépítési utasítást (vagy feladatot) jelent. Az MSBuild számos előre definiált feladatot tartalmaz, mint például a Copy, CSC, VBC, Exec. A feladatoknak mindig egy „Target” elemnek kell lennie, amely egy vagy több egymás után végrehajtott feladat halmaza, és egy projektfájl több célt is tartalmazhat.|

## Hivatkozások

* [A projektfájl ismertetése](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild Schema Elements](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

