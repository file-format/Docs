{
"dátum": "2023-08-03",
  "keywords": [
"usr",
"usr fájl",
"mi az usr fájl",
"hogyan kell megnyitni az usr fájlt",
"fájl",
"usr fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "USR fájlformátum - Lowrance GPS adatfájl",
  "description":"További információ az USR-formátumról és az API-król, amelyek USR-fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
      "parent": "gis"
}
},
"lastmod": "2023-08-03"
}

## Mi az az USR fájl?

A ".usr" fájlkiterjesztés a Lowrance GPS-eszközökhöz is kapcsolódik. Különösen a GPS-adatok tárolására szolgál a Lowrance GPS-eszközök által használt "User Data Format" (USR formátum) néven ismert formátumban.

Lowrance GPS egység használatakor az útpontokat, nyomvonalakat és útvonalakat ".usr" fájlként mentheti el. Ezek a fájlok általában olyan információkat tartalmaznak, mint a szélesség, hosszúság, magasság, időbélyeg és egyéb, a GPS-tevékenységekkel kapcsolatos adatok.

Íme néhány általánosan használt .usr fájlok Lowrance GPS-eszközökön:

- **Útpontok:** Az útpontok a GPS-en megjelölt helyek, például tereptárgyak, kedvenc horgászhelyek vagy érdekes helyek. Ezeket a helyeket .usr fájlként mentheti, és importálhatja, exportálhatja vagy megoszthatja más Lowrance GPS-felhasználókkal.

- **Nyomvonalak:** A nyomvonalak a GPS-mozgások rögzített útvonalát jelzik. Nyomkövetési naplóit .usr fájlként mentheti, így később áttekintheti és elemezheti útvonalait, vagy megoszthatja azokat másokkal.

- **Útvonalak:** Az útvonalak előre meghatározott útvonalak, amelyeket létrehozhat és elmenthet GPS-eszközére. Ezek az útvonalak .usr fájlként is menthetők későbbi felhasználás vagy megosztás céljából.

A Lowrance GPS-eszközén lévő .usr fájlok kezeléséhez általában olyan szoftvereket használ, mint a Lowrance "Insight Planner" vagy a "Lowrance GPS Utility" a GPS-adatok importálásához, exportálásához és kezeléséhez.

## USR fájlformátum - További információ

A Lowrance iFinder GPS-eszközökben az .usr fájlok létrejönnek, és az eszközbe helyezett MultiMediaCard (MMC) memóriakártyára kerülnek. Ezek a fájlok felhasználói adatokat tartalmaznak, például útpontokat, nyomvonalakat és útvonalakat.

Az .usr fájlok MMC-ről számítógépre átviteléhez kövesse az alábbi lépéseket:

- ** Távolítsa el az MMC-t:** Óvatosan vegye ki a MultiMediaCard (MMC) kártyát a Lowrance iFinder GPS-eszközből.

- **Helyezze be az MMC-t a számítógépbe:** Használjon megfelelő MMC-kártyaolvasót a memóriakártya behelyezéséhez a számítógép kártyaolvasó-nyílásába.

- **.usr fájlok megkeresése:** Miután a számítógép felismerte az MMC-t, hozzá kell férnie a rajta tárolt fájlokhoz. Keresse meg az .usr fájlokat, amelyek az Ön GPS-adatait tartalmazzák.

- **Konverzió a GPSBabel segítségével:** Az .usr fájlok másik GPS-formátumba konvertálásához használhatja a GPSBabel-t, amely egy ingyenes és nyílt forráskódú eszköz a különféle GPS-fájlformátumok kezelésére. A GPSBabel a bemeneti és kimeneti formátumok széles skáláját támogatja, lehetővé téve az .usr fájlok konvertálását más GPS szoftverekkel vagy eszközökkel kompatibilis formátumokká.

Letöltheti a GPSBabel-t a hivatalos webhelyről (http://www.gpsbabel.org/), és telepítheti számítógépére. A telepítést követően a szoftver parancssori felületét vagy grafikus felhasználói felületét (ha elérhető) használhatja az átalakításhoz.

Például, ha .usr fájlokat szeretne konvertálni GPX formátumba, használhatja a következő parancsokat:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

A fenti parancs arra utasítja a GPSBabelt, hogy olvassa be az "input.usr" bemeneti fájlt Lowrance USR formátumban, és írja be az "output.gpx" kimeneti fájlt GPX formátumban.

- **Konvertált fájlok importálása/használata:** Az átalakítás után a GPS-adatai az új formátumban (pl. GPX) lesznek, amelyeket más GPS-szoftverekkel vagy -eszközökkel is használhat, amelyek támogatják ezt a formátumot.

## USR fájl - Mivel nyitható meg?

Az USR-fájlokat megnyitó vagy hivatkozó programok közé tartoznak

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Hivatkozások
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

