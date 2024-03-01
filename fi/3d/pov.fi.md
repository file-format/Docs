
{
  "date": "2023-01-05",
  "keywords": [
"pov-tiedosto",
"pov-tiedostomuoto",
"mikä on pov-tiedosto",
"tiedosto",
"pov esimerkki",
"pov tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Opi POV-tiedostomuodoista ja sovellusliittymistä, jotka voivat avata ja luoda POV-tiedostoja.",
  "title": "POV - Näön pysyvyys -tiedosto",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-fiv"
}
},
  "lastmod": "2023-01-05"
}

## Mikä on POV-tiedosto?

POV-tiedosto on pelkkä tekstitiedosto, joka sisältää ohjeet POV-Ray-säteenseurantaohjelmistolle. Nämä ohjeet on kirjoitettu erityisellä skriptikielellä, joka on ominaista POV-Raylle. Se määrittää renderoitavan kohtauksen, mukaan lukien 3D-objektit, materiaalit, valaistuksen ja muut ominaisuudet, jotka määrittävät kohtauksen ulkonäön. POV-tiedostot käyttävät erityistä skriptikieltä, joka on ominaista POV-Raylle ja jota voidaan käyttää monimutkaisten ja yksityiskohtaisten 3D-kohtausten luomiseen. POV-tiedoston tiedostotunniste on yleensä .pov tai .povray. Kun avaat POV-tiedoston POV-Rayssa, ohjelmisto lukee tiedoston ohjeet ja luo niiden avulla näkymästä renderoidun kuvan.

Taiteilijat ja suunnittelijat käyttävät usein .pov-tiedostoja luodakseen 3D-grafiikkaa ja animaatioita erilaisiin sovelluksiin, kuten elokuviin, televisioon, videopeleihin ja markkinointimateriaaleihin.

## POV-tiedostomuoto

**.pov-tiedosto** alkaa yleensä sarjalla **#include**-lauseita, joita käytetään sisältämään ennalta määritettyjen värien, pintakuvioiden ja muiden resurssien kirjastot, joita voidaan käyttää kohtauksessa. Sitten tiedosto määrittää kohteen objektit, materiaalit ja muut ominaisuudet käyttämällä lohkoja. On olemassa monia muun tyyppisiä objekteja, materiaaleja ja muita ominaisuuksia, jotka voit määrittää .pov-tiedostossa, ja voit luoda monimutkaisempia ja yksityiskohtaisempia kohtauksia silmukoiden ja ehdollisten lausekkeiden avulla.

## Ohjelmistosovellukset POV:lle

POV-Ray ray Tracing -ohjelmisto käyttää .pov-tiedostomuotoa, joten ensisijainen sovellus .pov-tiedostojen avaamiseen on itse POV-Ray-ohjelmisto. Voit ladata POV-Rayn uusimman version viralliselta verkkosivustolta https://www.povray.org/.

POV-Rayn lisäksi on useita muita sovelluksia, jotka voivat avata ja muokata .pov-tiedostoja, mukaan lukien:

- BRL-CAD: avoimen lähdekoodin 3D-mallinnusohjelmisto, joka voi tuoda ja viedä .pov-tiedostoja
- MeshLab: 3D-verkkokäsittelyohjelmisto, joka voi tuoda ja viedä .pov-tiedostoja
- Blender: suosittu avoimen lähdekoodin 3D-grafiikkaohjelmisto, joka voi tuoda ja viedä .pov-tiedostoja

Saattaa olla myös muita ohjelmistosovelluksia, jotka voivat avata .pov-tiedostoja, joten sinun kannattaa kokeilla tiedostojen katselu- tai muunnostyökalua, jos et pysty avaamaan .pov-tiedostoa yllä olevilla sovelluksilla.

## POV-esimerkki

Esimerkiksi tässä on esimerkki .pov-tiedostosta, joka määrittää kohtauksen yhdellä sinisellä sylinterillä:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Tässä esimerkissä kameralohko määrittää kameran sijainnin ja suunnan kohtauksessa, light_source -lohko ilmoittaa valonlähteen ja määrittää sen sijainnin ja värin, ja sylinteri -lohko ilmoittaa sylinteriobjektin ja määrittää sen päätepisteet, säde ja materiaaliominaisuudet. Kun avaat tämän .pov-tiedoston POV-Ray-ohjelmistossa, se hahmontaa kuvan yhdestä sinisestä sylinteristä.

## Viitteet
 * [POV-Ray – Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Dokumentaatio POV-Ray-verkkosivusto](http://www.povray.org/documentation/)

