{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "file", "extension", "format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a GLTF-fájlokról és API-król, amelyek létrehozhatnak és megnyithatnak GLTF-fájlokat.",
  "title" :"GLTF – GL átviteli fájlformátum",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a GLTF fájl?

A glTF (GL Transmission Format) egy 3D fájlformátum, amely a 3D modellinformációkat JSON formátumban tárolja. A JSON használata minimalizálja a 3D-s eszközök méretét és az eszközök kicsomagolásához és használatához szükséges futásidejű feldolgozást. A 3D jelenetek és modellek alkalmazások általi hatékony átvitelére és betöltésére alkalmazták. A glTF-et a Khronos Group 3D Formats Working Group fejlesztette ki, és alkotói a 3D [JPEG](/hu/image/jpeg/) néven írják le.

A GLTF fájlformátum egy bővíthető, általános közzétételi formátumot határoz meg a 3D-s tartalomeszközök és -szolgáltatások számára, amely leegyszerűsíti a szerzői munkafolyamatokat, és lehetővé teszi a tartalom interoperábilis felhasználását az iparágban. A glTF fájlformátum létrehozásának szándéka egy bővíthető, közös közzétételi formátum meghatározása volt a 3D-s tartalomeszközök és -szolgáltatások számára, amely racionalizálja a szerzői munkafolyamatokat, és lehetővé teszi a tartalom interoperábilis felhasználását az iparágban. Minimalizálja a WebGL-t és más API-kat használó alkalmazások futásidejű feldolgozását.

## A GLTF fájl rövid története

A glTF 1.0 fájlformátum első specifikációit 2015 októberében jelentették be. Ez a Khronos által 2012 márciusában megkezdett erőfeszítések sorozataként jött létre. Ezen erőfeszítések célja a WebGL vontatása körüli lehetőségek felmérése volt. Ennek eredményeként 2012-ben a WebGl találkozón bemutatták a JSON formátumon alapuló glTF formátum első demóját. A formátumot időről időre több cég is átvette, köztük a Cesium, a 3D Tiles, az Oculus, a Microsoft, az Archilogic és mások.

A glTF 2.0 2017. június 5-én jelent meg a Web3D 2017 konferencián. Hosszú azoknak a cégeknek a listája, amelyek ezt követően elfogadták a glTF fájlformátumot.

## GLTF fájlformátum

A glTF 2.0 fájlformátum-specifikációi [online] (https://github.com/KhronosGroup/glTF/tree/master/specification/2.0) elérhetők referenciaként, és minden olvasással/írással kapcsolatos implementációnál tanulmányozni kell őket a glTF fájlformátum.

A glTF az eszközöket külső adatokat támogató JSON-fájlokként határozza meg. 3D-s modelleket ábrázol a következőkkel:

* A jelenet teljes leírása JSON-formátumú .glTF fájlban található, amely információkat tartalmaz a csomópontok hierarchiájáról, az anyagokról, a kamerákról, valamint a hálók, animációk és egyéb konstrukciók leíró adatait
* Bináris fájlok (.bin), amelyek geometriai és animációs adatokat, valamint egyéb pufferalapú adatokat tartalmaznak
* Képfájlok ([.jpg](/hu/image/jpeg/), [.png](/hu/image/png/)) textúrákhoz

Minden külső eszköz, például képek, külső fájlokban tárolódnak, amelyekre URI-n keresztül hivatkoznak. Ezeket az URI-kat a GLB-tároló mellett tárolják, vagy közvetlenül a JSON-ba ágyazzák be adat-URI-k segítségével. Minden érvényes glTF-nek meg kell adnia a verzióját.

A glTF-et úgy tervezték, hogy kis fájlméretet, gyors betöltést, teljes 3D-s jelenetábrázolást és bővíthetőséget érjen el. Ezek az egyedi tervezési célok a fő okai a glTF fájlformátum népszerűségének a 3D tartományban. Az alábbiakban felsoroljuk a glTF fájlformátum által támogatott mime típusokat a különböző fájltípusokhoz:

* A .gltf fájlok a model/gltf+json fájlt használják
* A .bin fájlok application/octet-streamet használnak
* A textúrafájlok a hivatalos kép/* típust használják az adott képformátum alapján. A modern webböngészőkkel való kompatibilitás érdekében a következő képformátumok támogatottak: image/jpeg, image/png.

### JSON kódolás

A glTF a következő további korlátozásokat írja elő a JSON fájlformátumra vonatkozóan

Az ügyféloldali megvalósítás egyszerűsítése érdekében a glTF további korlátozásokat tartalmaz a JSON-formátumra és a kódolásra vonatkozóan.

1. A JSON-nak UTF-8 kódolást kell használnia BOM nélkül.
1. Az ebben a specifikációban definiált összes karakterlánc (tulajdonságnevek, enumok) csak ASCII karakterkészletet használ, és egyszerű szövegként kell megírni, pl. "puffer" a `"\u0062\u0075\u0066\u0066\u0065\u0072"` helyett.
1. A JSON-objektumokon belüli neveknek (kulcsoknak) egyedinek kell lenniük, azaz nem engedélyezettek a duplikált kulcsok.

### URI-k

A pufferekre és a képforrásokra URI-k hivatkoznak. A következő két URI-típust kell támogatniuk az ügyfeleknek.

**Adat URI-k:** Az adat-URI-kat az RFC 2397 határozza meg, és a glTF használja az erőforrások JSON-ba ágyazására.

**Relatív URI-útvonalak:** vagy az RFC 3986 [4.2. szakasza](https://tools.ietf.org/html/rfc3986#section-4.2) által meghatározott útvonal-nosséma – séma, jogosultság vagy paraméterek nélkül. A fenntartott karaktereknek százalékos kódolásúaknak kell lenniük az RFC 3986 [2.2. szakasza] szerint (https://tools.ietf.org/html/rfc3986#section-2.2).

## Hivatkozások ##

* [glTF 2.0 specifikációi – Khronos](https://github.com/KhronosGroup/glTF)
* [glTF fájlformátum – a Wikipédia által](https://en.wikipedia.org/wiki/GlTF)

