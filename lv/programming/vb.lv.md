{
  "date": "2019-10-11",
  "keywords": [
"vb",
"failu",
"pagarinājumu",
"faila formātā",
"Visual Basic",
"Programmēšanas rokasgrāmata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VB — Visual Basic Code fails",
  "description": "Uzziniet par VB failu formātu un API, kas var izveidot un atvērt VB failus.",
  "linktitle": "VB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-v-lvb"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir VB fails?

VB fails ir avota koda fails, kas izveidots Visual Basic valodā, ko Microsoft izveidoja .NET lietojumprogrammu izstrādei. Vēl viena līdzīga valoda ar atšķirīgu sintaksi ir C#, kuras faili tiek saglabāti ar faila paplašinājumu [.CS](/programming/cs/). Faila formāts nodrošina zema līmeņa programmēšanas valodu koda rakstīšanai, kas tiek kompilēts, lai ģenerētu galīgo izvades failu EXE vai DLL formātā. Tos var izveidot un apkopot, izmantojot Microsoft Visual Studio. Microsoft Visual Studio Express var izmantot arī, lai izveidotu un atjauninātu šādus failus, kas ir bezmaksas IDE. Vienkāršā Visual Studio projektā [solution](/programming/sln/), kas izveidots ar VB valodu, var būt viens vai vairāki šādi faili. Faili, kas atzīmēti iekļaušanai kompilācijā, ir uzskaitīti failā [CSPROJ](/programming/csproj/), kas ir daļa no projekta un liek kompilatoram izmantot atzīmētos failus.

## VB faila formāts — vairāk informācijas

VB faili ir teksta failu formāti, kurus var atvērt jebkurā teksta redaktorā rediģēšanai. Tomēr, atverot atbalstītā IDE ar pareizu sintakses izcelšanu, kodu ir viegli lasīt un sakārtot. Vienkāršā VB failā ir:

* Nosaukumvietu deklarācija — lai atsauktos uz noteiktu funkcionalitāti, ko definē šī konkrētā nosaukumvieta

* Mainīgo deklarācija - lai deklarētu klases līmeņa mainīgos konkrētajai īstenošanai

* Metožu deklarācija - lai deklarētu metožu deklarāciju konkrētai funkcionalitātei


## VB faila formāta piemērs

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



