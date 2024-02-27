{
  "date": "2021-09-23",
  "keywords": [
"NØD",
"fil",
"udvidelse",
"filformat",
"NØDDERPROGRAMMERINGSsprog",
"Programmeringsvejledning",
"NUT eksempel",
"NUT filformat",
"egern sprog",
".nut filtypenavnet",
"NUT filer"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "NUT - Squirrel Language File",
  "description": "Lær om NUT-filformat og API'er, der kan oprette og åbne NUT-filer.",
  "linktitle": "NUT",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nu-dat"
}
},
  "lastmod": "2021-09-23"
}

## Hvad er en NUT fil?

NUT-filformatet tilhører programmeringssproget, der er kendt som Squirrel. Det er et objektorienteret programmeringssprog på højt niveau og bydende nødvendigt, som mest bruges i indlejrede systemer og videospil.

Egernsproget betragtes som et letvægts scriptsprog, der nemt kan justeres efter størrelse og båndbredde. Det involverer fordelen ved automatisk referencetælling og håndtering af skrald i hukommelsen.

Syntaksen af egernsproget tiltrækker udviklerne, da det er C-lignende og involverer scriptsprogets egenskab. Men stadig har det ganske færre fordele sammenlignet med andre mere populære programmeringssprog til dette formål.



## Kort historie ##

It was designed by Alberto Demichelis in 2003. Imidlertid blev en stabil version af dette sprog udgivet i 2016. Det blev designet under licensen af zlib/libpng. I 2010 blev licensen ændret og overført til MIT. Dette sprog betragtes som en inspireret version af [LUA](/programming/lua/) (programmeringssprog). Der er en liste med forslag til det tidligere sprog på webstedet designet af Alberto for at gøre det mere fordelagtigt.


## Teknisk specifikation ##

Egernsprogets egenskaber og specifikationer er flere. Det giver mulighed for dynamisk indtastning, egenskab for delegering, flere anvendelser af klasser og grænseflader. Syntaksen for dette sprog har en lighed med syntaksen for C-sproget. Applikationer såsom Enduro/X (en klyngeapplikationsserver) bruger dette sprog. Da Squirrel også bruges til videospil, er nogle af dem OpenTTD, GTA IV osv.

The stable release of the language is 3.0.7. Et værktøjssæt kendt som MirthKit bruger Squirrel programmeringssprog til at give en open source og cross-platform til todimensionelle spil. Naturen af dette sprog er dynamisk, og de fleste funktioner ligner [Python](/programming/py/), LUA osv. Det involverer også implementering af registerbaseret VM. Squirrels ydeevne er langsommere sammenlignet med LUA.

Der er også en anden .nut filtypenavn, hvorfor du bør se på størrelsen på filen for at finde ud af, hvilken NUT-fil du har. Squirrel script NUT-filer er for det meste mindre end 1 MB, mens video NUT-filer normalt er større end 1 MB i størrelse.


## NUT filformat eksempel ##

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

## Reference ##

* [NUT - af Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))




