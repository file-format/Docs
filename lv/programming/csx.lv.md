{
  "date": "2023-05-15",
  "keywords": [
"csx failu",
"kas ir csx fails",
"ko satur csx fails",
"kāds ir csx faila formāts",
"failu",
"csx faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CSX faila formāts — vizuālais C# skripts",
  "description": "Uzziniet par CSX formātu un API, kas var izveidot un atvērt CSX failus.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx-lv",
      "parent": "programming"
}
},
  "lastmod": "2023-05-15"
}

## Kas ir CSX fails?

Visual C# Script (pazīstams arī kā CSX) ir faila formāts, ko Microsoft .NET ekosistēmā izmanto Roslyn skriptu programma. CSX faili satur C# kodu, ko var izpildīt tieši, bez nepieciešamības veikt atsevišķu kompilācijas darbību.

CSX formāts ir raksturīgs Microsoft ekosistēmai un nav plaši izmantots faila formāts vispārējā programmēšanā. CSX faili bieži tiek izmantoti gadījumos, kad nepieciešama ātra prototipēšana vai skriptēšanas funkcionalitāte. Tie ļauj jums izveidot un palaist C# programmas vieglākā veidā, salīdzinot ar pilnvērtīgas kompilētas lietojumprogrammas izveidi.

Lai izpildītu CSX failus, varat izmantot tādus rīkus kā .NET Interactive Notebooks, kas nodrošina interaktīvu vidi C# koda palaišanai. Visual Studio kodu ar paplašinājumu C# un .NET Core SDK var izmantot arī darbam ar CSX failiem.

## Ko satur CSX fails?

CSX (C# Script) fails satur C# kodu, ko var izpildīt tieši. Tas var ietvert jebkuru derīgu C# kodu, piemēram, mainīgo deklarācijas, funkcijas, klases un citas programmēšanas konstrukcijas.

Šeit ir piemērs tam, ko var saturēt CSX fails:

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

CSX faili var ietvert arī importēšanas paziņojumus, ārējās bibliotēkas atsauces un citus C# valodas līdzekļus, lai atbalstītu koda funkcionalitāti. Kods tiek interpretēts un izpildīts lidojuma laikā, bez nepieciešamības to apkopot, padarot to piemērotu skriptu veidošanas un ātras prototipēšanas uzdevumiem.

## Kāds ir CSX faila formāts?

CSX (C# Script) formāts seko vienkāršam teksta formātam. Tam parasti ir faila paplašinājums .csx, lai to atšķirtu no parastajiem C# pirmkoda failiem (.cs).

CSX failus var rediģēt, izmantojot jebkuru teksta redaktoru vai integrēto izstrādes vidi (IDE), kas atbalsta C# sintakses izcelšanu. Kad CSX fails ir gatavs, to var izpildīt, izmantojot tādus rīkus kā .NET Interactive Notebooks, .NET Core komandrindas interfeiss (CLI) vai IDE ar C# skriptu atbalstu.

## Atsauces
* [C# programming with Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

