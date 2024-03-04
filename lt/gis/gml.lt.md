{
  "date": "2019-10-11",
  "keywords": [
"gml failą",
"kas yra gml failas",
"failą",
"gml pavyzdys",
"gml failo plėtinį",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GML – geografijos žymėjimo kalbos failo formatas",
  "description": "Sužinokite apie GML failo formatą ir API, kurios gali kurti ir atidaryti GML failus.",
  "linktitle": "GML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gm-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra GML failas?

GML reiškia geografijos žymėjimo kalbą, kuri yra pagrįsta XML specifikacijomis, kurias sukūrė Open Geospatial Consortium (OGC). Formatas naudojamas saugoti geografinių duomenų ypatybes, kad būtų galima keistis tarp skirtingų failų formatų. Jis naudojamas kaip geografinių sistemų modeliavimo kalba, taip pat kaip atviras mainų formatas geografinėms operacijoms internete.

## GML failo formatas ##

Kaip ir daugelyje XML pagrįstų gramatikų, gramatiką sudaro dvi dalys – schema, apibūdinanti dokumentą, ir egzemplioriaus dokumentas, kuriame yra tikrieji duomenys. GML dokumentas aprašomas naudojant GML schemą. Tai leidžia vartotojams ir kūrėjams apibūdinti bendruosius geografinių duomenų rinkinius, kuriuose yra taškų, linijų ir daugiakampių. Naudodami programų schemas, vartotojai gali nurodyti kelius, greitkelius ir tiltus, o ne taškus, linijas ir daugiakampius.

Verta paminėti, kad GML neturėtų būti interpretuojamas kaip erdvinių duomenų atvaizdavimas žemėlapiuose. GML turinio vaizdavimas skiriasi nuo tikslo, kuriam buvo sukurtas GML. Trumpai tariant, GML yra panašus į XML, nes jis naudojamas tik erdviniam turiniui, kurį galima naudoti atvaizdavimo programoms rodyti, laikyti.

### Turinio formavimas GML ###

GML represents spatial data using features which is a list of properties and geometries. A Property has a name, type and value description. Geometries are composed of basic geometry building blocks such as:

* taškai

* linijos

* kreivės

* paviršiai ir

* daugiakampiai


Planuojama, kad būsimos GML versijos palaikys 3D geometriją ir topologinius ryšius tarp funkcijų.

GML kodavimas jau leidžia naudoti gana sudėtingas funkcijas. Pavyzdžiui, funkcija gali būti sudaryta iš kitų funkcijų. Taigi vieną elementą, pavyzdžiui, oro uostą, gali sudaryti kitos funkcijos, pvz., riedėjimo takai, kilimo ir tūpimo takai, pakabos ir oro terminalai. Geografinio objekto geometrija taip pat gali būti sudaryta iš daugelio geometrijos elementų. Taigi geometriškai sudėtingas elementas gali būti sudarytas iš įvairių geometrijos tipų, įskaitant taškus, linijų eilutes ir daugiakampius, derinys.

### Pavyzdžiai ###

GML 1.0 ir 2.0 koduoja daugiakampius, taškus ir linijos eilutes taip:

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

## Nuorodos Nr.

* [GML specifikacijos](https://www.ogc.org/standard/gml/)

* [GML – pateikė Vikipedija](https://en.wikipedia.org/wiki/Geography_Markup_Language)


