{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "soubor", "přípona", "formát souboru", "Visual Basic", "Průvodce programováním" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - soubor kódu Visual Basic",
  "description":"Další informace o formátu souboru VB a rozhraních API, která mohou vytvářet a otevírat soubory VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor VB?

Soubor VB je soubor zdrojového kódu vytvořený v jazyce Visual Basic, který byl vytvořen společností Microsoft pro vývoj aplikací .NET. Dalším podobným jazykem s odlišnou syntaxí je C#, jehož soubory jsou uloženy s příponou [.CS](/cs/programming/cs/). Formát souboru poskytuje nízkoúrovňový programovací jazyk pro psaní kódu, který je zkompilován tak, aby vygeneroval konečný výstupní soubor ve formě EXE nebo DLL. Ty lze vytvořit a zkompilovat pomocí Microsoft Visual Studio. K vytváření a aktualizaci takových souborů lze také použít Microsoft Visual Studio Express, což je bezplatné IDE. Jednoduchý projekt Visual Studia [řešení](/cs/programming/sln/) vytvořený v jazyce VB může obsahovat jeden nebo více takových souborů. Soubory označené pro zahrnutí do kompilace jsou uvedeny v souboru [CSPROJ](/cs/programming/csproj/), který je součástí projektu a říká kompilátoru, aby použil označené soubory.

## Formát souboru VB – Další informace

Soubory VB jsou textové formáty souborů, které lze pro úpravy otevřít v libovolném textovém editoru. Při otevření v podporovaném IDE se správným zvýrazněním syntaxe je však kód snadno čitelný a uspořádaný. Jednoduchý soubor VB obsahuje:

* Deklarace jmenných prostorů – pro odkazování na konkrétní funkcionalitu definovanou tímto konkrétním jmenným prostorem
* Deklarace proměnných - Pro deklaraci proměnných na úrovni třídy pro konkrétní implementaci
* Deklarace metod - Pro deklaraci metod pro konkrétní funkcionalitu

## Příklad formátu souboru VB

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



