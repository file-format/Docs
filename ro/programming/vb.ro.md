{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "fișier", "extensie", "format fișier", "Visual Basic", "Ghid de programare"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Fișier cod Visual Basic",
  "description":"Aflați despre formatul de fișier VB și despre API-urile care pot crea și deschide fișiere VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier VB?

Un fișier VB este un fișier de cod sursă creat în limbajul Visual Basic care a fost creat de Microsoft pentru dezvoltarea aplicațiilor .NET. Un alt limbaj similar cu sintaxă diferită este C# ale cărui fișiere sunt salvate cu extensia de fișier [.CS](/ro/programming/cs/). Formatul de fișier oferă limbajul de programare de nivel scăzut pentru scrierea codului care este compilat pentru a genera fișierul final de ieșire sub formă de EXE sau DLL. Acestea pot fi create și compilate cu Microsoft Visual Studio. Microsoft Visual Studio Express poate fi folosit și pentru a crea și actualiza astfel de fișiere, care este un IDE gratuit. Un proiect simplu Visual Studio [soluție](/ro/programming/sln/) creat cu limbajul VB poate cuprinde unul sau mai multe astfel de fișiere. Fișierele marcate pentru includerea în compilare sunt listate în fișierul [CSPROJ](/ro/programming/csproj/), care face parte din proiect și îi spune compilatorului să folosească fișierele marcate.

## Format de fișier VB - Mai multe informații

Fișierele VB sunt formate de fișiere bazate pe text care pot fi deschise în orice editor de text pentru editare. Cu toate acestea, atunci când este deschis într-un IDE acceptat cu evidențierea corectă a sintaxelor, codul este ușor de citit și aranjat. Un fișier VB simplu conține:

* Declarație de spații de nume - Pentru referire la o anumită funcționalitate definită de acel spațiu de nume specific
* Declarație de variabile - Pentru a declara variabile la nivel de clasă pentru implementarea particulară
* Declarație de metode - Pentru a declara declarația de metode pentru o anumită funcționalitate

## Exemplu de format de fișier VB

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



