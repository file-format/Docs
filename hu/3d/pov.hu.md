
{
  "date": "2023-01-05",
  "keywords": [
"pov fájl",
"pov fájlformátum",
"mi az a pov fájl",
"fájlt",
"pov példa",
"pov fájlkiterjesztés",
"kiterjesztés",
"formátum"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Ismerje meg a POV-fájlformátumot és az API-kat, amelyek képesek POV-fájlok megnyitására és létrehozására.",
  "title": "POV – Persistence of Vision File",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-huv"
}
},
  "lastmod": "2023-01-05"
}

## Mi az a POV fájl?

A POV-fájl egy egyszerű szöveges fájl, amely utasításokat tartalmaz a POV-Ray sugárkövető szoftverhez. Ezek az utasítások egy speciális, a POV-Ray-re jellemző szkriptnyelven vannak megírva. Meghatározza a megjelenítendő jelenetet, beleértve a 3D objektumokat, anyagokat, világítást és egyéb tulajdonságokat, amelyek meghatározzák a jelenet megjelenését. A POV-fájlok egy speciális, a POV-Ray-re jellemző szkriptnyelvet használnak, és összetett és részletes 3D-s jelenetek létrehozására használhatók. A POV-fájlok kiterjesztése általában .pov” vagy .povray”. Amikor megnyit egy POV-fájlt a POV-Ray-ben, a szoftver beolvassa a fájlban található utasításokat, és ezek alapján előállítja a jelenet renderelt képét.

A .pov fájlokat művészek és tervezők gyakran használják 3D-s grafikák és animációk létrehozására különféle alkalmazásokhoz, beleértve a filmeket, a televíziózást, a videojátékokat és a marketinganyagokat.

## POV fájl formátum

A **.pov fájl** általában **#include** utasítások sorozatával kezdődik, amelyek előre meghatározott színek, textúrák és egyéb, a jelenetben használható források könyvtárait tartalmazzák. Ezután a fájl blokkok sorozatával határozza meg a jelenet objektumait, anyagait és egyéb tulajdonságait. Sok más típusú objektum, anyag és egyéb tulajdonság is megadható egy .pov fájlban, és ciklusok és feltételes utasítások segítségével összetettebb és részletesebb jeleneteket hozhat létre.

## Szoftveralkalmazások POV-hoz

A .pov fájlformátumot a POV-Ray ray nyomkövető szoftver használja, így a .pov fájlok megnyitásának elsődleges alkalmazása maga a POV-Ray szoftver. A POV-Ray legújabb verzióját letöltheti a hivatalos webhelyről: https://www.povray.org/.

A POV-Ray mellett számos más alkalmazás is képes megnyitni és szerkeszteni .pov fájlokat, többek között:

- BRL-CAD: Nyílt forráskódú 3D modellező szoftver, amely .pov fájlokat importál és exportál
- MeshLab: 3D mesh-feldolgozó szoftver, amely .pov fájlokat importál és exportál
- Blender: Népszerű nyílt forráskódú 3D grafikus szoftver, amely .pov fájlokat importál és exportál

Más szoftveralkalmazások is képesek megnyitni a .pov fájlokat, ezért érdemes lehet egy fájlnézegetőt vagy konvertáló eszközt használni, ha nem tud megnyitni egy .pov fájlt a fenti alkalmazásokkal.

## POV példa

Például itt van egy minta .pov fájl, amely egyetlen kék hengerrel határoz meg egy jelenetet:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Ebben a példában a kamerablokk határozza meg a kamera helyzetét és tájolását a jelenetben, a light_source blokk deklarál egy fényforrást, és határozza meg a helyzetét és színét, a cilinder blokk pedig egy hengeres objektumot deklarál, és meghatározza annak végpontjait, sugár és anyagtulajdonságok. Amikor megnyitja ezt a .pov fájlt a POV-Ray szoftverben, az egyetlen kék henger képét jeleníti meg.

## Hivatkozások
 * [POV-Ray – Wikipédia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Dokumentációs POV-Ray webhely] (http://www.povray.org/documentation/)

