{
  "date" : "2019-10-11",
  "keywords" :[ "plik gml", "co to jest plik gml", "plik", "przykład gml", "rozszerzenie pliku gml", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML — format pliku języka znaczników geograficznych",
  "description":"Poznaj format pliku GML i interfejsy API, które mogą tworzyć i otwierać pliki GML.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik GML?

GML to skrót od Geography Markup Language, który jest oparty na specyfikacjach XML opracowanych przez Open Geospatial Consortium (OGC). Format służy do przechowywania funkcji danych geograficznych w celu wymiany między różnymi formatami plików. Służy jako język modelowania dla systemów geograficznych, a także jako otwarty format wymiany dla transakcji geograficznych w Internecie.

## Format pliku GML ##

Podobnie jak w przypadku większości gramatyk opartych na XML, gramatyka składa się z dwóch części — schematu opisującego dokument i dokumentu instancji zawierającego rzeczywiste dane. Dokument GML jest opisany za pomocą schematu GML. Pozwala to użytkownikom i programistom opisywać ogólne zestawy danych geograficznych, które zawierają punkty, linie i wielokąty. Korzystając ze schematów aplikacyjnych, użytkownicy mogą odwoływać się do dróg, autostrad i mostów zamiast do punktów, linii i wielokątów.

Warto zauważyć, że GML nie powinien być interpretowany jako reprezentacja danych przestrzennych na mapach. Reprezentacja treści GML jest inna niż cel, dla którego GML został stworzony. Krótko mówiąc, GML jest podobny do XML, ponieważ służy tylko do przechowywania treści przestrzennych, które mogą być używane przez aplikacje mapujące do celów wyświetlania.

### Tworzenie treści w GML ###

GML reprezentuje dane przestrzenne za pomocą funkcji, które są listą właściwości i geometrii. Właściwość ma nazwę, typ i opis wartości. Geometria składa się z podstawowych bloków konstrukcyjnych geometrii, takich jak:

* punkty
* linie
* Krzywe
* sufrakcje i
* wielokąty

Planuje się, że przyszłe wersje GML będą obsługiwać geometrię 3D, a także relacje topologiczne między elementami.

Kodowanie GML pozwala już na dość złożone funkcje. Cecha może na przykład składać się z innych cech. Pojedynczy obiekt, taki jak lotnisko, może zatem składać się z innych obiektów, takich jak drogi kołowania, pasy startowe, hangary i terminale lotnicze. Geometria obiektu geograficznego może również składać się z wielu elementów geometrii. Złożony geometrycznie element może zatem składać się z kombinacji typów geometrii, w tym punktów, ciągów linii i wielokątów.

### Przykłady ###

GML 1.0 i 2.0 kodują wielokąty, punkty i obiekty LineString w następujący sposób:

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

## Bibliografia ##

* [Specyfikacje GML](https://www.ogc.org/standard/gml/)
* [GML – z Wikipedii](https://en.wikipedia.org/wiki/Geography_Markup_Language)

