{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "fájl", "kiterjesztés", "fájlformátum", "ICI implementáció", "Programozási útmutató", "ici példa", "ICI programozási nyelv", "ICI moduljai", "ICI adatmodellje", "ICI dokumentációja", "ICI nyelv" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - programozási nyelvi fájl",
  "description":"További információ az ICI fájlformátumról és az API-król, amelyek ICI-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Mi az ICI fájl?

Az értelmezett általános célú programozási nyelv, amely számos funkciót, például dinamikus gépelést és rugalmas adattípusokat tartalmaz, ICI (nem mozaikszó) programozási nyelvként ismert. Hasonlónak tekinthető a [Perl](/hu/programing/pl/) nyelvhez. Ez az ICI nyelv folyamvezérlő konstrukciókat és a C nyelv néhány operátorát is tartalmazza. Ez nem egy objektum-orientált nyelv, de az OOP néhány jellemzője elérhető egy speciális öröklési módszerrel, amelyet szuperstruktúráknak nevezünk. A [C](/hu/programozás/c)-hez hasonlóan ez az ICI programozási nyelv is ugyanazzal a rendszerfelülettel és szabványos könyvtárral rendelkezik a beépített funkciókhoz.


## Rövid története ##

Az 1980-as évek végén Tim Long fejlesztette ki általános célú értelmezett programozási nyelvként. Ennek a nyelvnek a legtöbb funkciója hasonló a C-hez, és néhány jellemzőt speciális módszerekkel is el tud érni. Ez a nyelv nyilvános tulajdonban van, és továbbértékesíthető nyelvként is elérhető, és senki sem köteles megemlíteni, honnan szerezte a forráskódot. Az ICI dokumentációja a Canon Information System Research Australia szerzői joga alá tartozik.

## Műszaki specifikáció ##

Ezen a nyelven két különböző adattípust használnak. Ez a kettő primitív és összesített adattípus. Mindkettő különböző kifejezéseket tartalmaz a nyelvben előre meghatározott összetételük szerint. Ez a nyelv különböző modulokat támogat, például beágyazott és szubrutinokat. Mivel egyes tulajdonságai hasonlóak a Perlhez, szigorúan integrálódik a reguláris kifejezésekkel.

A halmazok heterogének és egymásba ágyazottak lehetnek. Ezek a készletek támogatják az általánosan használt halmazműveleteket, mint például az Unió és az Intersection stb. Leginkább nyelvként használják a multinacionális szervezetek tulajdonában lévő alkalmazások alapvető megvalósítása érdekében.

Szinte minden típusú program írható ezen a nyelven, és többnyire azok a speciális programok, amelyek összetett adatstruktúrákat tartalmaznak, az ICI programozási nyelven íródnak. Az alkalmazások tartalmazhatják az ICI implementációt oly módon, hogy bele kell írni őket. Az alkalmazás funkcionális részei megvalósíthatók az ICI moduljaival. Az ICI nyelve némileg hasonlít a C nyelvre, de az ICI adatmodellje meglehetősen magasabb szintű, és olyan típusokkal különbözik, mint a szótárak (struct), halmazok, dinamikus tömbök, reguláris kifejezések és (valós) karakterláncok.


## ICI fájlformátum példa ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Hivatkozási szám

* [ICI programozási nyelv](http://atrn.org/ici/doc/ici.html)



