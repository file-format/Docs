{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "fișier", "extensie", "format fișier", "Locație GPS", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - Format fișier de locație GPS",
  "description":"Aflați despre formatul de fișier LOC și despre API-urile care pot crea și deschide fișiere LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Ce este un fișier LOC?

Un fișier cu extensia .loc este un fișier de locație GPS care conține locații geospațiale ca puncte de referință. Un punct de referință este o pereche de valori Latitudine-Longitudine care se referă la o locație utilizată de aplicațiile Sistemului de Informații Geografice (GIS). Programele de cartografiere GPS, cum ar fi DeLorme Topo, folosesc fișiere LOC pentru a citi și afișa informațiile conținute de aceste fișiere LOC ca straturi selectabile de către utilizatorii finali. În plus, acestea sunt folosite pentru a face schimb de date GPS între aplicații. Fișierele LOC pot fi deschise folosind aplicații precum [TopoGrafix EasyGPS](https://www.easygps.com/) care afișează conținutul unor astfel de fișiere, cum ar fi straturi și date trasate pe hartă la locația geografică respectivă.

## Format de fișier LOC - Mai multe informații

Fișierele LOC au asemănări cu fișierele [GPX](/ro/gis/gpx/), dar sunt salvate în format diferit. Acestea sunt salvate ca fișiere [XML](/ro/web/xml/) în care conținutul punctelor de referință și informațiile asociate sunt conținute în etichete structurate. Deoarece XML este un limbaj generalizat pentru schimbul de date între diferite aplicații, acest lucru facilitează schimbul de date LOC cu alte aplicații.

## Format de fișier LOC - Exemplu

Urmează antetul și textul unui punct de referință dintr-un fișier LOC. După cum se poate vedea, informațiile din antet conțin sursa locației datelor. Punctul de trecere conține informații precum „ID” și datele de conținut asociate asociate cu punctul de trecere. În cele din urmă, punctul de referință este o colecție de valori de latitudine și longitudine și textul asociat cu acest punct de referință.

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

## Referințe

* [TopGraphic EasyGPS](https://www.easygps.com/)

