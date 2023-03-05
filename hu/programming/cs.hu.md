{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "file", "extension", "file format", "CSharp", "Programming Language" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - CSharp Code File",
  "description":"További információ a CS fájlformátumról és az API-król, amelyek CS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a CS fájl?

A .cs kiterjesztésű fájlok a C# programozási nyelv forráskódjai. A Microsoft által a .NET-keretrendszerrel való használatra bevezetett fájlformátum az alacsony szintű programozási nyelvet biztosítja a kód írásához, amelyet a végső kimeneti fájl EXE vagy DLL formátumban történő előállításához fordítanak le. Ezeket a Microsoft Visual Studio programmal lehet létrehozni és lefordítani. A Microsoft Visual Studio Express is használható ilyen fájlok létrehozására és frissítésére, amely egy ingyenes IDE. A CS-fájlokat olyan alkalmazások fejlesztésére használják, amelyek az egyszerű asztali alkalmazásoktól a bonyolultabb programokig terjedhetnek. Egy egyszerű Visual Studio projekt [megoldás](/hu/programing/sln/), amelyet C# nyelvvel hoztak létre, egy vagy több ilyen fájlból állhat. A fordításba való felvételre megjelölt fájlok a [CSPROJ](/hu/programming/csproj/) fájlban vannak felsorolva, amely a projekt részét képezi, és utasítja a fordítót a megjelölt fájlok használatára.

## CS fájlformátum ##

A CS fájlok szöveg alapú fájlformátumok, amelyek bármely szövegszerkesztőben megnyithatók szerkesztés céljából. Ha azonban egy támogatott IDE-ben nyitja meg megfelelő szintaktikai kiemeléssel, a kód könnyen olvasható és elrendezhető. Egy egyszerű CS fájl a következőket tartalmazza:

* Névterek deklarációja – Az adott névtér által meghatározott adott funkcióra való hivatkozáshoz
* Változók deklarálása – Osztályszintű változók deklarálása az adott megvalósításhoz
* Methods Declaration – Metódusok deklarációja az adott funkcióhoz

### Szintaxis ###

* Pontosvesszővel jelöljük az utasítás végét.
* A göndör zárójelek az utasítások csoportosítására szolgálnak. Az utasításokat általában metódusokba (függvényekbe), a metódusokat osztályokba és az osztályokat névterekbe csoportosítják.
* A változók hozzárendelése egyenlőségjellel történik, de összehasonlításuk két egymást követő egyenlőségjellel történik.
* Szögletes zárójelet használunk a tömbökhöz, mind deklarálásukra, mind pedig arra, hogy az egyikben egy adott indexen értéket kapjunk.

### Példa ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

