{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "soubor", "přípona", "formát souboru", "CSharp", "Programovací jazyk" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - CSharp Code File",
  "description":"Další informace o formátu souboru CS a rozhraních API, která mohou vytvářet a otevírat soubory CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor CS?

Soubory s příponou .cs jsou soubory zdrojového kódu pro programovací jazyk C#. Souborový formát představený společností Microsoft pro použití s rozhraním .NET Framework poskytuje nízkoúrovňový programovací jazyk pro psaní kódu, který je zkompilován tak, aby generoval konečný výstupní soubor ve formě EXE nebo DLL. Ty lze vytvořit a zkompilovat pomocí Microsoft Visual Studio. K vytváření a aktualizaci takových souborů lze také použít Microsoft Visual Studio Express, což je bezplatné IDE. Soubory CS se používají pro vývoj aplikací, které se mohou pohybovat od jednoduchých desktopových aplikací až po složitější programy. Jednoduchý projekt Visual Studia [řešení](/cs/programming/sln/) vytvořený v jazyce C# může obsahovat jeden nebo více takových souborů. Soubory označené pro zahrnutí do kompilace jsou uvedeny v souboru [CSPROJ](/cs/programming/csproj/), který je součástí projektu a říká kompilátoru, aby použil označené soubory.

## Formát souboru CS ##

Soubory CS jsou textové formáty souborů, které lze pro úpravy otevřít v libovolném textovém editoru. Při otevření v podporovaném IDE se správným zvýrazněním syntaxe je však kód snadno čitelný a uspořádaný. Jednoduchý soubor CS obsahuje:

* Deklarace jmenných prostorů – pro odkazování na konkrétní funkcionalitu definovanou tímto konkrétním jmenným prostorem
* Deklarace proměnných - Pro deklaraci proměnných na úrovni třídy pro konkrétní implementaci
* Deklarace metod - Pro deklaraci metod pro konkrétní funkcionalitu

### Syntaxe ###

* K označení konce příkazu se používají středníky.
* Složené závorky se používají k seskupování příkazů. Příkazy jsou běžně seskupeny do metod (funkcí), metod do tříd a tříd do jmenných prostorů.
* Proměnné se přiřazují pomocí znaménka rovná se, ale porovnávají se pomocí dvou po sobě jdoucích znamének rovná se.
* Hranaté závorky se používají s poli, jak k jejich deklaraci, tak k získání hodnoty daného indexu v jednom z nich.

### Příklad ###

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

