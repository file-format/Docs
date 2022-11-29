{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "fil", "tillägg", "filformat", "NUT-programspråk", "Programmeringsguide", "NUT-exempel", "NUT-filformat", "squirrel language", ".nut filändelsefil ", "NUT-filer" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - Squirrel Language File",
  "description":"Läs mer om NUT-filformat och API:er som kan skapa och öppna NUT-filer.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Vad är en NUT fil?

NUT hänvisar till filen NUT Open Container Format. Detta NUT-filformat tillhör programmeringsspråket som är känt som Squirrel. Det är ett objektorienterat programmeringsspråk på hög nivå och imperativt som används mest i inbyggda system och videospel.

Ekorrspråket anses vara ett lättviktigt skriptspråk som enkelt kan justeras efter storlek och bandbredd. Det innebär fördelen med automatisk referensräkning och hantering av skräp i minnet.

Syntaxen för ekorrspråket lockar utvecklarna eftersom det är C-liknande och involverar funktionen av skriptspråk. Men ändå har det ganska färre fördelar jämfört med andra mer populära programmeringsspråk för detta ändamål.



## Kortfattad bakgrund ##

Det designades av Alberto Demichelis 2003. Men en stabil version av detta språk släpptes 2016. Det designades under licensen av zlib/libpng. 2010 ändrades licensen och överfördes till MIT. Detta språk anses vara en inspirerad version av [LUA](/sv/programming/lua/) (Programmeringsspråk). Det finns en lista med förslag på det tidigare språket på webbplatsen designad av Alberto för att göra det mer fördelaktigt.


## Teknisk specifikation ##

Egenskapen och specifikationerna för ekorrspråket är flera. Det ger möjlighet till dynamisk typning, egenskap för delegering, flera användningar av klasser och gränssnitt. Syntaxen för detta språk har en likhet med syntaxen för C-språket. Applikationer som Enduro/X (en klusterapplikationsserver) använder detta språk. Eftersom Squirrel också används för videospel, är några av dessa OpenTTD, GTA IV, etc.

Den stabila versionen av språket är 3.0.7. En verktygslåda känd som MirthKit använder programmeringsspråket Squirrel för att tillhandahålla en öppen källkod och plattformsoberoende för tvådimensionella spel. Det här språkets natur är dynamiskt och de flesta funktioner liknar [Python](/sv/programming/py/), LUA, etc. Det involverar också implementering av registerbaserad VM. Prestandan hos Squirrel är långsammare jämfört med LUA.

Det finns också en annan filtyp för filtillägget ".nut", varför du bör titta på storleken på filen för att ta reda på vilken NUT-fil du har. Squirrel script NUT-filer är oftast mindre än 1 MB medan video NUT-filer vanligtvis är större än 1 MB.


## NUT filformat exempel ##

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

## Referens ##

* [NUT - av Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))



