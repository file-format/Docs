
{
  "date": "2023-01-05",
  "keywords": [
"pov soubor",
"formát souboru pov",
"co je soubor pov",
"soubor",
"pov příklad",
"přípona souboru pov",
"rozšíření",
"formát"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Přečtěte si o formátu souboru POV a rozhraních API, která mohou otevírat a vytvářet soubory POV.",
  "title": "POV - Persistence of Vision File",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-csv"
}
},
  "lastmod": "2023-01-05"
}

## Co je soubor POV?

Soubor POV je prostý textový soubor, který obsahuje pokyny pro software pro sledování paprsku POV-Ray. Tyto instrukce jsou napsány ve speciálním skriptovacím jazyce, který je specifický pro POV-Ray. Určuje scénu, která se má vykreslit, včetně 3D objektů, materiálů, osvětlení a dalších vlastností, které definují vzhled scény. Soubory POV používají speciální skriptovací jazyk, který je specifický pro POV-Ray a lze jej použít k vytváření složitých a detailních 3D scén. Přípona souboru pro soubor POV je obvykle .pov nebo .povray. Když otevřete soubor POV v POV-Ray, software přečte pokyny v souboru a použije je ke generování vykresleného obrazu scény.

Soubory .pov často používají umělci a návrháři k vytváření 3D grafiky a animací pro různé aplikace, včetně filmu, televize, videoher a marketingových materiálů.

## Formát souboru POV

Soubor **.pov** obvykle začíná sérií příkazů **#include**, které se používají k zahrnutí knihoven předdefinovaných barev, textur a dalších zdrojů, které lze ve scéně použít. Poté soubor definuje objekty, materiály a další vlastnosti scény pomocí řady bloků. Existuje mnoho dalších typů objektů, materiálů a dalších vlastností, které můžete zadat v souboru .pov, a můžete použít smyčky a podmíněné příkazy k vytvoření složitějších a podrobnějších scén.

## Softwarové aplikace pro POV

Formát souboru .pov používá software pro sledování paprsků POV-Ray, takže primární aplikací pro otevírání souborů .pov je samotný software POV-Ray. Nejnovější verzi POV-Ray si můžete stáhnout z oficiálních stránek https://www.povray.org/.

Kromě POV-Ray existuje řada dalších aplikací, které mohou otevírat a upravovat soubory .pov, včetně:

- BRL-CAD: Software pro 3D modelování s otevřeným zdrojovým kódem, který dokáže importovat a exportovat soubory .pov
- MeshLab: Software pro zpracování 3D sítě, který dokáže importovat a exportovat soubory .pov
- Blender: Populární open-source 3D grafický software, který dokáže importovat a exportovat soubory .pov

Mohou existovat další softwarové aplikace, které mohou také otevřít soubory .pov, takže pokud nemůžete otevřít soubor .pov pomocí výše uvedených aplikací, můžete zkusit použít prohlížeč souborů nebo nástroj pro převod souborů.

## Příklad POV

Zde je například ukázkový soubor .pov, který definuje scénu s jedním modrým válcem:

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

V tomto příkladu blok kamery určuje polohu a orientaci kamery ve scéně, blok `light_source` deklaruje zdroj světla a určuje jeho polohu a barvu a blok `cylindr` deklaruje objekt válce a určuje jeho koncové body, poloměr a vlastnosti materiálu. Když tento soubor .pov otevřete v softwaru POV-Ray, vykreslí se obrázek jednoho modrého válce.

## Reference
 * [POV-Ray – Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Webová stránka Dokumentace POV-Ray](http://www.povray.org/documentation/)

