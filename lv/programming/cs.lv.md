{
  "date": "2019-10-11",
  "keywords": [
"cs",
"failu",
"pagarinājumu",
"faila formātā",
"CSharp",
"Programmēšanas valoda"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CS — CSarp koda fails",
  "description": "Uzziniet par CS failu formātu un API, kas var izveidot un atvērt CS failus.",
  "linktitle": "CS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c-lvs"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir CS fails?

Faili ar paplašinājumu .cs ir avota koda faili C# programmēšanas valodai. Faila formāts, ko Microsoft ieviesa lietošanai ar .NET Framework, nodrošina zema līmeņa programmēšanas valodu koda rakstīšanai, kas tiek kompilēts, lai ģenerētu galīgo izvades failu EXE vai DLL formātā. Tos var izveidot un apkopot, izmantojot Microsoft Visual Studio. Microsoft Visual Studio Express var izmantot arī, lai izveidotu un atjauninātu šādus failus, kas ir bezmaksas IDE. CS faili tiek izmantoti lietojumprogrammu izstrādei, sākot no vienkāršām darbvirsmas lietojumprogrammām līdz sarežģītākām programmām. Vienkāršā Visual Studio projektā [solution](/programming/sln/), kas izveidots ar C# valodu, var būt viens vai vairāki šādi faili. Faili, kas atzīmēti iekļaušanai kompilācijā, ir uzskaitīti failā [CSPROJ](/programming/csproj/), kas ir daļa no projekta un liek kompilatoram izmantot atzīmētos failus.

## CS faila formāts ##

CS faili ir teksta failu formāti, kurus var atvērt jebkurā teksta redaktorā rediģēšanai. Tomēr, atverot atbalstītā IDE ar pareizu sintakses izcelšanu, kodu ir viegli lasīt un sakārtot. Vienkāršā CS failā ir:

* Nosaukumvietu deklarācija — lai atsauktos uz noteiktu funkcionalitāti, ko definē šī konkrētā nosaukumvieta

* Mainīgo deklarācija - lai deklarētu klases līmeņa mainīgos konkrētajai īstenošanai

* Metožu deklarācija - lai deklarētu metožu deklarāciju konkrētai funkcionalitātei


### Sintakse ###

* Semikolus izmanto, lai apzīmētu paziņojuma beigas.

* Izteikumu grupēšanai tiek izmantotas cirtainas iekavas. Paziņojumi parasti tiek grupēti metodēs (funkcijās), metodes klasēs un klases nosaukumu telpās.

* Mainīgie tiek piešķirti, izmantojot vienādības zīmi, bet salīdzināti, izmantojot divas secīgas vienādības zīmes.

* Kvadrātiekavas tiek izmantotas ar masīviem, gan lai tos deklarētu, gan lai vienā no tiem iegūtu vērtību noteiktā indeksā.


### Piemērs ###

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

## Citi CS faili

Tālāk ir norādīti citi failu veidi, kuros tiek izmantots faila paplašinājums **.cs**.

**Datu faili un spēle**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Programmēšana**
- [CS — CSarp koda fails](/programming/cs/)

