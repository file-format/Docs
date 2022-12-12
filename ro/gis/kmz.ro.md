{
  "date" : "2019-10-11",
  "keywords" :[ "fișier kmz", "ce este un fișier kmz", "fișier", "exemplu kmz", "extensie fișier kmz", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - Format fișier comprimat KML",
  "description":"Aflați despre formatul de fișier KMZ și despre API-urile care pot crea și deschide fișiere KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier KMZ?

Fișierul KMZ (KML Zipped) este o reprezentare a fișierului arhivat [KML](/ro/gis/kml/) care conține informații geospațiale care pot fi vizualizate în aplicații GIS precum Google Earth. Informațiile despre marcatorii de locație sunt reprezentate în fișier ca latitudine și longitudine împreună cu un nume personalizat. Fișierul KMZ ambalat unic poate fi partajat cu ușurință cu alți utilizatori. Fișierele KMZ pot include și date model 3D pentru reprezentarea geografică a modelului. Un fișier KMZ poate fi deschis în Google Maps salvând fișierul într-o locație online și apoi tastând adresa URL în caseta de căutare Google Maps.

## Structura fișierului ##

Conținutul unui fișier MKZ constă dintr-un fișier KML principal și zero sau mai multe fișiere asociate. Poate fi extras folosind utilitarul standard de decompresie precum WinZIP. Formatul de fișier KMZ este, de asemenea, comprimat într-o arhivă cu un raport de compresie de 10:1. Puteți exporta date din Google Earth, cum ar fi aplicațiile, direct în formatul de fișier KMZ. Fișierul KML principal se numește **doc.kml**. În timp ce împachetați un fișier KMZ, la acesta pot fi adăugate mai multe fișiere KML, dar acest lucru nu va fi de niciun beneficiu, deoarece Google Earth caută primul fișier KML când deschide fișierul KMZ și îl citește. Ignoră orice alte fișiere KML găsite în arhivă. Pentru a fi siguri că fișierul KML dorit este citit de Google Earth, se recomandă plasarea unui singur fișier KML în interiorul fișierului KMZ.

Imaginile, modelele, texturile, fișierele de sunet și alte resurse la care se face referire în fișierul doc.kml sunt plasate într-un alt subfolder în interiorul folderului principal. Acest lucru poate implica o oarecare complexitate, de asemenea, în funcție de numărul de fișiere suportate. Legăturile către aceste resurse constitutive pot fi de referință relativ sau prin referință absolută.

### Referințe relative ###

Când resursele sunt plasate alături de doc.kml principal într-un sub-folder din folderul principal, referința relativă poate indica aceste fișiere de suport, așa cum se arată în exemplul următor (doar pentru pictogramă).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Referințe absolute ###

Resursele pot fi referite absolut, de asemenea. Referințele absolute conțin adresa URL completă a fișierului legat. Când fișierele sunt postate pe un server central, referința absolută asigură faptul că acestea rămân fără ambiguitate în comparație cu referirea relativă. Fișierul local nu este recomandat să fie referit în mod absolut, deoarece aceste legături se vor întrerupe atunci când fișierele sunt mutate într-un sistem nou. Un exemplu de referință absolută este următorul:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Vezi si ##

* [GeoJSON](/ro/gis/geojson/)

## Referințe ##

* [Fișiere Google Earth și KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

