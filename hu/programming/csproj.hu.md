{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"További információ a CSPROJ fájlformátumról és az API-król, amelyek CSPROJ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Mi az a CSProj fájl?
A CSPROJ kiterjesztésű fájlok egy C# projektfájlt képviselnek, amely tartalmazza a projektben szereplő fájlok listáját a rendszerösszeállításokra való hivatkozásokkal együtt. Amikor új projektet kezdeményez a Microsoft VIiual Studio programban, egy .csproj fájlt kap a fő megoldás ([.sln](/hu/programming/sln/)) fájl mellett. Ha egy projektben egynél több összeállítás van, akkor azonos számú projektfájl is lesz, ahol az .sln fájl mindegyiket összekapcsolja a projekt részeként. Ennek a fájlnak a tartalma meghatározza a projekt felépítéséhez szükséges összes követelményt, például a tartalmazandó tartalmat, a platformkövetelményeket, a verziószámítási információkat, a webszerver- vagy adatbázis-kiszolgáló beállításait és az elvégzendő feladatokat. A projektfájl tartalma XML fájlformátumban van elrendezve, és bármely szövegszerkesztőben megnyitható szerkesztésre és megtekintésre. Logikus nézetet ad a projektfájloknak a megfelelő elrendezéshez.

## CSPROJ fájlformátum száma

A fejlesztők maguk is létrehozhatnak projektfájlokat az [MSBuild XML séma](https://msdn.microsoft.com/library/5dy88c2e.aspx) tiszteletben tartásával. A projektfájlok nyílt és átlátható szerkezete lehetővé teszi az alkalmazásfejlesztők számára, hogy kifinomult és finoman szabályozzák a projektek felépítését és telepítését. Egy ilyen projektfájl tartalma nagyon egyértelmű kapcsolatban áll egymással. A következő ábra egy ilyen projektfájl kulcsfontosságú elemeit és ezek közötti kapcsolatot mutatja be.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

A következő szakaszok a projektfájl fájlformátum-elemeit dolgozzák fel.

### Projektelem ###

A [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) elem minden projektfájl gyökéreleme. Azonosítja a projektfájl XML-sémáját, és attribútumokat is tartalmazhat az összeállítási folyamat belépési pontjainak megadásához.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Tulajdonságok és feltételek

A tulajdonságok jelentik a projekt felépítéséhez szükséges információkat. Az ilyen tulajdonságokat a [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) elem határozza meg. Ezek a tulajdonságok kulcs-érték párokból állnak, ahol a tulajdonságelem neve határozza meg a tulajdonságkulcsot, és az elem tartalma határozza meg a tulajdonság értékét. Például megadhat a Kiszolgálónév és a ConnectionString nevű tulajdonságokat statikus kiszolgálónév és kapcsolati karakterlánc tárolására.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Elemeken keresztül a feltételek megadhatók az elem értékelési kritériumainak megadása érdekében. Ezt a Feltétel szó határozza meg, miközben az alábbiak szerint definiálja a tulajdonságot:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Amikor az MSBuild feldolgozza ezt a tulajdonságdefiníciót, először ellenőrzi, hogy elérhető-e **$(OutputRoot)** tulajdonságérték. Ha a tulajdonság értéke üres – más szóval a felhasználó nem adott meg értéket ehhez a tulajdonsághoz –, a feltétel kiértékelése **true**, a tulajdonság értéke pedig **..\Publish\Out.**

### Tételek és cikkcsoportok

A projektfájl az építési folyamat bemeneteit határozza meg, amelyek valójában különböző fájltípusok. Az MSBuild nómenklatúrában ezeket a bemeneteket Item elemek képviselik, és egy [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) elemen belül vannak meghatározva. A **Tulajdon** elemekhez hasonlóan az **Elem** elemeket is tetszés szerint nevezheti el. Azonban meg kell adnia egy **Include** attribútumot az elem által képviselt fájl vagy helyettesítő karakter azonosításához.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Célok és feladatok

A [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) elem egy egyedi összeállítási utasítást (vagy feladatot) jelent. Az MSBuild számos előre meghatározott feladatot tartalmaz. Például:

* A **Másolás** feladat a fájlokat új helyre másolja.
* A **Csc** feladat meghívja a Visual C# fordítót.
* A **Vbc** feladat meghívja a Visual Basic fordítót.
* Az **Exec** feladat egy megadott programot futtat.
* Az **Üzenet** feladat üzenetet ír egy naplózónak.

A feladatoknak mindig a [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) elemekben kell szerepelniük. A **Target** elem egy vagy több feladat halmaza, amelyek egymás után kerülnek végrehajtásra, és egy projektfájl több célt is tartalmazhat.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Hivatkozások

* [A projektfájl ismertetése – MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- fájl)

