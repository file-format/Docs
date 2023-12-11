{
"date":"2023-10-11",
   "keywords":[
"mtl",
"soubor mtl",
"soubor knihovny šablon materiálů mtl obj",
"jak otevřít soubor mtl",
"soubor",
"přípona souboru mtl",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru MTL - soubor knihovny šablon materiálu OBJ",
   "description":"Další informace o formátu souborů knihovny MTL OBJ Material Template Library a rozhraních API, která mohou vytvářet a otevírat soubory MTL.",
   "linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Co je soubor MTL?

Soubor MTL, zkratka pro **Material Template Library**, je doprovodný souborový formát používaný v 3D počítačové grafice a modelování. Často je spojen s **formátem souboru Wavefront OBJ**, což je běžný formát pro ukládání 3D modelů a jejich přidružených materiálů a textur.

## Knihovna šablon materiálů

Zde jsou důležité informace o souborech MTL:

1. **Definice materiálů**: Soubor ".mtl" obsahuje definice materiálů, které jsou aplikovány na 3D objekty v odpovídajícím souboru OBJ. Každá definice materiálu specifikuje různé vlastnosti, jako je barva, lesk, průhlednost a texturní mapy.
    





2. **Text-Based Format**: Soubory ".mtl" jsou obvykle soubory ve formátu prostého textu, což znamená, že je lze snadno upravovat pomocí textového editoru. Každá definice materiálu se skládá ze sady příkazů a tyto příkazy definují vlastnosti materiálu.
    





3. **Mapování textur**: Jednou ze základních funkcí souboru ".mtl" je definovat, jak se textury (soubory obrázků) mapují na povrchy 3D modelu. Určuje cestu k souboru textury a způsob, jakým má být zabalen nebo aplikován na model.
    





4. **Příklady příkazů MTL**: Zde je několik příkladů příkazů, které můžete najít v souboru „.mtl“:
    





- `newmtl MaterialName`: Toto definuje nový materiál s názvem "MaterialName."
- `Ka rgb`: Okolní barva materiálu, specifikovaná v hodnotách RGB.
- `Kd rgb`: Rozptýlená barva materiálu, specifikovaná v hodnotách RGB.
- `Ks rgb`: Odrazová barva materiálu, specifikovaná v hodnotách RGB.
- "Hodnota Ns": Lesklý nebo zrcadlový exponent materiálu.
- `map_Kd texturefile.jpg`: Určuje mapu rozptýlené textury pro materiál.
5. **Více materiálů**: Soubor OBJ může odkazovat na více materiálů a každý materiál je definován v souboru „.mtl“. To umožňuje komplexní 3D modely s různými materiály aplikovanými na různé díly.
    





6. **Kompatibilita**: Soubory ".mtl" jsou široce podporovány softwarem pro 3D modelování a renderovacími moduly, což umožňuje přenášet 3D modely a jejich materiály mezi různými softwarovými aplikacemi.

## Jak otevřít soubor MTL?

Soubory MTL jsou textové soubory, takže je lze otevřít pomocí libovolného textového editoru včetně

- Poznámkový blok (Windows)
- Notepad++ (Windows)
- Visual Studio Code
- Vznešený text
- Atom
- TextEdit (macOS)

Programy, které otevírají nebo odkazují na soubory MTL, zahrnují

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

**Podtyp:** Soubory 3D obrázků

## Reference
* [Soubor .obj Wavefront](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

