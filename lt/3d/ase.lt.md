{
  "date": "2021-01-22",
  "keywords": [
"ASE",
"failą",
"formatu",
"Failo tipas",
"pratęsimas",
"kas yra ASE failas?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie ASE failo formatą ir API, kurios gali atidaryti ir kurti ASE failus.",
  "title": "ASE – Autodesk ASCII scenos eksporto failas",
  "linktitle": "ASE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-as-lte"
}
},
  "lastmod": "2021-01-22"
}

## Kas yra ASE failas?

A file with a .ase extension is an Autodesk ASCII Scene Export file format that is an ASCII representation of a scene, containing 2D or 3D information while exporting scene data using Autodesk. Autodesk provides options to include scene components while exporting scene data. You can include Mesh definition along with vertex and face information, Material description, transform animation data for the objects, complete mesh definition of every n frames, animation data for cameras and lights and IK joint settings.

## ASE failo formatas – daugiau informacijos

ASE failai yra tekstiniai failai, saugomi ASCII formatu, kuriuos galima atidaryti bet kuriame teksto rengyklėje. ASE faile gali būti šių tipų Autodesk teikiamos informacijos.

### Išvesties parinktys

 * Tinklo apibrėžimas – eksportuoja kiekvieno tinklelio apibrėžimą, įskaitant geometrinių objektų viršūnių ir paviršių informaciją. Be to, įjungus šią funkciją, įjungiami elementai, esantys grupės tinklelio parinktyse, aprašyta toliau.
 * `Materials` - Includes the material description. If a material is not assigned to an object, its wireframe color is exported. All levels of a material tree are included, so this can produce a lot of text.
 * Transformuoti animacijos raktus – apima objektų transformacijos animacijos duomenis. Jei objektas yra tikslinė kamera arba prožektorius, bus įtraukti tikslinės animacijos duomenys.
 * Animuotas tinklelis – eksportuoja visą tinklelio apibrėžimą kas n kadrų. Dažnį nurodo toliau aprašytas valdiklio išvesties suktukas. Kiekviename bloke yra ta pati informacija, nurodyta grupės tinklelio parinktyse, aprašyta toliau. Įjungus tai gali būti sukurtas didžiulis failas, net ir mažoms scenoms.
 * Animuotos kameros / šviesos nustatymai – eksportuoja kamerų ir šviesų animacijos duomenis, pvz., spalvą, intensyvumą, kritimą, žemėlapio paklaidą ir pan. Išveda bloką kas n kadrų, kaip nurodo valdiklio išvesties suktukas.
 * Atvirkštinės kinematinės jungtys – eksportuoja IK jungties nustatymus į hierarchijos šaką.

### Objektų tipai

Čia esantys elementai leidžia nurodyti, kurią objekto kategoriją norite įtraukti į išvestį. Galite įtraukti geometrinius objektus, figūras, kameras, šviesas ir pagalbinius objektus.

 * Geometrinis
 * Formos
 * Fotoaparatai
 * Šviesos
 * Pagalbininkai

### Tinklo parinktys

 * Mesh Normals – eksportuoja veido ir viršūnių normaliuosius elementus. Pirmiausia pateikiamas veido normalus, o po to – trijų veidą laikančių viršūnių normaliosios. Įjungus tai, gaunamas daug didesnis failas.
 * Mapping Coordinates – eksportuoja atvaizdavimo viršūnių ir veidų sąrašą pagal TVert ir TVFace struktūras, aprašytas 3ds Max programinės įrangos kūrimo rinkinyje. Jei objektas naudoja veido atvaizdavimą, eksportuojamas veidų žemėlapio sąrašas, kuriame yra kiekvieno veido UVW koordinatės.
 * Vertex Colors – eksportuoja viršūnių spalvas.

### Valdiklio išvestis

 * Naudoti raktus – eksportuoja raktų reikšmes. Jei valdiklis nenaudoja klavišų, naudojamas Force Sample metodas. Transformacijos valdiklių atveju parinktis Naudoti raktus veikia tik tuo atveju, jei visi transformavimo valdikliai yra linijiniai / TCB arba Bezier. Jei viename iš transformavimo takelių naudojamas kitokio tipo valdiklis, visiems transformavimo takeliams naudojamas Force Sample metodas.
 * Force Samples – atrenka valdiklio vertes pagal dažnį, nurodytą Frames per Sample Controller.

## Nuorodos

 * [Autodesk – eksportavimas į ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

