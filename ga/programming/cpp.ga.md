{
  "date": "2019-10-11",
  "keywords": [
"c++",
"comhad",
"síneadh",
"formáid comhaid",
"C++",
"Teanga Ríomhchlárúcháin"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CPP - C++ Comhad Cód Foinse",
  "description": "Foghlaim faoi fhormáid comhaid CPP agus APIanna ar féidir leo comhaid CPP a chruthú agus a oscailt.",
  "linktitle": "CPP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cp-gap"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad C++ ann?

Comhaid le cód foinse iad comhaid a bhfuil síneadh comhad CPP acu le haghaidh feidhmchlár atá scríofa i dteanga ríomhchlárúcháin C++. Féadfaidh níos mó ná comhad CPP amháin a bheith i dtionscadal C++ amháin mar chód foinse an fheidhmchláir. Is éard atá i dtionscadal den sórt sin cineálacha éagsúla comhaid, ar a dtugtar comhaid cur chun feidhme ar na comhaid CPP toisc go bhfuil iontu na sainmhínithe go léir ar na modhanna a dearbhaíodh sa chomhad ceannteidil (.h). Is é an toradh a bhíonn ar thionscadal C++ ina iomláine ná feidhmchlár inrite nuair a chuirtear le chéile ina iomláine é.

## Struchtúr Comhad CPP

Tá struchtúr comhaid CPP simplí i gcomparáid leis na comhaid ceanntásc. Is é príomhchuspóir comhad cur chun feidhme den sórt sin an comhéadan a scaradh ón gcur chun feidhme. Mar thoradh air seo dearbhaítear feidhmeanna na mball go léir i gcomhad ceanntásca agus a sonraí laistigh den chomhad CPP. Is féidir comhad feidhmithe CPP a úsáid mar chomhad simplí chun feidhmchlár a scríobh nó mar chur i bhfeidhm ranga.

### Feidhmiú Neamhspleách

I gcomhad CPP nuair a úsáidtear é mar fheidhmchlár neamhspleách, féadfaidh sé na feidhmiúcháin go léir a chuimsiú ann gan ceanglas maidir le dearbhú modhanna a bheith sa chomhad ceanntásca. Is éard atá i gcur chun feidhme den sórt sin na modhanna go léir a shainítear sa chomhad cur chun feidhme i gcás ina rialaítear iontráil an fheidhmchláir le príomh-mhodh a ghlacann ionchur roghnach úsáideora mar argóintí. Is féidir leis freisin aon leabharlanna ó Leabharlann Caighdeánach C++ a bheidh le húsáid ag aon mhodhanna dearbhaithe sa chomhad.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Feidhmiú Ranga

I gClárú atá Dírithe ar Oibiachtaí (OOP), úsáidtear comhad CPP mar shainiú ranga. I gcás den sórt sin, dearbhaítear gach ball sonraí ranga agus feidhmeanna na mball laistigh den chomhad ceanntásca. Is féidir tagairt a dhéanamh do mhodhanna caighdeánacha leabharlainne freisin i ngach comhad ceanntásc. Tagraíonn an comhad CPP sainmhínithe ranga don chomhad ceanntásca i ráiteas cuimsithe ag tús an chomhaid. Den chuid is mó, cuimsíonn forbróirí bogearraí tuairimí ag tús comhad feidhmithe ranga den sórt sin a sholáthraíonn faisnéis faoi inneachar iarbhír an chomhaid, sonraí an údair agus an dáta feidhmithe. I gcásanna den sórt sin, ní mór na hainmneacha céanna a bheith ar na comhaid cur chun feidhme ceanntásca. Seo a leanas sampla de cheanntásc agus de chomhad feidhmithe dá leithéid.

### Comhad Ceanntásc

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### Comhad Forfheidhmithe CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Tagairtí

* [Forfheidhmiú an Aicme - Le Vicipéid]( https://en.wikipedia.org/wiki/Class_implementation_file)


