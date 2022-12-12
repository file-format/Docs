{
  "date" : "2019-10-11",
  "keywords" :[ "soubor gml", "co je soubor gml", "soubor", "příklad gml", "přípona souboru gml", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Geography Markup Language File Format",
  "description":"Další informace o formátu souborů GML a rozhraních API, která mohou vytvářet a otevírat soubory GML.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor GML?

GML je zkratka pro Geography Markup Language, která je založena na specifikacích XML vyvinutých Open Geospatial Consortium (OGC). Formát se používá k ukládání funkcí geografických dat pro výměnu mezi různými formáty souborů. Slouží jako modelovací jazyk pro geografické systémy a také jako otevřený výměnný formát pro geografické transakce na internetu.

## Formát souboru GML ##

Stejně jako u většiny gramatik založených na XML má gramatika dvě části – schéma, které popisuje dokument, a dokument instance, který obsahuje skutečná data. Dokument GML je popsán pomocí schématu GML. To umožňuje uživatelům a vývojářům popisovat generické sady geografických dat, které obsahují body, čáry a polygony. Pomocí aplikačních schémat mohou uživatelé namísto bodů, čar a polygonů odkazovat na silnice, dálnice a mosty.

Stojí za zmínku, že GML by nemělo být interpretováno pro reprezentaci prostorových dat na mapách. Reprezentace obsahu GML se liší od účelu, pro který byl GML vytvořen. Stručně řečeno, GML je podobný XML v tom, že se používá pouze pro uchovávání prostorového obsahu, který lze použít v mapovacích aplikacích pro účely zobrazení.

### Tvorba obsahu v GML ###

GML představuje prostorová data pomocí prvků, což je seznam vlastností a geometrií. Vlastnost má název, typ a popis hodnoty. Geometrie se skládají ze základních geometrických stavebních bloků, jako jsou:

* body
* čáry
* křivky
* povrchy a
* polygony

Budoucí verze GML jsou plánovány tak, aby podporovaly 3D geometrii i topologické vztahy mezi prvky.

Kódování GML již umožňuje poměrně složité funkce. Prvek může být například složen z jiných prvků. Jediný prvek, jako je letiště, by se tak mohl skládat z dalších prvků, jako jsou pojezdové dráhy, dráhy, hangáry a letištní terminály. Geometrie geografického prvku může být také složena z mnoha prvků geometrie. Geometricky složitý prvek se tak může skládat ze směsi typů geometrie včetně bodů, řetězců čar a mnohoúhelníků.

### Příklady ###

GML 1.0 a 2.0 kódují objekty Polygons, Points a LineString následovně:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Reference ##

* [Specifikace GML](http://www.opengeospatial.org/standards/gml)
* [GML – z Wikipedie](https://en.wikipedia.org/wiki/Geography_Markup_Language)

