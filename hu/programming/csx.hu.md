{
"dátum": "2023-05-15",
  "keywords": [
"csx fájl",
"mi az a csx fájl",
"mit tartalmaz a csx fájl",
"mi a csx fájl formátuma",
"fájl",
"csx fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CSX fájlformátum - Visual C# Script",
  "description":"További információ a CSX formátumról és az API-król, amelyek CSX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## Mi az a CSX fájl?

A Visual C# Script (más néven CSX) a Roslyn szkriptmotor által használt fájlformátum a Microsoft .NET ökoszisztémájában. A CSX fájlok C# kódot tartalmaznak, amely külön fordítási lépés nélkül közvetlenül végrehajtható.

A CSX formátum a Microsoft ökoszisztémájára jellemző, és nem széles körben használt fájlformátum az általános programozásban. A CSX-fájlokat gyakran használják olyan esetekben, amikor gyors prototípus-készítésre vagy parancsfájlokra van szükség. Lehetővé teszik a C# programok egyszerűbb létrehozását és futtatását, mint egy teljes értékű lefordított alkalmazás létrehozása.

A CSX fájlok végrehajtásához olyan eszközöket használhat, mint a .NET Interactive Notebooks, amelyek interaktív környezetet biztosítanak a C# kód futtatásához. A C# kiterjesztésű Visual Studio Code és a .NET Core SDK is használható CSX fájlokkal való munkavégzésre.

## Mit tartalmaz a CSX fájl?

A CSX (C# Script) fájl C# kódot tartalmaz, amely közvetlenül végrehajtható. Tartalmazhat bármilyen érvényes C# kódot, például változódeklarációkat, függvényeket, osztályokat és egyéb programozási konstrukciókat.

Íme egy példa arra, hogy mit tartalmazhat a CSX fájl:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

A CSX-fájlok importálási utasításokat, külső könyvtári hivatkozásokat és egyéb C#-nyelvi szolgáltatásokat is tartalmazhatnak a kód funkcióinak támogatására. A kód értelmezése és végrehajtása menet közben történik, fordítás nélkül, így alkalmas szkriptelési és gyors prototípuskészítési feladatokra.

## Mi a CSX fájl formátuma?

A CSX (C# Script) formátum egyszerű szövegalapú formátumot követ. Általában .csx fájlkiterjesztéssel rendelkezik, amely megkülönbözteti a hagyományos C# forráskódfájloktól (.cs).

A CSX fájlok bármilyen szövegszerkesztővel vagy integrált fejlesztői környezettel (IDE) szerkeszthetők, amely támogatja a C# szintaxis kiemelését. Amint a CSX-fájl készen áll, végrehajtható olyan eszközökkel, mint a .NET Interactive Notebooks, a .NET Core parancssori felület (CLI) vagy egy C# szkriptet támogató IDE.

## Hivatkozások
* [C# programozás Visual Studio Code segítségével](https://code.visualstudio.com/docs/languages/csharp)

