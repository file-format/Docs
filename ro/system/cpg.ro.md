{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier CPG - fișierul paginii de cod ESRI",
  "description":"Aflați despre formatul fișierului CPG și despre API-urile care pot crea și deschide fișiere CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## Ce este un fișier CPG?

Un fișier CPG este un fișier opțional, care necesită ESRI Shapefile, care este utilizat pentru a specifica pagina de coduri pentru identificarea setului de caractere care urmează să fie utilizat. Acestea sunt stocate în format de fișier text simplu și conțin informații despre codificarea aplicată pentru crearea fișierului de formă. În cazul în care un fișier CPG nu este disponibil, atunci fișierul de formă utilizează codificarea implicită a sistemului. Un fișier CPG, dacă este prezent, trebuie să aibă același prefix ca cel al fișierului [SHP](/ro/gis/shp/), de exemplu, roads.shp, roads.cpg.

Fișierele CPG pot fi deschise cu ESRI ArcGIS Pro.

### Format fișier CPG - Mai multe informații

Când vizualizați un shapefile în ArcCatalog sau orice altă aplicație ArcGIS, vedeți doar shapefile. Dar, în realitate, shapefile utilizează alte fișiere asociate care sunt citite împreună cu fișierul shape principal. Fișierul CPG este, de asemenea, unul dintre acestea dacă este prezent alături de fișierul principal SHP.

## Referințe

* [Extensii de fișiere Shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

