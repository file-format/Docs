{
  "date" : "2021-07-30",
  "keywords" :[ "soubor dlg", "formát souboru dlg", "co je soubor dlg", "soubor", "příklad dlg", "přípona souboru dlg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Formát indexu tvaru Shapefile",
  "description":"Další informace o formátu souboru DLG a rozhraních API, která mohou vytvářet a otevírat soubory DLG.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Co je soubor DLG?
Soubor s příponou .dlg obsahuje Digital Line Graph, což je kartografický mapový prvek zobrazený v digitální vektorové podobě, který spravuje US Geological Survey (USGS). Soubory DLG jsou k dispozici ve dvou různých formátech:
1. **Volitelný formát**: Snadno použitelný formát, který zahrnuje 80bajtovou délku logického záznamu, pozemní souřadnicový systém UTM a topologické vazby obsažené v liniových, uzlových a plošných prvcích.
2. **Formát SDTS (Spatial Data Transfer Standard)**: formát, který usnadňuje přenos prostorových dat mezi různými počítačovými systémy.

## Formát souboru DLG
Formát souboru DLG je určen pro mapy USGS a jsou přenášeny ve velkém, středním a malém měřítku s až devíti různými kategoriemi funkcí. Soubory DLG přicházejí ve volitelných formátech a formátech SDTS (Spatial Data Transfer Standard), které mají topologickou strukturu pro použití v mapových a GIS aplikacích.
### Specifikace formátu souboru DLG
Soubory DLG jsou distribuovány ve třech různých měřítcích:

1. **Velké měřítko** – obvykle odpovídá:
- USGS 7,5 krát 7,5 minuty
- série topografických čtyřúhelníků v měřítku 1:24 000 a 1:25 000
- Měřítko 1:63 360 pro Aljašku
- Měřítko 1:30 000 pro Portoriko
 

2. **Střední stupnice** – odvozeno z USGS:

- 30-krát 60 minut

- Mapové série v měřítku 1:100 000
3. **Malé měřítko** – odvozeno z sekčních map USGS v měřítku 1:2 000 000 Národního atlasu Spojených států
### Datové kategorie
V souborech DLG je k dispozici devět různých kategorií vrstev nebo funkcí:
1. Systém veřejného průzkumu půdy (PLSS)
2. Hranice (BD)
3. Doprava (TR)
4. Hydrografie (HY)
5. Hypsografie (HP)
6. Nevegetativní znaky (NV)
7. Kontrola a značky průzkumu (SM)

8. Uměle vytvořené prvky (MS)

9. Vegetativní povrchový kryt (SC)

Velké soubory DLG nabízejí všech devět vrstev, zatímco středně velké soubory nabízejí pět vrstev PLSS, BD, TR, HY a HP. Malé DLG nabízejí pět vrstev PLSS, BD, TR, HY a MS.

## Reference

* [Digitální spojnicový graf – od Wikipedie)](https://en.wikipedia.org/wiki/Digital_line_graph)


