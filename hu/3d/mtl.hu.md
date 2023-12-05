{
"dátum":"2023-10-11",
   "keywords":[
"mtl",
"mtl fájl",
"mtl obj anyagsablon könyvtár fájl",
"hogyan lehet megnyitni egy mtl fájlt",
"fájl",
"mtl fájl kiterjesztése",
"kiterjesztés",
"fájl"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"MTL fájl formátum - OBJ anyagsablon könyvtár fájl",
   "description":"További információ az MTL OBJ Material Template Library fájlformátumról és az API-król, amelyek MTL fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Mi az MTL fájl?

Az MTL fájl, a **Material Template Library** rövidítése, a 3D számítógépes grafikában és modellezésben használt kísérőfájlformátum. Gyakran társítják a **Wavefront OBJ fájlformátumhoz**, amely a 3D-s modellek és a hozzájuk tartozó anyagok és textúrák tárolásának általános formátuma.

## Anyag sablonkönyvtár

Itt van fontos információ az MTL fájlokról:

1. **Anyagdefiníciók**: Az ".mtl" fájl olyan anyagok definícióit tartalmazza, amelyeket a megfelelő OBJ-fájlban alkalmaznak a 3D objektumokra. Minden anyagdefiníció különböző tulajdonságokat határoz meg, mint például a szín, a fényesség, az átlátszóság és a textúratérképek.
    





2. **Szövegalapú formátum**: Az ".mtl" fájlok jellemzően egyszerű szöveges fájlok, ami azt jelenti, hogy könnyen szerkeszthetők szövegszerkesztővel. Minden anyagdefiníció állítások halmazából áll, és ezek az állítások határozzák meg az anyag tulajdonságait.
    





3. **Texture Mapping**: Az ".mtl" fájl egyik alapvető funkciója annak meghatározása, hogy a textúrák (képfájlok) hogyan legyenek leképezve a 3D modell felületeire. Meghatározza a textúrafájl elérési útját és azt, hogy hogyan kell csomagolni vagy alkalmazni a modellre.
    





4. **Példa MTL-utasításokra**: Íme néhány példa utasítás, amelyeket egy ".mtl" fájlban találhat:
    





- `newmtl MaterialName`: Ez határozza meg az új anyagot "MaterialName" néven.
- "Ka rgb": Az anyag környezeti színe, RGB-értékekben meghatározott.
- `Kd rgb`: Az anyag szórt színe, RGB értékekben megadva.
- "Ks rgb": Az anyag tükröződő színe, RGB értékekben meghatározott.
- "Ns érték": az anyag fényessége vagy tükörkitevője.
- `map_Kd texturefile.jpg`: Diffúz textúratérképet határoz meg az anyaghoz.
5. **Több anyag**: Egy OBJ-fájl több anyagra is hivatkozhat, és minden anyag az ".mtl" fájlban van meghatározva. Ez lehetővé teszi összetett 3D-s modellek készítését, amelyekben különböző anyagokat alkalmaznak a különböző részeken.
    





6. **Kompatibilitás**: Az ".mtl" fájlokat széles körben támogatják a 3D modellező szoftverek és a renderelő motorok, lehetővé téve a 3D modellek és anyagaik átvitelét a különböző szoftveralkalmazások között.

## MTL fájl - Mivel nyitható meg egy MTL fájl?

Az MTL fájlok szöveg alapú fájlok, így bármilyen szövegszerkesztővel megnyithatók, beleértve

- Jegyzettömb (Windows)
- Jegyzettömb++ (Windows)
- Visual Studio kód
- Magasztos szöveg
- Atom
- TextEdit (macOS)

Az MTL fájlokat megnyitó vagy hivatkozó programok közé tartozik

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

**Altípus:** 3D képfájlok

## Hivatkozások
* [Wavefront .obj fájl](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

