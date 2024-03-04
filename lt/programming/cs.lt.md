{
  "date": "2019-10-11",
  "keywords": [
"cs",
"failą",
"pratęsimas",
"Dokumento formatas",
"CSharp",
"Programavimo kalba"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CS – CSharp kodo failas",
  "description": "Sužinokite apie CS failo formatą ir API, kurios gali kurti ir atidaryti CS failus.",
  "linktitle": "CS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c-lts"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra CS failas?

Failai su plėtiniu .cs yra C# programavimo kalbos šaltinio kodo failai. Microsoft sukurtas naudoti su .NET Framework, failo formatas suteikia žemo lygio programavimo kalbą, skirtą rašyti kodą, kuris sukompiliuojamas, kad būtų sukurtas galutinis išvesties failas EXE arba DLL pavidalu. Juos galima sukurti ir sukompiliuoti naudojant Microsoft Visual Studio. Microsoft Visual Studio Express taip pat gali būti naudojamas kurti ir atnaujinti tokius failus, kurie yra nemokama IDE. CS failai naudojami kuriant programas, kurios gali būti nuo paprastų darbalaukio programų iki sudėtingesnių programų. Paprastas Visual Studio projektas [solution](/programming/sln/), sukurtas naudojant C# kalbą, gali apimti vieną ar daugiau tokių failų. Failai, pažymėti įtraukti į kompiliaciją, yra išvardyti faile [CSPROJ](/programming/csproj/), kuris yra projekto dalis ir nurodo kompiliatoriui naudoti pažymėtus failus.

## CS failo formatas ##

CS failai yra tekstiniai failų formatai, kuriuos galima atidaryti bet kuriame teksto rengyklėje redaguoti. Tačiau atidarius palaikomoje IDE su tinkamu sintaksės paryškinimu, kodą lengva perskaityti ir tvarkyti. Paprastame CS faile yra:

* Vardų erdvių deklaracija – skirta nuorodai į tam tikrą funkciją, apibrėžtą toje konkrečioje vardų erdvėje

* Kintamųjų deklaracija – deklaruoti klasės lygio kintamuosius konkrečiam įgyvendinimui

* Metodų deklaracija – deklaruoti tam tikros funkcijos metodų deklaraciją


### Sintaksė ###

* Teiginio pabaigai pažymėti naudojami kabliataškiai.

* Garbanotieji skliaustai naudojami teiginiams grupuoti. Teiginiai paprastai grupuojami į metodus (funkcijas), metodai į klases ir klasės į vardų erdves.

* Kintamieji priskiriami naudojant lygybės ženklą, bet lyginami naudojant du iš eilės lygybės ženklus.

* Kvadratiniai skliaustai naudojami su masyvais, norint juos deklaruoti ir gauti tam tikro indekso vertę viename iš jų.


### Pavyzdys ###

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

## Kiti CS failai

Štai kiti failų tipai, kuriuose naudojamas **.cs** failo plėtinys.

**Duomenų failai ir žaidimas**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Programavimas**
- [CS – CSharp kodo failas](/programming/cs/)

