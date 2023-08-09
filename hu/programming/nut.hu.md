{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "fájl", "kiterjesztés", "fájlformátum", "NUT programozási nyelv", "Programozási útmutató", "NUT példa", "NUT fájlformátum", "mókus nyelv", ".nut kiterjesztésű fájl", "NUT fájlok" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Squirrel Language File",
  "description":"További információ a NUT fájlformátumról és az API-król, amelyek NUT fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Mi az a NUT fájl?

A NUT a NUT Open Container Format fájlra utal. Ez a NUT fájlformátum a Squirrel néven ismert programozási nyelvhez tartozik. Ez egy objektum-orientált, magas szintű és kötelező programozási nyelv, amelyet leginkább beágyazott rendszerekben és videojátékokban használnak.

A mókusnyelv könnyű szkriptnyelvnek tekinthető, amely könnyen beállítható a méret és a sávszélesség szerint. Ez magában foglalja az automatikus referenciaszámlálás és a memóriában lévő szemétkezelés előnyeit.

A mókusnyelv szintaxisa vonzza a fejlesztőket, mivel C-szerű, és magában foglalja a szkriptnyelv jellemzőit. Ennek ellenére sokkal kevesebb előnnyel rendelkezik, mint más népszerűbb programozási nyelvek erre a célra.



## Rövid története ##

Alberto Demichelis tervezte 2003-ban. Ennek a nyelvnek a stabil verziója azonban 2016-ban jelent meg. A zlib/libpng licence alatt készült. 2010-ben az engedélyt megváltoztatták, és átkerült az MIT-hez. Ez a nyelv a [LUA](/hu/programming/lua/) (programozási nyelv) ihletett változatának tekinthető. Az Alberto által tervezett weboldalon az előbbi nyelvre vonatkozó javaslatok listája található, hogy előnyösebb legyen.


## Műszaki specifikáció ##

A mókusnyelv jellemzői és specifikációi többféleek. Lehetővé teszi a dinamikus gépelést, a delegálás tulajdonságát, az osztályok és interfészek többféle felhasználását. Ennek a nyelvnek a szintaxisa hasonló a C nyelv szintaxisához. Az olyan alkalmazások, mint például az Enduro/X (fürtös alkalmazásszerver), ezt a nyelvet használják. Mivel a Squirrel-t videojátékokhoz is használják, ezek közül néhány OpenTTD, GTA IV stb.

A nyelv stabil kiadása a 3.0.7. A MirthKit néven ismert eszközkészlet Squirrel programozási nyelvet használ, hogy nyílt forráskódú és több platformot biztosítson a kétdimenziós játékokhoz. Ennek a nyelvnek a természete dinamikus, és a legtöbb szolgáltatás hasonló a [Python](/hu/programing/py/), a LUA stb. nyelvhez. A regiszter alapú virtuális gépek megvalósítását is magában foglalja. A Squirrel teljesítménye lassabb a LUA-hoz képest.

Van egy másik ".nut" kiterjesztésű fájltípus is, ezért érdemes a fájl méretét megnézni, hogy megtudja, melyik NUT fájlja van. A Squirrel script NUT fájlok többnyire kisebbek, mint 1 MB, míg a video NUT fájlok általában 1 MB-nál nagyobbak.


## NUT fájlformátum ## példa

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

## Hivatkozási szám

* [NUT – a Wikipédia által](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



