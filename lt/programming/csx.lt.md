{
  "date": "2023-05-15",
  "keywords": [
"csx failą",
"kas yra csx failas",
"kas yra csx faile",
"koks yra csx failo formatas",
"failą",
"csx failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CSX failo formatas – Visual C# Script",
  "description": "Sužinokite apie CSX formatą ir API, kurios gali kurti ir atidaryti CSX failus.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx-lt",
      "parent": "programming"
}
},
  "lastmod": "2023-05-15"
}

## Kas yra CSX failas?

Visual C# Script (taip pat žinomas kaip CSX) yra failo formatas, kurį Microsoft .NET ekosistemoje naudoja Roslyn scenarijų variklis. CSX failuose yra C# kodas, kurį galima vykdyti tiesiogiai, nereikia atskiro kompiliavimo veiksmo.

CSX formatas yra būdingas Microsoft ekosistemai, o ne bendrame programavime plačiai naudojamas failų formatas. CSX failai dažnai naudojami tais atvejais, kai reikia greito prototipų ar scenarijų kūrimo. Jie leidžia kurti ir paleisti C# programas lengvesniu būdu, palyginti su visavertės kompiliuotos programos kūrimu.

Norėdami vykdyti CSX failus, galite naudoti tokius įrankius kaip .NET Interactive Notebooks, kurie suteikia interaktyvią aplinką C# kodui paleisti. Visual Studio kodas su C# plėtiniu ir .NET Core SDK taip pat gali būti naudojamas darbui su CSX failais.

## Kas yra CSX faile?

CSX (C# Script) faile yra C# kodas, kurį galima vykdyti tiesiogiai. Tai gali apimti bet kokį galiojantį C# kodą, pvz., kintamųjų deklaracijas, funkcijas, klases ir kitas programavimo konstrukcijas.

Štai pavyzdys, kas gali būti CSX faile:

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

CSX failuose taip pat gali būti importavimo teiginių, išorinių bibliotekos nuorodų ir kitų C# kalbos funkcijų, palaikančių kodo funkcijas. Kodas interpretuojamas ir vykdomas skrydžio metu, jo nereikia kompiliuoti, todėl jis tinka scenarijų ir greitoms prototipų kūrimo užduotims.

## Koks yra CSX failo formatas?

CSX (C# Script) formatas atitinka paprastą teksto formatą. Paprastai jis turi failo plėtinį .csx, kad atskirtų jį nuo įprastų C# šaltinio kodo failų (.cs).

CSX failus galima redaguoti naudojant bet kurį teksto rengyklę arba integruotą kūrimo aplinką (IDE), kuri palaiko C# sintaksės paryškinimą. Kai CSX failas bus paruoštas, jį galima vykdyti naudojant tokius įrankius kaip .NET Interactive Notebooks, .NET Core komandų eilutės sąsaja (CLI) arba IDE su C# scenarijų palaikymu.

## Nuorodos
* [C# programming with Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

