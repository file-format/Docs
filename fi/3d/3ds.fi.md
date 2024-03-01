{
  "date": "2019-10-11",
  "keywords": [
"3DS",
"tiedosto",
"muoto",
"tiedostotyyppi",
"laajennus",
"mikä on 3DS-tiedosto?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi 3DS-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda 3DS-tiedostoja.",
  "title": "3DS tiedostomuoto",
  "linktitle": "3DS",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3ds"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on 3DS-tiedosto?

Tiedosto, jonka laajennus on .3ds, edustaa Autodesk 3D Studion käyttämää 3D Sudio (DOS) mesh-tiedostomuotoa. Autodesk 3D Studio on ollut 3D-tiedostomuotomarkkinoilla 1990-luvulta lähtien ja on nyt kehittynyt 3D Studio MAX:ksi 3D-mallinnuksen, animaation ja renderöinnin parissa. 3DS-tiedosto sisältää tietoja kohtausten ja kuvien 3D-esitystä varten, ja se on yksi suosituimmista tiedostomuodoista 3D-tietojen tuonnissa ja viennissä. Se ottaa huomioon tiedot, kuten kameran sijainnit, verkkotiedot, valaistustiedot, näkymän konfiguraatiot, tasoitusryhmätiedot, bittikarttaviitteet ja attribuutit luodakseen pisteitä ja polygoneja näkymän renderöimiseksi.

## 3DS-tiedostomuoto – lisätietoja
Pohjimmiltaan 3DS on binääritiedostomuoto, ja se noudattaa ennalta määritettyä rakennetta tietojen tallentamiseksi ja hakemiseksi. Binääritiedostomuoto mahdollistaa 3DS-tiedostomuodon nopeammin pienemmän kuin tekstipohjaiset tiedostomuodot. 3DS-tiedoston sisällä olevat tiedot tallennetaan paloina.

### 3DS Chunk

Jokainen 3DS-tiedoston pala on tietolohko, joka sisältää tunnuksen, lohkon pituuden seuraavan lohkon sijaintia varten ja itse tiedot. Osatunnuksen avulla 3DS-tiedostomuodon lukijat voivat ohittaa lohkot, joita he eivät tunnista. Se auttaa myös muodon laajennettavuutta. Jokainen pala tallentaa tietoja, jotka liittyvät muotoihin, valaistukseen ja katselutietoihin, jotka yhdessä tekevät kohtauksen. Palat on järjestetty hierarkkiseen rakenteeseen 3DS-tiedostossa ja muistuttavat XML-dokumenttiobjektipuuta esityksessä.

**Chunk ID:** The first two bytes of a chunk represent a chunk identifier that lets the file reader decide whether to consider it during reading or skip i-fit.

**Osan pituus:** Osatunnusta seuraa 4 tavun kokonaisluku (pieni-endianissa), joka tarkoittaa osan pituutta. Tämä pituus sisältää myös datan pituuden, sen alilohkojen pituuden ja 6-tavun otsikon.

**Hyötykuorma:** Kappaleen pituutta seuraavat lohkon todelliset datatavut, joita seuraavat sen alipalat samassa hierarkkisessa rakenteessa, jota voidaan laajentaa useille tasoille.

### Palan rakenne

Yksinkertaisen kappaleen hierarkkinen rakenne on seuraavanlainen:

**pala**

|aloitus|loppu|koko|nimi
--- | --- | --- | ---
|0|1|2|Osatunnus
|2|5|4|Seuraava osa

Palloille on asetettu hierarkia, joka tunnistetaan sen tunnuksella. 3ds-tiedoston ensisijainen osatunnus on 4D4Dh. Tämä on aina tiedoston ensimmäinen osa. Ensisijaisessa osassa ovat pääpalat.

**Pääpalat**

|id|Kuvaus
--- | ---
|3D3D|Objektiverkkotietojen alku.
|B000|Avainkehystietojen aloitus.

ID-lohkon jälkeen oleva Next Chunk -osoitin osoittaa seuraavaan pääosaan.
Heti pääosan jälkeen on toinen pala. Tämä voi olla mikä tahansa muun tyyppinen pala, joka on sallittu sen pääosien laajuudessa.
For the Mesh description (3D3D) they could be any multiples of.

**3D3D:n osat - Mesh Block**


|id|Kuvaus
--- | ---
|1100|tuntematon
|1200|Taustaväri.
|1201|tuntematon
|1300|tuntematon
|1400|tuntematon
|1420|tuntematon
|1450|tuntematon
|1500|tuntematon
|2100|Ambient Color Block
|2200|sumu?
|2201|sumu?
|2210|sumu?
|2300|tuntematon
|3000|tuntematon
|4000|Objektilohko
|7001|tuntematon
|AFFF|tuntematon

**4000:n osalohkot - Objektin kuvauslohko**
Subchunk 4000:n ensimmäinen kohde on objektien nimen ASCIIZ-merkkijono.
Muista, että esine voi olla verkko, valo tai kamera.

|id|Kuvaus
--- | ---
|4010|tuntematon
|4012|varjo?
|4100|Kolmikulmainen monikulmioobjekti
|4600|Kevyt
|4700|Kamera

## Viitteet

* [Geometriatiedostomuodot – Autodesk](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)

* [3DS - Wikipedia](https://en.wikipedia.org/wiki/.3ds)


