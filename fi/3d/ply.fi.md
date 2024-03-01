{
  "date": "2019-12-12",
  "keywords": [
"PLY",
"tiedosto",
"laajennus",
"muoto",
"3D tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi PLY-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PLY-tiedostoja.",
  "title": "PLY - Polygon 3D -tiedostomuoto",
  "linktitle": "PLY",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-pl-fiy"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on PLY-tiedosto?

PLY, Polygon File Format, edustaa 3D-tiedostomuotoa, joka tallentaa graafisia objekteja, jotka on kuvattu kokoelmana polygoneja. Tämän tiedostomuodon tarkoituksena oli luoda yksinkertainen ja helppo tiedostotyyppi, joka on tarpeeksi yleinen ollakseen hyödyllinen useille malleille. PLY-tiedostomuoto tulee sekä ASCII- että binaarimuodossa kompaktia tallennusta ja nopeaa tallennusta ja latausta varten. Tiedostomuotoa käyttävät eri sovellukset, jotka tukevat 3D-tiedostojen lukemista.

PLY-muodossa olevat objektit kuvataan joukolla huippuja, kasvoja ja muita elementtejä sekä ominaisuuksia, kuten väri ja normaali suunta, jotka voidaan liittää näihin elementteihin. Muita ominaisuuksia, jotka voidaan myös tallentaa objektiin, ovat:

* Pintanormaalit

* tekstuurin koordinaatit

* läpinäkyvyys

* alueen tietojen luotettavuus

* ominaisuudet monikulmion etu- ja takapuolelle


PLY-muodon edustama kohde voi olla tulosta useista lähteistä, kuten käsin digitoiduista objekteista, monikulmioobjekteista mallinnussovelluksista, etäisyystiedoista, kolmioista marssikuutioista, pintatiedoista ja radiositeettimalleista.

## Lyhyt historia

PLY-formaatin kehittivät 1990-luvulla Greg Turk ja muut Stanfordin grafiikkalaboratoriossa, ja siksi se tunnetaan myös nimellä Stanford Triangle Format. Sen jälkeen tiedostomuodossa on versio 1.0, eikä siihen ole tehty muita muutoksia.

## PLY-tiedostomuoto

Yksinkertainen PLY-objekti koostuu elementtien kokoelmasta objektin esittämiseksi. Se koostuu listasta (x,y,z) kärjen kolmiosista ja listasta kasvot, jotka ovat itse asiassa indeksejä kärkiluetteloon. Vertices ja pinnat ovat kaksi esimerkkiä elementeistä, ja suurin osa PLY-tiedostosta koostuu näistä kahdesta elementistä. Uusia ominaisuuksia voidaan myös luoda ja liittää objektin elementteihin, mutta ne tulee lisätä siten, että vanhat ohjelmat eivät katkea näitä uusia ominaisuuksia vastaan. Tällaiset ominaisuudet voidaan hylätä myös lukemalla sovelluksia. Lisäksi tällä elementillä voidaan luoda uusia elementtejä ja määrittää ominaisuuksia.

### Tiedostorakenne

PLY-tiedostomuodon tiedostorakenne on seuraava:

| Kenttä
---|
|Tiedoston otsikko
|Vertex List
|Kasvoluettelo
|Luettelo muista elementeistä

#### Esimerkkirakenne

Käytämme seuraavaa esimerkkiä seuraavassa keskustelussamme PLY-tiedostomuodon eri osien osalta.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Tiedoston otsikko

PLY-tiedostomuodon otsikko koostuu ASCII-tekstistä sekä ASCII- että binäärimuodolle. Otsikko-osion alku ja loppu tunnistetaan kerros- ja loppuotsikkoavainsanoilla. Otsikon alussa on taikasana ply, jota lukijat käyttävät PLY-tiedostomuodon tunnistamiseen. Seuraava rivi näyttää tämän tiedoston versionumeron. PLY-tiedostomuodossa olevat kommentit alkavat kommenttiavainsanalla jokaisen kommenttirivin alussa.

#### Elementtiavainsana

Elementtiavainsana kertoo sitten, mitä tiedoston sisällä on. Sitä seuraavat sen tietyn elementtityypin ominaisuudet, joissa jokaisella ominaisuudella on ominaisuustyyppi ja järjestys määritettynä alla olevan kuvan mukaisesti:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Tässä nimenomaisessa esimerkissä tietyllä kärkielementillä on 3 float-tyyppistä ominaisuutta, joiden järjestys on määritetty.

#### Tietotyyppien tyypit

Omaisuudella voi olla kahdenlaisia tietotyyppejä.

Skalaari: Skalaaritietotyypit ovat seuraavat:

|#Nimi|#Tyyppi|#Tavujen määrä
|merkki|hahmo|1
|uchar|allekirjoittamaton merkki|1
|lyhyt|lyhyt kokonaisluku|2
|ushort|signed lyhyt kokonaisluku|2
|int|Kokonaisluku|4
|uint|signaamaton kokonaisluku|4
|kelluke|yksitarkkuuskelluke|4
|kaksois|kaksoistarkkuuskelluke|8

Lista: Ominaisuuden määrittelyissä on erityinen muoto, joka käyttää luettelotietotyyppiä. Esimerkki tästä on yllä olevasta kuutiotiedostosta:

`ominaisuusluettelo uchar int vertex_index`

Tämä tarkoittaa, että ominaisuus vertex_index sisältää ensin etumerkittömän merkin, joka kertoo kuinka monta indeksiä ominaisuus sisältää, ja sen jälkeen luettelon, joka sisältää näin monta kokonaislukua. Jokainen tämän muuttuvan pituuden luettelon kokonaisluku on indeksi kärkeen.

## Viitteet ##

* [PLY-tiedostomuoto](http://paulbourke.net/dataformats/ply/)

* [PLY - Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))


