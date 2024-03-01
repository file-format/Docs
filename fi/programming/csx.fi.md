{
  "date": "2023-05-15",
  "keywords": [
"csx tiedosto",
"mikä on csx-tiedosto",
"mitä csx-tiedosto sisältää",
"mikä on csx-tiedoston muoto",
"tiedosto",
"csx tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CSX-tiedostomuoto - Visuaalinen C#-skripti",
  "description": "Opi CSX-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata CSX-tiedostoja.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx-fi",
      "parent": "programming"
}
},
  "lastmod": "2023-05-15"
}

## Mikä on CSX-tiedosto?

Visual C# Script (tunnetaan myös nimellä CSX) on Roslynin komentosarjamoottorin käyttämä tiedostomuoto Microsoftin .NET-ekosysteemissä. CSX-tiedostot sisältävät C#-koodin, joka voidaan suorittaa suoraan ilman erillistä käännösvaihetta.

CSX-muoto on erityinen Microsoftin ekosysteemille, eikä se ole yleisesti käytetty tiedostomuoto yleisessä ohjelmoinnissa. CSX-tiedostoja käytetään usein tilanteissa, joissa tarvitaan nopeaa prototyyppi- tai komentosarjatoimintoa. Niiden avulla voit luoda ja suorittaa C#-ohjelmia kevyemmällä tavalla kuin täysimittaisen käännetyn sovelluksen luominen.

CSX-tiedostojen suorittamiseen voit käyttää työkaluja, kuten .NET Interactive Notebooks, jotka tarjoavat interaktiivisen ympäristön C#-koodin suorittamiseen. Visual Studio Codea C#-laajennuksella ja .NET Core SDK:lla voidaan käyttää myös CSX-tiedostojen kanssa työskentelemiseen.

## Mitä CSX-tiedosto sisältää?

CSX (C# Script) -tiedosto sisältää C#-koodin, joka voidaan suorittaa suoraan. Se voi sisältää mitä tahansa kelvollista C#-koodia, kuten muuttujamäärityksiä, toimintoja, luokkia ja muita ohjelmointirakenteita.

Tässä on esimerkki siitä, mitä CSX-tiedosto saattaa sisältää:

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

CSX-tiedostot voivat sisältää myös tuontilausekkeita, ulkoisia kirjastoviittauksia ja muita C#-kielen ominaisuuksia tukemaan koodin toimintoja. Koodi tulkitaan ja suoritetaan lennossa ilman käännöstä, joten se sopii komentosarjoihin ja nopeisiin prototyyppitehtäviin.

## Mikä on CSX-tiedoston muoto?

CSX (C# Script) -muoto noudattaa yksinkertaista tekstipohjaista muotoa. Sen tiedostotunniste on yleensä .csx, joka erottaa sen tavallisista C#-lähdekooditiedostoista (.cs).

CSX-tiedostoja voidaan muokata millä tahansa tekstieditorilla tai integroidulla kehitysympäristöllä (IDE), joka tukee C#-syntaksin korostusta. Kun CSX-tiedosto on valmis, se voidaan suorittaa käyttämällä työkaluja, kuten .NET Interactive Notebooks, .NET Core -komentoriviliittymä (CLI) tai IDE, jossa on C#-komentosarjatukea.

## Viitteet
* [C# programming with Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

