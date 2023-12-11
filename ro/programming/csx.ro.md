{
"data": "2023-05-15",
  "keywords": [
"fișier csx",
"Ce este un fișier csx",
"ce conține fișierul csx",
"care este formatul fișierului csx",
"fişier",
"extensie fișier csx",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format fișier CSX - Script Visual C#",
  "description":"Aflați despre formatul CSX și despre API-urile care pot crea și deschide fișiere CSX.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## Ce este un fișier CSX?

Visual C# Script (cunoscut și ca CSX) este un format de fișier folosit de motorul de scripting Roslyn în ecosistemul .NET al Microsoft. Fișierele CSX conțin cod C# care poate fi executat direct, fără a fi nevoie de un pas de compilare separat.

Formatul CSX este specific ecosistemului Microsoft și nu este un format de fișier utilizat pe scară largă în programarea generală. Fișierele CSX sunt adesea folosite în scenarii în care este necesară o funcționalitate rapidă de prototipare sau de scriptare. Acestea vă permit să creați și să rulați programe C# într-un mod mai ușor în comparație cu crearea unei aplicații compilate cu drepturi depline.

Pentru a executa fișiere CSX, puteți utiliza instrumente precum .NET Interactive Notebooks, care oferă un mediu interactiv pentru rularea codului C#. Visual Studio Code cu extensia C# și .NET Core SDK poate fi folosit și pentru a lucra cu fișiere CSX.

## Ce conține fișierul CSX?

Un fișier CSX (C# Script) conține cod C# care poate fi executat direct. Poate include orice cod C# valid, cum ar fi declarații de variabile, funcții, clase și alte constructe de programare.

Iată un exemplu despre ce ar putea conține fișierul CSX:

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

Fișierele CSX pot include, de asemenea, instrucțiuni de import, referințe externe de bibliotecă și alte caracteristici ale limbajului C# pentru a sprijini funcționalitatea codului. Codul este interpretat și executat din mers, fără a fi nevoie de compilare, ceea ce îl face potrivit pentru sarcini de scriptare și prototipare rapidă.

## Care este formatul fișierului CSX?

Formatul CSX (C# Script) urmează un format simplu bazat pe text. De obicei, are extensia de fișier .csx pentru a-l diferenția de fișierele obișnuite de cod sursă C# (.cs).

Fișierele CSX pot fi editate folosind orice editor de text sau mediu de dezvoltare integrat (IDE) care acceptă evidențierea sintaxei C#. Odată ce fișierul CSX este gata, acesta poate fi executat folosind instrumente precum .NET Interactive Notebooks, interfața de linie de comandă (CLI) .NET Core sau un IDE cu suport pentru scripting C#.

## Referințe
* [Programare C# cu Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

