{
  "date": "2021-09-23",
  "keywords": [
"RIEKSTS",
"failu",
"pagarinājumu",
"faila formātā",
"riekstu programmēšanas valoda",
"Programmēšanas rokasgrāmata",
"RIEKSTU piemērs",
"NUT faila formāts",
"vāveres valoda",
".nut paplašinājuma fails",
"NUT faili"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "RIKSTS — vāveres valodas fails",
  "description": "Uzziniet par NUT faila formātu un API, kas var izveidot un atvērt NUT failus.",
  "linktitle": "NUT",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nu-lvt"
}
},
  "lastmod": "2021-09-23"
}

## Kas ir NUT fails?

NUT faila formāts pieder programmēšanas valodai, kas ir pazīstama kā Squirrel. Tā ir uz objektu orientēta, augsta līmeņa un obligāta programmēšanas valoda, ko galvenokārt izmanto iegultās sistēmās un videospēlēs.

Vāveres valoda tiek uzskatīta par vieglu skriptu valodu, kuru var viegli pielāgot atbilstoši izmēram un joslas platumam. Tas ietver automātiskās atsauces skaitīšanas priekšrocības un atmiņā esošo atkritumu pārvaldību.

Vāveres valodas sintakse piesaista izstrādātājus, jo tā ir līdzīga C un ietver skriptu valodas iezīmi. Bet tomēr tai ir mazāk priekšrocību, salīdzinot ar citām šim nolūkam populārākajām programmēšanas valodām.



## Īsa vēsture ##

It was designed by Alberto Demichelis in 2003. Tomēr 2016. gadā tika izlaista šīs valodas stabila versija. Tā tika izstrādāta saskaņā ar zlib/libpng licenci. 2010. gadā licence tika mainīta un nodota MIT. Šī valoda tiek uzskatīta par iedvesmotu [LUA](/programming/lua/) (programmēšanas valoda) versiju. Alberto izstrādātajā tīmekļa vietnē ir saraksts ar ieteikumiem par iepriekšējo valodu, lai padarītu to izdevīgāku.


## Tehniskā specifikācija ##

Vāveres valodas iezīme un specifikācijas ir vairākas. Tas nodrošina dinamiskās rakstīšanas iespēju, deleģēšanas īpašumu, vairākus klašu un saskarņu lietojumus. Šīs valodas sintakse ir līdzīga C valodas sintaksei. Lietojumprogrammas, piemēram, Enduro/X (klastera lietojumprogrammu serveris), izmanto šo valodu. Tā kā Squirrel tiek izmantota arī videospēlēm, dažas no tām ir OpenTTD, GTA IV utt.

The stable release of the language is 3.0.7. Rīku komplekts, kas pazīstams kā MirthKit, izmanto Squirrel programmēšanas valodu, lai nodrošinātu atvērtā koda un starpplatformu divdimensiju spēlēm. Šīs valodas būtība ir dinamiska, un lielākā daļa funkciju ir līdzīgas [Python](/programming/py/), LUA utt. Tā ietver arī uz reģistriem balstītas virtuālās mašīnas ieviešanu. Vāveres darbība ir lēnāka, salīdzinot ar LLU.

Ir arī vēl viens paplašinājuma faila tips .nut, tāpēc jums vajadzētu apskatīt faila lielumu, lai uzzinātu, kurš NUT fails jums ir. Vāveres skripta NUT faili lielākoties ir mazāki par 1 MB, savukārt video NUT faili parasti ir lielāki par 1 MB.


## NUT faila formāta piemērs ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Atsauce Nr.

* [NUT — Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))




