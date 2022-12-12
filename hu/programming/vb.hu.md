{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "file", "extension", "file format", "Visual Basic", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic Code File",
  "description":"További információ a VB fájlformátumról és az API-król, amelyek VB-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a VB fájl?

A VB-fájl egy Visual Basic nyelven létrehozott forráskódfájl, amelyet a Microsoft .NET-alkalmazások fejlesztésére hozott létre. Egy másik hasonló, eltérő szintaxisú nyelv a C#, amelynek fájljai [.CS](/hu/programming/cs/) fájlkiterjesztéssel kerülnek mentésre. A fájlformátum biztosítja az alacsony szintű programozási nyelvet a kód írásához, amelyet a végső kimeneti fájl EXE vagy DLL formátumban történő előállításához fordítanak le. Ezeket a Microsoft Visual Studio programmal lehet létrehozni és lefordítani. A Microsoft Visual Studio Express is használható ilyen fájlok létrehozására és frissítésére, amely egy ingyenes IDE. A VB nyelvvel létrehozott egyszerű Visual Studio projekt [megoldás] (/hu/programing/sln/) egy vagy több ilyen fájlból állhat. A fordításba való felvételre megjelölt fájlok a [CSPROJ](/hu/programming/csproj/) fájlban vannak felsorolva, amely a projekt részét képezi, és utasítja a fordítót a megjelölt fájlok használatára.

## VB fájlformátum - További információ

A VB fájlok szöveg alapú fájlformátumok, amelyek bármely szövegszerkesztőben megnyithatók szerkesztés céljából. Ha azonban egy támogatott IDE-ben nyitja meg megfelelő szintaktikai kiemeléssel, a kód könnyen olvasható és elrendezhető. Egy egyszerű VB fájl a következőket tartalmazza:

* Névterek deklarációja – Az adott névtér által meghatározott adott funkcióra való hivatkozáshoz
* Változók deklarálása – Osztályszintű változók deklarálása az adott megvalósításhoz
* Methods Declaration – Metódusok deklarációja az adott funkcióhoz

## VB fájlformátum példa

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



