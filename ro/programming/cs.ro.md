{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "fișier", "extensie", "format fișier", "CSharp", "Limbaj de programare"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - Fișier cod CSharp",
  "description":"Aflați despre formatul de fișier CS și despre API-urile care pot crea și deschide fișiere CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier CS?

Fișierele cu extensia .cs sunt fișiere de cod sursă pentru limbajul de programare C#. Introdus de Microsoft pentru a fi utilizat cu .NET Framework, formatul de fișier oferă limbajul de programare de nivel scăzut pentru scrierea codului care este compilat pentru a genera fișierul final de ieșire sub formă de EXE sau DLL. Acestea pot fi create și compilate cu Microsoft Visual Studio. Microsoft Visual Studio Express poate fi folosit și pentru a crea și actualiza astfel de fișiere, care este un IDE gratuit. Fișierele CS sunt folosite pentru dezvoltarea de aplicații care pot varia de la simple aplicații desktop la programe mai complexe. Un proiect simplu Visual Studio [soluție](/ro/programming/sln/) creat cu limbajul C# poate cuprinde unul sau mai multe astfel de fișiere. Fișierele marcate pentru includerea în compilare sunt listate în fișierul [CSPROJ](/ro/programming/csproj/), care face parte din proiect și îi spune compilatorului să folosească fișierele marcate.

## Format fișier CS ##

Fișierele CS sunt formate de fișiere bazate pe text care pot fi deschise în orice editor de text pentru editare. Cu toate acestea, atunci când este deschis într-un IDE acceptat cu evidențierea corectă a sintaxelor, codul este ușor de citit și aranjat. Un fișier CS simplu conține:

* Declarație de spații de nume - Pentru referire la o anumită funcționalitate definită de acel spațiu de nume specific
* Declarație de variabile - Pentru a declara variabile la nivel de clasă pentru implementarea particulară
* Declarație de metode - Pentru a declara declarația de metode pentru o anumită funcționalitate

### Sintaxă ###

* Punctele și virgulă sunt folosite pentru a indica sfârșitul unei declarații.
* Parantezele sunt folosite pentru a grupa declarațiile. Instrucțiunile sunt grupate în mod obișnuit în metode (funcții), metodele în clase și clasele în spații de nume.
* Variabilele sunt atribuite folosind un semn egal, dar comparate folosind două semne egal consecutive.
* Parantezele pătrate sunt folosite cu tablouri, atât pentru a le declara, cât și pentru a obține o valoare la un index dat într-unul dintre ele.

### Exemplu ###

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

