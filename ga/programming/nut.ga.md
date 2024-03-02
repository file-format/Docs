{
  "date": "2021-09-23",
  "keywords": [
"NUT",
"comhad",
"síneadh",
"formáid comhaid",
"NUT рrоgramming teanga",
"Treoir Ríomhchlárúcháin",
"NUT shampla",
"Formáid comhaid NUT",
"teanga iora",
".nut comhad síneadh",
"Comhaid NUT"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "NUT - Comhad Teanga Iora",
  "description": "Foghlaim faoi fhormáid comhaid NUT agus APIanna ar féidir leo comhaid NUT a chruthú agus a oscailt.",
  "linktitle": "NUT",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nu-gat"
}
},
  "lastmod": "2021-09-23"
}

## Cad is comhad NUT ann?

Baineann formáid comhaid NUT leis an teanga ríomhchlárúcháin ar a dtugtar Iora. Is teanga ríomhchlárúcháin atá dírithe ar oibiachtaí, ardleibhéil agus ríthábhachtach í a úsáidtear go príomha i gcórais leabaithe agus i bhfíschluichí.

Meastar gur teanga éadrom scriptithe í an teanga iora ar féidir a choigeartú go héasca de réir méid agus bandaleithead. Baineann sé leis an leas a bhaint as comhaireamh tagartha uathoibríoch agus bainistiú truflais cuimhne.

Meallann comhréir na teanga iora na forbróirí mar go bhfuil sí cosúil le C agus baineann sé le gné na teanga scriptithe. Ach fós féin, tá i bhfad níos lú buntáistí ag baint leis i gcomparáid le teangacha ríomhchlárúcháin eile a bhfuil tóir orthu chun na críche seo.



## Stair Ghearr ##

It was designed by Alberto Demichelis in 2003. Mar sin féin, eisíodh leagan cobhsaí den teanga seo in 2016. Dearadh é faoi cheadúnas zlib/ libpng. In 2010 athraíodh an ceadúnas agus aistríodh chuig MIT é. Breathnaítear ar an teanga seo mar leagan spreagtha de [LUA](/programming/lua/) (Teanga ríomhchlárúcháin). Tá liosta moltaí don iar-theanga ar an suíomh Gréasáin atá deartha ag Alberto le go mbeidh sé níos tairbhí.


## Sonraíocht Theicniúil ##

Tá gné agus sonraíochtaí teanga an iora iolrach. Soláthraíonn sé áis do chlóscríobh dinimiciúil, maoin an tarmligin, roinnt úsáidí ranganna agus comhéadain. Tá cosúlacht idir comhréir na teanga seo agus comhréir na teanga C. Úsáideann feidhmchláir ar nós Enduro/X (freastalaí feidhmchlár braisle) an teanga seo. Toisc go n-úsáidtear Iora le haghaidh cluichí físeáin freisin, tá cuid acu sin OpenTTD, GTA IV, etc.

The stable release of the language is 3.0.7. Úsáideann foireann uirlisí ar a dtugtar MirthKit teanga ríomhchláraithe Squirrel chun foinse oscailte agus tras-ardán a sholáthar do chluichí déthoiseacha. Tá nádúr na teanga seo dinimiciúil agus tá an chuid is mó de na gnéithe cosúil le [Python](/programming/py/), LUA, etc. Baineann sé freisin le cur i bhfeidhm clár-bhunaithe VM. Tá feidhmíocht Iora níos moille i gcomparáid le LUA.

Tá cineál comhaid síneadh .nut eile ann freisin agus is é sin an fáth gur chóir duit breathnú ar mhéid an chomhaid chun a fháil amach cén comhad NUT atá agat. Tá comhaid NUT script iora níos lú ná 1 MB den chuid is mó ach bíonn comhaid físe NUT níos mó ná 1 MB de ghnáth.


## Sampla Formáid Chomhaid NUT ##

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

## Tagairt ##

* [NUT - le Vicipéid](https://en.wikipedia.org/wiki/Squirrel_(programming_language))




