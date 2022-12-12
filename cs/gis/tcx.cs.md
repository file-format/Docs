{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru TCX – soubor XML školícího centra",
  "description":"Další informace o formátu souboru TCX a rozhraních API, která mohou vytvářet a otevírat soubory TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Co je soubor TCX?

Soubor TCX (Training Center XML) je formát pro výměnu dat používaný ke sdílení dat mezi fitness zařízeními. Byl představen v roce 2008 s produktem Garmin's Training Center. Údaje o cvičení, jako je srdeční frekvence, kadence běhu, kadence na kole, kalorie a čas kola, jsou uloženy ve formátu [XML](/cs/web/xml/) v souboru TCX. Kromě toho jsou v souboru TCX také zahrnuty souhrnné údaje o tréninkové trase. Soubory TCX jsou podobné souborům [FIT](/cs/gis/fit/), které se vytvářejí pomocí sportovních nositelných zařízení Garmin.

## Formát souboru TCX – Další informace

Soubory TCX se ukládají na disk jako soubory XML s každým záznamem uloženým jako aktivita. Aktivita obsahuje všechna data tréninku, jako je čas, čas na kolo, Id, srdeční frekvence, intenzita, kadence a informace o trase, které obsahují dvojice pozic spolu s časovým razítkem pro tuto zeměpisnou šířku a délku podobnou [GPX] (/cs/gis/gpx/) soubory.

### Verze formátu souboru TCX

Existují dvě verze tohoto formátu s vlastními schématy XML hostovanými společností Garmin. Následuje několik z nich:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Datový protokol TCX

Rychlá verze formátu TCX XML je k dispozici na Github jako [TcxDataProtocol] (https://github.com/FitnessKit/TcxDataProtocol).

## Reference ##

* [XML školícího centra](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

