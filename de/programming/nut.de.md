{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "Datei", "Erweiterung", "Dateiformat", "NUT-Programmiersprache", "Programmierhandbuch", "NUT-Beispiel", "NUT-Dateiformat", "Eichhörnchensprache", ".nut-Erweiterungsdatei ", "NUT-Dateien" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Eichhörnchen-Sprachdatei",
  "description":"Erfahren Sie mehr über das NUT-Dateiformat und APIs, die NUT-Dateien erstellen und öffnen können.",
  "linktitle" :"MUTTER",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Was ist eine NUT-Datei?

Die NUT bezieht sich auf die NUT Open Container Format-Datei. Dieses NUT-Dateiformat gehört zu der Programmiersprache, die als Squirrel bekannt ist. Es ist eine objektorientierte, anspruchsvolle und imperative Programmiersprache, die hauptsächlich in eingebetteten Systemen und Videospielen verwendet wird.

Die Squirrel-Sprache gilt als leichtgewichtige Skriptsprache, die je nach Größe und Bandbreite einfach angepasst werden kann. Es beinhaltet den Vorteil der automatischen Referenzzählung und der Verwaltung von Müll im Speicher.

Die Syntax der Squirrel-Sprache zieht die Entwickler an, da sie C-ähnlich ist und die Funktion der Skriptsprache beinhaltet. Aber dennoch hat es im Vergleich zu anderen populäreren Programmiersprachen für diesen Zweck deutlich weniger Vorteile.



## Kurze Geschichte ##

Es wurde 2003 von Alberto Demichelis entworfen. Eine stabile Version dieser Sprache wurde jedoch 2016 veröffentlicht. Sie wurde unter der Lizenz von zlib/libpng entwickelt. 2010 wurde die Lizenz geändert und an MIT übertragen. Diese Sprache gilt als inspirierte Version von [LUA](/de/programming/lua/) (Programmiersprache). Es gibt eine Liste mit Vorschlägen für die frühere Sprache auf der von Alberto gestalteten Website, um sie vorteilhafter zu machen.


## Technische Spezifikation ##

Die Merkmale und Spezifikationen der Eichhörnchensprache sind vielfältig. Es bietet die Möglichkeit der dynamischen Typisierung, die Eigenschaft der Delegation, verschiedene Verwendungen von Klassen und Schnittstellen. Die Syntax dieser Sprache hat Ähnlichkeit mit der Syntax der Sprache C. Anwendungen wie Enduro/X (ein Cluster-Anwendungsserver) verwenden diese Sprache. Da Squirrel auch für Videospiele verwendet wird, sind einige davon OpenTTD, GTA IV usw.

Die stabile Version der Sprache ist 3.0.7. Ein Toolkit namens MirthKit verwendet die Programmiersprache Squirrel, um eine Open-Source- und plattformübergreifende Lösung für zweidimensionale Spiele bereitzustellen. Die Art dieser Sprache ist dynamisch und die meisten Funktionen ähneln [Python](/de/programming/py/), LUA usw. Sie beinhaltet auch die Implementierung einer registerbasierten VM. Die Leistung von Squirrel ist im Vergleich zu LUA langsamer.

Es gibt auch einen anderen Dateierweiterungstyp „.nut“, weshalb Sie sich die Größe der Datei ansehen sollten, um herauszufinden, welche NUT-Datei Sie haben. Eichhörnchenskript-NUT-Dateien sind meistens kleiner als 1 MB, während Video-NUT-Dateien normalerweise größer als 1 MB sind.


## Beispiel für ein NUT-Dateiformat ##

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

## Bezug ##

* [NUT - von Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



