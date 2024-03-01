{
  "date": "2020-03-16",
  "keywords": [
"STL tiedosto",
"Muoto",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi STL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata STL-tiedostoja.",
  "title": "STL-tiedostomuoto",
  "linktitle": "STL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-st-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on STL-tiedosto?

STL, lyhenne sanoista stereolitrografia, on vaihdettava tiedostomuoto, joka edustaa 3-ulotteista pintageometriaa. Tiedostomuotoa käytetään useilla aloilla, kuten nopeassa prototyyppien valmistuksessa, 3D-tulostuksessa ja tietokoneavusteisessa valmistuksessa. Se edustaa pintaa sarjana pieniä kolmioita, jotka tunnetaan faseteina, joissa jokaista puolta kuvataan kohtisuoralla suunnalla ja kolmella pisteellä, jotka edustavat kolmion huippuja. Sovellukset käyttävät saatuja tietoja määrittääkseen valmistajan rakentaman 3D-muodon poikkileikkauksen. STL-tiedostomuodossa ei ole saatavilla tietoja värin, tekstuurin tai muiden yleisten [CAD](/cad/)-mallin attribuuttien esittämisestä.

## Lyhyt historia ##

The development of STL file format dates back to 1987. 3D Systems on kehittänyt sen käytettäväksi kaupallisissa 3D-tulostimissa. STL-tiedostomuodon tarkistettua versiota, joka tunnetaan nimellä STL 2.0, ehdotettiin vuonna 2009 tiedostomuotopäivityksillä.

## Tiedostomuodon tiedot ##

STL-tiedosto edustaa pintageometriaa fasettien avulla. Fasetit määrittelevät 3D-objektin pinnan, ja ne tunnistetaan yksiselitteisesti yksikkönormaalilla, joka on kohtisuorassa kolmioon nähden, jonka pituus on 1,0, ja kolmella kärjellä. Jokaiselle taholle on tallennettu yhteensä 12 numeroa normaalina, ja jokainen kärkipiste on määritelty kolmella koordinaatilla. StL-tiedosto ei sisällä mittakaavatietoja; koordinaatit ovat mielivaltaisissa yksiköissä.

STL-tiedostomuodon määrityksiä voidaan tarkastella seuraavista kahdesta näkökulmasta.

### Facets Orientation ###

Fasetin suunta määräytyy yksikkönormaalin suunnan ja kärkien listausjärjestyksen mukaan. Fasettien suunta määritetään kahdella tavalla seuraavasti:

* Normaalin suunta on ulospäin

* Huippupisteet on listattu ulkopuolelta vastapäivään oikean käden sääntöä noudattaen.


### Vertex to the Vertex -sääntö ###

Tämän säännön mukaan jokaisella kolmiolla on kaksi kärkeä kunkin viereisen kolmion kanssa. Näin ollen yhden kolmion kärki ei voi olla toisen kolmion sivulla.

## Tiedostomuodot ##

STL on saatavana ASCII-muodossa sekä binäärimuodossa kompaktille tiedostomuodolle.

### STL ASCII -muoto ###

STL-tiedostomuodon ASCII-versio on kirjoitettu tavallisella ASCII-muodolla. Suuren koonsa vuoksi tiedostomuotoa ei kuitenkaan ole valittu suositeltavaksi käyttömuodoksi. ASCII STL -tiedoston syntaksi on seuraava:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
The bold face words represent keywords that should always be lowercase. Symbols in italics are variables which are to be replaced with user-specified values.  The numerical data in the **facet normal** and **vertex** lines are single precision floats, for example, 1.23456E+789. **Fasetin normaali**-koordinaatilla voi olla johtava miinusmerkki; **vertex**-koordinaatti ei välttämättä.

### STL-binaarimuoto ###

Binäärimuoto käyttää IEEE-kokonaislukua ja liukulukua. Tiedostomuoto esitetään seuraavasti:

|Kenttä|Tiedot|
---|---|
|Otsikko|80 merkkiä|
|Kolmioiden lukumäärä|4-tavuinen pieni endian etumerkitön kokonaisluku|
|Tiedot jokaiselle kolmiolle|12 32-bittistä liukulukua|

Tarkempi näkymä tiedostomuodosta on kuten alla.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Viitteet ##

* [STL-muoto](http://www.fabbers.com/tech/STL_Format)

* [STL - Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))


