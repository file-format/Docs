{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "fișier", "extensie", "format fișier", "limbaj de programare NUT", "Ghid de programare", "exemplu NUT", "format fișier NUT", "limbaj veveriță", "fișier extensie .nut ", "Fișiere NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Fișier limbaj veveriță",
  "description":"Aflați despre formatul de fișier NUT și despre API-urile care pot crea și deschide fișiere NUT.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Ce este un fișier NUT?

NUT se referă la fișierul NUT Open Container Format. Acest format de fișier NUT aparține limbajului de programare cunoscut sub numele de Squirrel. Este un limbaj de programare orientat pe obiecte, de nivel înalt și imperativ, care este folosit mai ales în sistemele încorporate și jocurile video.

Limbajul veveriță este considerat un limbaj de scripting ușor, care poate fi ușor ajustat în funcție de dimensiune și lățime de bandă. Aceasta implică avantajul numărării automate a referințelor și gestionarea gunoiului în memorie.

Sintaxa limbajului veveriță atrage dezvoltatorii deoarece este asemănătoare C și implică caracteristica limbajului de scripting. Dar totuși, are destul de puține avantaje în comparație cu alte limbaje de programare mai populare în acest scop.



## Scurt istoric ##

A fost proiectat de Alberto Demichelis în 2003. Cu toate acestea, o versiune stabilă a acestui limbaj a fost lansată în 2016. A fost proiectat sub licența zlib/libpng. În 2010, licența a fost schimbată și transferată la MIT. Acest limbaj este considerat o versiune inspirată a [LUA](/ro/programming/lua/) (limbaj de programare). Există o listă de sugestii pentru limba anterioară pe site-ul web conceput de Alberto pentru a o face mai avantajoasă.


## Specificație tehnică ##

Caracteristicile și specificațiile limbajului veveriță sunt multiple. Oferă facilitatea de tastare dinamică, proprietatea delegării, mai multe utilizări ale claselor și interfețelor. Sintaxa acestui limbaj are o asemănare cu sintaxa limbajului C. Aplicații precum Enduro/X (un server de aplicații de cluster) folosesc acest limbaj. Deoarece Squirrel este folosit și pentru jocuri video, unele dintre acestea sunt OpenTTD, GTA IV etc.

Versiunea stabilă a limbii este 3.0.7. Un set de instrumente cunoscut sub numele de MirthKit folosește limbajul de programare Squirrel pentru a oferi o sursă deschisă și o platformă încrucișată pentru jocuri bidimensionale. Natura acestui limbaj este dinamică și majoritatea caracteristicilor sunt similare cu [Python](/ro/programming/py/), LUA, etc. De asemenea, implică implementarea VM-ului bazat pe registre. Performanța lui Squirrel este mai lentă în comparație cu LUA.

Există și un alt tip de fișier cu extensie „.nut”, motiv pentru care ar trebui să vă uitați la dimensiunea fișierului pentru a afla ce fișier NUT aveți. Fișierele NUT cu script Squirrel sunt în mare parte mai mici de 1 MB, în timp ce fișierele video NUT sunt de obicei mai mari de 1 MB.


## Exemplu de format de fișier NUT ##

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

## Referință ##

* [NUT - de Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



