{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "soubor", "rozšíření", "formát souboru", "Poloha GPS", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - GPS Location File Format",
  "description":"Další informace o formátu souboru LOC a rozhraních API, která mohou vytvářet a otevírat soubory LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Co je soubor LOC?

Soubor s příponou .loc je soubor polohy GPS, který obsahuje geoprostorové polohy jako trasové body. Trasový bod je dvojice hodnot zeměpisné šířky a délky, která odkazuje na místo používané aplikacemi geografického informačního systému (GIS). Mapovací programy GPS, jako je DeLorme Topo, používají soubory LOC ke čtení a zobrazování informací obsažených v těchto souborech LOC jako volitelné vrstvy koncovými uživateli. Ty navíc slouží k výměně GPS dat mezi aplikacemi. Soubory LOC lze otevřít pomocí aplikací, jako je [TopoGrafix EasyGPS](https://www.easygps.com/), které zobrazují obsah takových souborů jako vrstvy a data vykreslená na mapě v příslušné geolokaci.

## Formát souboru LOC – Další informace

Soubory LOC jsou podobné souborům [GPX](/cs/gis/gpx/), ale jsou uloženy v jiném formátu. Ty se ukládají jako soubory [XML](/cs/web/xml/), kde je obsah trasových bodů a související informace obsaženy ve strukturovaných značkách. Protože XML je zobecněný jazyk pro výměnu dat mezi různými aplikacemi, usnadňuje to výměnu dat LOC s jinými aplikacemi.

## Formát souboru LOC – příklad

Následuje záhlaví a text jednoho navigačního bodu ze souboru LOC. Jak je vidět, informace záhlaví obsahuje zdroj umístění dat. Trasový bod obsahuje informace, jako je „ID“ a související data obsahu spojená s trasovým bodem. A konečně, trasový bod je sbírka hodnot zeměpisné šířky a délky a text spojený s tímto konkrétním trasovým bodem.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Reference

* [TopGraphic EasyGPS](https://www.easygps.com/)

