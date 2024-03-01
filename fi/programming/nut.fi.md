{
  "date": "2021-09-23",
  "keywords": [
"MUTTERI",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Pähkinän ohjelmointikieli",
"Ohjelmointiopas",
"Pähkinä esimerkki",
"NUT-tiedostomuoto",
"oravan kieltä",
".nut-päätetiedosto",
"NUT tiedostot"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "Pähkinä - Squirrel Language File",
  "description": "Opi NUT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NUT-tiedostoja.",
  "linktitle": "NUT",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nu-fit"
}
},
  "lastmod": "2021-09-23"
}

## Mikä on NUT-tiedosto?

NUT-tiedostomuoto kuuluu ohjelmointikieleen, joka tunnetaan nimellä Squirrel. Se on oliokeskeinen, korkeatasoinen ja pakottava ohjelmointikieli, jota käytetään enimmäkseen sulautetuissa järjestelmissä ja videopeleissä.

Oravakieltä pidetään kevyenä skriptikielenä, jota voidaan helposti säätää koon ja kaistanleveyden mukaan. Siihen liittyy automaattinen viitelaskenta ja muistissa olevien roskien hallinta.

Oravakielen syntaksi houkuttelee kehittäjiä, koska se on C-tyyppinen ja sisältää komentosarjakielen ominaisuuden. Mutta silti, sillä on melko vähemmän etuja verrattuna muihin suositumpiin ohjelmointikieliin tähän tarkoitukseen.



## Lyhyt historia ##

It was designed by Alberto Demichelis in 2003. Tästä kielestä julkaistiin kuitenkin vakaa versio vuonna 2016. Se on suunniteltu zlib/libpng-lisenssillä. Vuonna 2010 lisenssi muutettiin ja siirrettiin MIT:lle. Tätä kieltä pidetään [LUA](/programming/lua/):n (ohjelmointikieli) innoittamana versiona. Alberton suunnittelemalla verkkosivustolla on luettelo aiemman kielen ehdotuksista tehdäkseen siitä edullisemman.


## Tekniset ominaisuudet ##

Oravakielen ominaisuudet ja tekniset tiedot ovat useita. Se tarjoaa mahdollisuuden dynaamiseen kirjoittamiseen, delegointiominaisuuteen, useisiin luokkien ja rajapintojen käyttötarkoituksiin. Tämän kielen syntaksi on samankaltainen kuin C-kielen syntaksi. Sovellukset, kuten Enduro/X (klusterisovelluspalvelin), käyttävät tätä kieltä. Koska Squirrelia käytetään myös videopeleihin, jotkut niistä ovat OpenTTD, GTA IV jne.

The stable release of the language is 3.0.7. MirthKit-niminen työkalupakki käyttää Squirrel-ohjelmointikieltä tarjotakseen avoimen lähdekoodin ja monialustan kaksiulotteisille peleille. Tämän kielen luonne on dynaaminen, ja useimmat ominaisuudet ovat samanlaisia kuin [Python](/programming/py/), LUA jne. Se sisältää myös rekisteripohjaisen virtuaalikoneen toteutuksen. Squirrelin suorituskyky on hitaampaa kuin LUA.

On myös toinen .nut-tiedostopääte, minkä vuoksi sinun kannattaa katsoa tiedoston kokoa selvittääksesi mikä NUT-tiedosto sinulla on. Squirrel script NUT-tiedostot ovat enimmäkseen pienempiä kuin 1 Mt, kun taas video NUT-tiedostot ovat yleensä suurempia kuin 1 Mt.


## NUT-tiedostomuotoesimerkki ##

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

## Viite ##

* [NUT - Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(ohjelmointikieli))




