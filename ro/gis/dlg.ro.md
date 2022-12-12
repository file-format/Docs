{
  "date" : "2021-07-30",
  "keywords" :[ "fișier dlg", "format fișier dlg", "ce este un fișier dlg", "fișier", "exemplu dlg", "extensie fișier dlg", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Formatul index al formei Shapefile",
  "description":"Aflați despre formatul de fișier DLG și despre API-urile care pot crea și deschide fișiere DLG.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## Ce este un fișier DLG?
Un fișier cu extensia .dlg conține Digital Line Graph, care este o caracteristică a hărții cartografice prezentată sub formă de vector digital, care este administrată de US Geological Survey (USGS). Fișierele DLG sunt disponibile în două formate diferite:
1. **Format opțional**: un format simplu de utilizat care încorporează o lungime de înregistrare logică de 80 de octeți, sistemul de coordonate la sol UTM și legături de topologie conținute în elemente de linie, nod și zonă.
2. **Format standard de transfer de date spațiale (SDTS)**: un format care facilitează transferul de date spațiale între diferite sisteme informatice.

## Format de fișier DLG
Formatul de fișier DLG este conceput pentru hărțile USGS și sunt transmise la scară mare, intermediară și mică, cu până la nouă categorii diferite de caracteristici. Fișierele DLG vin în formate opționale și Spatial Data Transfer Standard (SDTS) având structurate topologic pentru a fi utilizate în aplicații de cartografiere și GIS.
### Specificații pentru formatul fișierului DLG
Fișierele DLG sunt distribuite la trei scări diferite:

1. **La scară mare** - corespunde în mod normal:
- USGS 7,5 cu 7,5 minute
- Serii de hărți topografice patrulatere la scară 1:24.000 și 1:25.000
- Scara 1:63.360 pentru Alaska
- Scara 1:30.000 pentru Puerto Rico
 

2. **Scara intermediară** - derivat din USGS:

- 30- pe 60 de minute

- Seria de hărți la scară 1:100.000
3. **La scară mică** - derivat din hărțile secționale USGS la scară 1:2.000.000 ale Atlasului Național al Statelor Unite
### Categorii de date
Nouă categorii diferite de straturi sau caracteristici sunt disponibile în fișierele DLG:
1. Sistemul Public de Supraveghere a Terenului (PLSS)
2. Limite (BD)
3. Transport (TR)
4. Hidrografie (HY)
5. Hipografie (HP)
6. Caracteristici non-vegetative (NV)
7. Controlul sondajului și marcatori (SM)

8. Caracteristici create de om (MS)

9. Acoperire vegetativă a suprafeței (SC)

Fișierele DLG la scară mare oferă toate cele nouă straturi, în timp ce la scară intermediară oferă cele cinci straturi PLSS, BD, TR, HY și HP. DLG-urile la scară mică oferă cele cinci straturi de PLSS, BD, TR, HY și MS.

## Referințe

* [Grafic cu linii digitale - de Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


