{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CUBE File - Gaussian Cube File - Mi az .cube fájl és hogyan nyitható meg?",
  "description" : "További információ a Gaussian Cube File-ról és a megnyitásáról.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-hu-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Mi az a CUBE fájl?

A CUBE fájlformátumot, más néven Gaussian Cube fájlt (.cube) használják a számítási kémiában molekuláris adatok, különösen a kvantumkémiai számításokból származó elektronsűrűség információ tárolására. Ezt a formátumot általában a **Gaussian szoftvercsomaggal** társítják, amelyet széles körben használnak ab initio elektronikus szerkezeti számítások elvégzésére.

A Gaussian Cube fájlok háromdimenziós adatokat tárolnak, amelyek jellemzően az elektronsűrűséget vagy a molekulák egyéb tulajdonságait reprezentálják, és amelyeket kvantumkémiai számításokkal nyernek. A fájl fejlécet tartalmaz metaadatokkal (például origó, adatpontok száma az egyes tengelyek mentén és térköz), majd a tér minden rácspontjában a számunkra érdekes tulajdonságot (például elektronsűrűséget) reprezentáló számértékek rácsát.

A Gaussian-kocka fájl (.cube) egy egyszerű szöveges fájl, meghatározott szerkezettel. A fejléc információkat tartalmaz a molekuláris rendszerről és az adatrácsról, az adatértékek pedig háromdimenziós rács formátumban vannak elrendezve. A Gaussian Cube fájlokat gyakran használják molekuláris tulajdonságok megjelenítésére molekuláris megjelenítő szoftver segítségével. Az olyan programok, mint a **VMD (Visual Molecular Dynamics)** vagy a **PyMOL**, képesek olvasni a Gauss-kocka fájlokat a molekulafelületek, az elektronsűrűség vagy más számított tulajdonságok megjelenítéséhez.

## Egyszerűsített példa a Gauss-kocka fájlra:

```
Cubefile példa
Gaussian generálta
   0 1 0 0 0 0 0 0 0 0
   0.0000000000000000E+00 0.0000000000000000E+00 0.0000000000000000E+00
  50 0.1000000000000000E+01 0.0000000000000000E+00 0.0000000000000000E+00
  50 0.0000000000000000E+00 0.1000000000000000E+01 0.0000000000000000E+00
  50 0.0000000000000000E+00 0.0000000000000000E+00 0.1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (az elektronsűrűség adatértékei minden rácspontban)
```

## A Gauss-ról

A Gaussian a kvantumkémia és a számítási kémia szoftveralkalmazásainak csomagja. A Gauss-féle elsődleges hangsúly az ab initio kvantumkémiai módszereken van, amelyek rendkívül pontos, de számításigényes megközelítések a molekulák elektronszerkezetének tanulmányozására. A szoftvert széles körben használják kutatási és akadémiai környezetben különféle alkalmazásokhoz, beleértve a molekuláris tulajdonságok előrejelzését, a reakciómechanizmusok tanulmányozását és a molekuláris szerkezetek feltárását.

## Az NWChemről

Az NWChem egy nyílt forráskódú számítási kémiai szoftver, amelyet nagy teljesítményű kvantumkémiai szimulációkhoz terveztek. Olyan ab initio módszereket alkalmaz, mint a Hartree-Fock és a sűrűségfunkcionális elmélet, támogatja a párhuzamos számításokat a klaszterek hatékony számításaihoz, és különféle tudományterületeken talál alkalmazásokat, beleértve a számítási kémiát, a biokémiát és az anyagtudományt. Az NWChem sokoldalúságáról ismert, lehetővé téve a kutatók számára, hogy különféle vegyi rendszereket tanulmányozzanak, és nyílt forráskódú jellege ösztönzi a közösségi hozzájárulásokat és a testreszabást.

## A VMD-ről

A VMD, amely a Visual Molecular Dynamics rövidítése, egy erőteljes és széles körben használt molekuláris vizualizációs program molekuláris dinamikai (MD) pályák, valamint statikus molekuláris struktúrák megjelenítésére, elemzésére és animálására. Különösen népszerű a számítási kémia, a molekuláris biológia és a szerkezeti bioinformatika területén. A VMD kiváló a molekuláris struktúrák megjelenítésében, és kiváló minőségű 3D-s megjelenítést biztosít a molekulákról és molekuláris komplexekről. Számos molekuláris fájlformátumot támogat.

## A PyMOL-ról

A PyMOL egy molekuláris vizualizációs rendszer és szoftvereszköz, amelyet molekuláris szerkezetek háromdimenziós megjelenítésére használnak. Különösen népszerű a szerkezetbiológia, a bioinformatika és a számítási kémia területén. A PyMOL kiváló minőségű 3D-s megjelenítést biztosít a molekuláris szerkezetekről, lehetővé téve a felhasználók számára, hogy vizualizálják és felfedezzék a biológiai makromolekulák alakjait, felületeit és kölcsönhatásait.

## CUBE fájl megnyitása?

A CUBE fájl a következő programokkal nyitható meg és hivatkozhat rájuk.

- **NWChem** (ingyenes) (Windows, MAC, Linux)

## Referenciák
* [Gauss-kocka fájlformátum](https://paulbourke.net/dataformats/cube/)