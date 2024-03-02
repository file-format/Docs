{
  "date": "2020-01-10",
  "keywords": [
"c",
".c",
"cad é comhad ac",
"Conas a oscailt comhad c",
"síneadh",
"comhad",
"c comhad",
"c formáid comhaid",
"c síneadh comhad"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "C - C Comhad Ríomhchlárúcháin Teanga",
  "description": "Foghlaim faoi fhormáid comhaid C agus APIanna ar féidir leo comhaid C a chruthú agus a oscailt.",
  "linktitle": "C",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--gac"
}
},
  "lastmod": "2020-01-10"
}

## Cad is comhad C ann?

Comhad cód foinse atá scríofa i dteanga ríomhchlárúcháin C is ea comhad a shábháiltear le síneadh comhad c. Áirítear leis an gcomhad **C** feidhmiú fheidhmiúlacht an fheidhmchláir go léir i bhfoirm cód foinse. Tá dearbhú an chóid foinse scríofa sna comhaid ceanntásca a shábháiltear leis an iarmhír [.h](/programming/h/). Is é C++ an fhoirm nua-aimseartha de theanga C agus úsáidtear é chun an chuid is mó de na bogearraí a fhorbairt sa lá atá inniu ann.

## Stair Ghearr

Tháinig teanga C i réim mar thoradh ar fhóntais éagsúla a chruthú do chóras oibriúcháin UNIX. Denis Ritchie, an fear a bhí taobh thiar de chruthú na teanga ríomhchlárúcháin seo, a thosaigh an obair ar dtús sna 1960í agus sna 1970idí.

## C Formáid Chomhaid

Scríobhtar comhaid C i bhformáid gnáth-théacs de réir chomhréir na teanga ríomhchlárúcháin. Beidh na nithe seo a leanas i gcomhad tipiciúil C:

 * ráiteas iompórtála ag barr an chomhaid chun aon Chomhaid ceanntásc a allmhairiú
 * modh amháin nó níos mó chun an fheidhmiúlacht atá ag teastáil a chur i bhfeidhm

### Iompórtáil Ceanntásca

Áiríonn na comhaid ceanntásc, le síneadh .h, ráitis riachtanacha chun comhaid feidhmiúlachta eile a áireamh sa tionscadal. Ina theannta sin, cuimsíonn siad seo na dearbhuithe modhanna a shainítear sa chomhad cur chun feidhme. Cuirtear comhaid ceanntásca san áireamh ag baint úsáide as an ráiteas cuimsithe mar a thaispeántar thíos.

```
#include <filename.h>
```

### Forfheidhmiú an Chóid Fhoinsigh

Déantar cur i bhfeidhm iarbhír na gceanglas feidhme a chódú mar mhodhanna sa chomhad C. Tá cineál tuairisceáin, ainm modha ag gach modh i gcomhad C agus d'fhéadfadh go mbeadh roinnt paraiméadair ionchuir aige. Mura bhfuil an cineál tuairisceáin ar neamhní, féadfaidh an modh a bheith ag tabhairt luach áirithe ar ais.

### C Cód Sampla
Seo clár samplach ac:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Tagairtí** ##

* [Forfheidhmiú an Aicme - Le Vicipéid]( https://en.wikipedia.org/wiki/Class_implementation_file)


