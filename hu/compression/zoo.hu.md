{
"dátum":"2023-11-09",
   "keywords":[
"állatkert",
"állatkert fájl",
"zoo tömörített fájl",
"hogyan lehet megnyitni egy állatkerti fájlt",
"fájl",
"zoo fájlkiterjesztés",
"kiterjesztés",
"fájl"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"ZOO Fájl - Mi az .zoo fájl, és hogyan kell megnyitni?",
   "description":"További információ a ZOO tömörített fájlformátumról és az API-król, amelyek ZOO fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
         "parent":"compression"
}
},
"lastmod":"2023-11-09"
}

## Mi az a ZOO fájl?

A ".zoo" fájl egy archív formátum, amely fájlok és könyvtárak tömörítésére és tárolására szolgál; hasonló más archív formátumokhoz, mint például a ".zip", ".tar" és ".rar". A ".zoo" formátum népszerű volt a számítástechnika korai napjaiban, de az utóbbi években kevésbé elterjedt. Eredetileg **Rahul Dhesi** fejlesztette ki, és elsősorban Unix és DOS rendszereken használták.

A ".zoo" fájl általában egy vagy több fájlt és könyvtárat tartalmaz, amelyeket tömörítettek és egyetlen fájlba archiváltak. Létrehozhat és kibonthat ".zoo" fájlokat különféle szoftvereszközökkel, amelyek támogatják ezt a formátumot.

A ZOO archívumok egyedülálló funkcióval rendelkeznek, amely lehetővé teszi ugyanazon fájl több verziójának tárolását, feltéve, hogy mindegyik verziót különböző időpontban módosították. Ez azt jelenti, hogy a ZOO-felhasználók közvetlenül a ZOO archívumából menthetik el és érhetik el a fájl korábbi iterációit. Ez a funkció lehetővé teszi a felhasználók számára, hogy visszatérjenek a fájl korábbi verziójához, vagy összehasonlítsák a régebbi verziót egy újabbal, kényelmes módot kínálva a fájlok módosításainak és időbeli változásainak kezelésére.

## A ZOO fájlok általános műveletei

Íme néhány, a `.zoo` fájlokkal kapcsolatos általános művelet:

1. ** `.zoo` fájl létrehozása:** A `.zoo` fájl létrehozásához használhatja a parancssori segédprogramot, például a "zoo"-t. Például a következő parancs `.zoo` archívumot hoz létre a könyvtárból:
    








`zoo a -c archívum.zoo directory/`
    








Ebben a parancsban az "a" az "add" rövidítése, a "-c" a tömörítést jelöli, az "archive.zoo" pedig a kimeneti archívum neve.
    








2. **Fájlok kibontása `.zoo` fájlból:** A `.zoo` archívum tartalmának kicsomagolásához a következő parancsokat használhatja:
    








`állatkert és archívum.állatkert`
    








Ez a parancs kicsomagolja a fájlokat az "archive.zoo" fájlból.
    








3. **A `.zoo` fájl tartalmának listázása:** A `.zoo` archívum tartalmát listázhatja anélkül, hogy kicsomagolná őket az "l" opció használatával:
    








    








`zoo l archive.zoo`

## ZOO fájl - Mivel nyitható meg egy ZOO fájl?

A ZOO fájlokat megnyitó programok közé tartozik

- **zoo** (ingyenes) (Windows, Linux)

## Hivatkozások
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
