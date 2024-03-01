{
  "date": "2019-10-11",
  "keywords": [
"obj tiedosto",
"obj tiedostomuoto",
"mikä on obj-tiedosto",
"tiedosto",
"obj esimerkki",
"obj tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBJ-tiedostomuoto",
  "description": "Opi OBJ-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda OBJ-tiedostoja.",
  "linktitle": "OBJ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ob-fij"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on OBJ-tiedosto?

Wavefrontin Advanced Visualizer -sovellus käyttää **OBJ**-tiedostoja geometristen objektien määrittämiseen ja tallentamiseen. Geometristen tietojen siirtäminen taaksepäin ja eteenpäin on mahdollista OBJ-tiedostojen kautta. OBJ-muoto tukee sekä monikulmion geometriaa, kuten pisteitä, viivoja, pintakuvioita, pintoja ja vapaamuotoista geometriaa (käyrät ja pinnat). Tämä muoto ei tue animaatioita tai valoon ja kohtausten sijaintiin liittyviä tietoja.

OBJ-tiedosto on yleensä CAD:n (Computer Aided Design) luoman 3D-mallinnusprosessin lopputuote. Oletusjärjestys kärkipisteiden tallentamiseen on vastapäivään välttäen kasvonormaalien nimenomaista ilmoitusta. Vaikka OBJ-tiedostot ilmoittavat mittakaavatiedot kommenttirivillä, OBJ-koordinaateille ei ole ilmoitettu yksikköjä.

## 3D OBJ -muodon historia

Wavefront Technologies created OBJ file format for its Advanced Visualizer application to store geometric objects and 3D data. Its version 2.11 is superseded by a newly documented version 3. Tiedostomuoto on avoin, ja muut toimittajat ovat ottaneet sen käyttöön 3D-grafiikkasovelluksessaan. Wavefront Technologies piti tämän tiedostomuodon avoimen lähdekoodin ja neutraalina.

## OBJ-tiedostomuoto

3D-objekteissa pintageometrian koodaus on haastavaa työtä, jonka OBJ-tiedostomuoto suoritti erittäin hyvin. Tämä muoto on varsin monipuolinen, koska se tarjoaa useita vaihtoehtoja pintageometrian koodaamiseen. Seuraavassa on kolme sallittua muotoa, joilla on omat etunsa ja puutteensa:

### Tessellaatio monikulmiopinnoilla

OBJ-tiedostomuoto helpottaa 3D-mallin pinnan tessellointia käyttämällä yksinkertaisia tai monimutkaisia geometrisia muotoja. Mallin pintageometriakoodausta varten tiedosto tallentaa kunkin polygonin pisteet ja normaalit. Vaikka tessellaatio lisää mallin karkeutta, on kuitenkin välttämätöntä löytää oikea tasapaino tiedoston koon ja tulostuslaadun välillä.

### Vapaamuotoinen käyrä

OBJ-tiedostomuoto sallii käyttäjän määrittelemien vapaamuotoisten pintakäyrien määrittää mallin pintageometrian. Koska vapaamuotoiset käyrät ovat monimutkaisempia kuin monikulmiopinnat, koska kaarevat viivat voidaan määrittää parhaiten vapaamuotoisilla käyrillä, jos matemaattisia parametreja on vähän. Siksi vapaamuotoiset käyrät luovat korkealaatuisen koodauksen minkä tahansa 3D-mallin tiedostokokoa laajentamatta, koska dataa on vähemmän kuin monikulmion tessellaatioita.

### Vapaamuotoiset pinnat

OBJ-tiedostomuoto määrittää myös pintageometrian laatoituksen vapaamuotoisilla pintalapuilla. Tällaiset vapaamuotoiset pintapaikat (NURBS) sopivat hyvin pinnoille, joilla ei ole jäykkiä radiaalimittoja, kuten kuorma-auton runko, helikopterin siivet tai veneen runko. Vapaamuotoisten pintojen käyttö on erittäin edullista, koska ne ovat tarkempia pitämään tiedostokoot pienempänä suuremmalla tarkkuudella. Nämä pinnat ovat olennainen osa ilmailu- ja autoteollisuutta, jossa alhainen tarkkuus on anteeksiantamatonta.

Seuraavat avainsanat on järjestetty tietotyypin mukaan pinnan geometrian määrittelemiseksi.


|Elementit|Vapaamuotoiset käyrän/pinnan runkolausekkeet|Vapaan muodon käyrän/pinnan määritteet
---|---|---|
|p|Piste|parm|Parametriarvot|deg|aste
|l|Line|trim|Ulkoinen trimmaussilmukka|bmat|Perusmatriisi
|f|Kasvo|reikä|Sisäinen leikkaussilmukka|askel|Askelkoko
|curv|Curve|scrv|Erikoiskäyrä|cstype|Kaari tai pintatyyppi
|käyrä2|2D-käyrä|sp|Erikoispiste|**Liitännät ja pintojen ryhmittely**
|surf|Pinta|end|Lopeta lauseke|con|connect
|**Näytä/renderöi attribuutit**|g|Ryhmän nimi
|viiste|Viiston interpolointi|shadow_obj|Varjojen luominen|s|Tasoitusryhmä
|lod|Tarkkuustaso|trace_obj|Ray tracing|mg|Yhdistävä ryhmä
|d_interp|Poista interpolointi|ctech|Käyrän approksimaatiotekniikka|o|Objektin nimi
|c_interp|Värien interpolointi|stech|Pintojen approksimaatiotekniikka|
|usemtl|Materiaalin nimi|mtllib|Materiaalikirjasto|
|**Geometriset kärjet**|
|v|Geometriset kärjet|vn|Vertex-normaalit|
|vt|Tektuuripisteet|vp|Parametriavaruuspisteet|

### Väri ja rakenne

OBJ-tiedoston avulla väri- ja pintakuviotiedot voidaan tallentaa siihen liittyvään tiedostomuotoon, jota kutsutaan materiaalimallikirjastoksi (MTL). Moniväriset geometriset mallit renderöidään käyttämällä näitä kahta tiedostoa yhdessä. MTL-tiedostot ovat ASCII-pohjaisia ja helpottavat tietokoneiden renderöintiä kuvaamalla pinnan valoa heijastavia ominaisuuksia käyttämällä Phong-heijastuksen mallia. Useat ohjelmistotoimittajat ovat omaksuneet standardin, jotka hyödyntävät sitä materiaalien vaihdossa. MTL-muoto on hieman vanhentunut, koska se ei tue uusimpia teknologioita, kuten peili- ja parallaksikarttoja.

## Viitteet

* [Wavefront .obj-tiedosto](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


