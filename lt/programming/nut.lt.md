{
  "date": "2021-09-23",
  "keywords": [
"RIEŠUTAS",
"failą",
"pratęsimas",
"Dokumento formatas",
"RIEŠTŲ programavimo kalba",
"Programavimo vadovas",
"RIEŠUTŲ pavyzdys",
"NUT failo formatas",
"voverės kalba",
".nut plėtinio failas",
"NUT failai"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "RIEŠUTAS – voverės kalbos failas",
  "description": "Sužinokite apie NUT failo formatą ir API, kurios gali kurti ir atidaryti NUT failus.",
  "linktitle": "NUT",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nu-ltt"
}
},
  "lastmod": "2021-09-23"
}

## Kas yra NUT failas?

NUT failo formatas priklauso programavimo kalbai, kuri yra žinoma kaip Voverė. Tai į objektą orientuota, aukšto lygio ir privaloma programavimo kalba, kuri dažniausiai naudojama įterptosiose sistemose ir vaizdo žaidimuose.

Voverės kalba laikoma lengva scenarijų kalba, kurią galima lengvai koreguoti pagal dydį ir pralaidumą. Tai apima automatinio nuorodų skaičiavimo ir atmintyje esančių šiukšlių valdymo pranašumus.

Voverės kalbos sintaksė pritraukia kūrėjus, nes ji yra panaši į C ir apima scenarijų kalbos funkciją. Tačiau jis turi daug mažiau pranašumų, palyginti su kitomis šiam tikslui skirtomis populiaresnėmis programavimo kalbomis.



## Trumpa istorija ##

It was designed by Alberto Demichelis in 2003. Tačiau 2016 m. buvo išleista stabili šios kalbos versija. Ji buvo sukurta pagal zlib/libpng licenciją. 2010 m. licencija buvo pakeista ir perduota MIT. Ši kalba laikoma įkvėpta [LUA](/programming/lua/) (programavimo kalba) versija. Alberto sukurtoje svetainėje yra pasiūlymų dėl ankstesnės kalbos sąrašas, kad ji būtų naudingesnė.


## Techninė specifikacija Nr.

Voverės kalbos ypatybės ir specifikacijos yra įvairios. Tai suteikia galimybę dinaminiam spausdinimui, delegavimo savybėms, keletui klasių ir sąsajų naudojimo būdų. Šios kalbos sintaksė yra panaši į C kalbos sintaksę. Tokios programos kaip Enduro/X (klasterio programų serveris) naudoja šią kalbą. Kadangi Squirrel taip pat naudojama vaizdo žaidimams, kai kurie iš jų yra OpenTTD, GTA IV ir kt.

The stable release of the language is 3.0.7. Įrankių rinkinys, žinomas kaip MirthKit, naudoja Squirrel programavimo kalbą, kad teiktų atvirojo kodo ir kelių platformų dvimačiams žaidimams. Šios kalbos pobūdis yra dinamiškas, o dauguma funkcijų panašios į [Python](/programming/py/), LUA ir kt. Ji taip pat apima registrų VM diegimą. Squirrel našumas yra lėtesnis, palyginti su LŽŪA.

Taip pat yra ir kito tipo .nut plėtinio failo tipas, todėl turėtumėte pažvelgti į failo dydį, kad sužinotumėte, kurį NUT failą turite. Voverės scenarijaus NUT failai dažniausiai yra mažesni nei 1 MB, o vaizdo įrašų NUT failai paprastai yra didesni nei 1 MB.


## NUT failo formato pavyzdys ##

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

## Nuoroda ##

* [NUT – Vikipedijos](https://en.wikipedia.org/wiki/Squirrel_(programming_language))




