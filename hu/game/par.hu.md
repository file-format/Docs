{
"dátum":"2023-07-18",
   "keywords":[
"PAR",
"PAR fájl",
"fájl",
"PAR fájl kiterjesztése",
"kiterjesztés",
"fájl"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"PAR fájlformátum - FMS repülőgép-paraméterek fájl",
   "description":"További információ a PAR-formátumról és az API-król, amelyek PAR-fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"game-par",
         "parent":"game"
}
},
"lastmod":"2023-07-18"
}

## Mi az a PAR fájl?

A PAR-fájlt, amelyet általában repülőgép-paraméter-fájlként ismernek, kifejezetten az FMS (Flying-Model-Simulator), egy Windows operációs rendszerekhez tervezett repülésszimulációs játék használ. Célja a repülőgép geometriájára és fizikai jellemzőire vonatkozó kulcsfontosságú adatok tárolása, beleértve az olyan tulajdonságokat, mint a tömeg, a súlypont és a tehetetlenségi nyomatékok. Ezek a PAR fájlok fontos szerepet játszanak a testreszabott repülőgépek létrehozásában a játékon belül, lehetővé téve a játékosoknak, hogy szimulálják és repüljék saját egyedi virtuális repülőgépeiket, pontos és valósághű fizikával.

## PAR fájlformátum - További információ

Az FMS egy repülőgépeken használt szoftverrendszer, amely segíti a navigációt, a repüléstervezést és az autopilóta funkciókat. Az FMS Aircraft Parameters File, amelyet gyakran PAR fájlnak is szoktak rövidíteni, a repülőgép teljesítményjellemzőivel és repüléskezelésével kapcsolatos konkrét adatokat tartalmaz.

Ez a PAR fájlformátum a repülésszimulációs szoftverekre jellemző, például az olyan népszerű repülésszimulátor-programokban, mint a Microsoft Flight Simulator vagy az X-Plane. A fájl különféle paramétereket és adatokat tartalmaz, amelyek meghatározzák a szimulátoron belüli virtuális repülőgép viselkedését, teljesítményét és rendszereit.

Az FMS Aircraft Parameters fájl általában olyan információkat tartalmaz, mint:

- **Repülőgép specifikációi:** Ez magában foglalja a repülőgép fizikai jellemzőinek részleteit, például tömegét, méreteit, üzemanyag-kapacitását és a motor jellemzőit.

- **Repülési teljesítményadatok:** A repülőgép teljesítményére vonatkozó adatokat tartalmaznak a repülés különböző fázisaiban, beleértve az emelkedést, az utazást, a süllyedést és a leszállást. Ez magában foglalhatja az emelkedési sebességeket, az üzemanyag-fogyasztási arányokat, a sebességkorlátozásokat és más, a teljesítménnyel kapcsolatos paramétereket.

- **Autopilot beállításai:** A fájl meghatározhatja a repülőgép robotpilóta viselkedését és korlátozásait, beleértve az autopilot módokat, a magassági és iránykorlátokat, valamint a vezérlés érzékenységét.

- **Navigációs adatok:** Tartalmazhatnak navigációval kapcsolatos paramétereket, például a repülőgép navigációs adatbázisát, beleértve az útpontokat, a légutakat és a repülőtéri adatokat.

Ezeket a PAR fájlokat általában repülőgép-fejlesztők vagy külső rajongók hozzák létre és karbantartják, akiknek célja, hogy valósághű és pontos szimulációs élményt nyújtsanak a repülésszimulátor szoftveren belül. A fájlok ezután betöltődnek a szimulátorba, hogy meghatározzák a szimulált repülőgép viselkedését és teljesítményjellemzőit.

## A PAR fájlok, 3D modellek, textúrák és hangok szerepe a repülésszimulációs játékokban

A PAR fájlok csak egy részét képezik a teljes repülőgép-adatcsomagnak. A PAR fájlok mellett számos más fájl is létezik, amelyek együttesen hozzájárulnak egy repülőgép teljes ábrázolásához a játékon belül. Ezek a további fájlok általában 3D modellfájlokat, textúra bittérképeket és hangokat tartalmaznak.

- **3D-s modellfájlok:**

A repülésszimulációs játékokhoz részletes 3D-s modellekre van szükség ahhoz, hogy vizuálisan ábrázolják a repülőgépet a virtuális környezetben. Ezek a 3D modellek különböző alkatrészekből állnak, mint például a törzs, a szárnyak, a futómű és a repülőgép egyéb bonyolult részei. A 3D-s modellfájlok biztosítják a repülőgép megjelenésének és alakjának pontos ábrázolásához szükséges vizuális szerkezetet és geometriát a játékon belül.

- **Texture Bitmaps:**

A textúra bittérképek, más néven textúrák vagy képtérképek, a 3D modellek színének, felületi részleteinek és vizuális valósághűségének adására szolgálnak. Ezek a textúrafájlok olyan információkat tartalmaznak, mint a festéksémák, matricák, logók és felületi textúrák, például fém, műanyag vagy szövet. A textúra bittérképek 3D modellekre történő alkalmazásával a játékban lévő repülőgépek vizuálisan javíthatók, ami magával ragadóbb és vizuálisan vonzóbb élményt eredményez.

- **Hangok:**

A hangfájlok a repülésszimulációs játékok elengedhetetlen elemei, mivel hallási visszajelzést és valósághűséget biztosítanak. Ezek a fájlok jellemzően tartalmazzák a motorhangokat, a pilótafülke hangjait, a környezeti hatásokat, mint például a szél vagy az eső, és más, repülőgép-specifikus hangjelzéseket. A megfelelő hangfájlok beépítésével a játék pontosan újra tudja teremteni a szimulált repülőgéphez kapcsolódó hangkörnyezetet, tovább fokozva az általános elmélyülést.

Míg a PAR fájl konkrét adatokat tartalmaz a repülőgép teljesítményével és repüléskezelésével kapcsolatban, a PAR fájlok, 3D modellfájlok, textúra bittérképek és hangfájlok kombinációja együttesen kelt életre a virtuális repülőgépet a repülésszimulációs játékban. Minden fájl egyedi célt szolgál a repülőgép átfogó és valósághű ábrázolásának létrehozásában, amely magával ragadó élményt biztosít a játékosok számára.

## PAR fájl - Mivel nyitható meg egy PAR fájl?

A PAR fájlokat megnyitó programok közé tartozik

- Repülő modell-szimulátor (FMS)
- Microsoft Flight Simulator
- X-Plane

## Hivatkozások
* [Flying-Model-Simulator (FMS)](https://modelsimulator.com/)
* [Microsoft Flight Simulator](https://en.wikipedia.org/wiki/Microsoft_Flight_Simulator)


