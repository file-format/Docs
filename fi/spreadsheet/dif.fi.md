{
  "date": "2019-12-10",
  "keywords": [
"DIF",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Tiedonsiirtotiedosto",
"Laskentataulukko"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Tiedostomuoto-opas tietää, mikä on DIF-tiedostopääte ja API:t, jotka voivat luoda ja avata DIF-tiedostoja.",
  "title": "DIF - Data Interchange File Format",
  "linktitle": "DIF",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-di-fif"
}
},
  "lastmod": "2019-12-10"
}

## Mikä on DIF-tiedosto?

DIF on lyhenne sanoista Data Interchange Format, jota käytetään tuomaan/viemään laskentataulukkotietoja eri sovellusten välillä. Näitä ovat Microsoft Excel, OpenOffice Calc, StarCalc ja monet muut. Se tallentaa tiedot yhteen laskentataulukkoon, mikä on tämän tiedostomuodon ainoa rajoitus.

## DIF-tiedostomuodon ## lyhyt historia

DIF-tiedostomuodon kehitti Software Arts, Inc. 1980-luvun alussa. DIF:n tiedostomuotomääritykset sisällytettiin VisiCalciin, joka oli ensimmäinen henkilökohtaisten tietokoneiden taulukkolaskentaohjelma. Nämä tekniset tiedot olivat tekijänoikeudella suojattuja vuonna 1981, ja ne olivat Software Arts Products Corp.:n rekisteröity tavaramerkki.

## DIF-tiedostomuoto ##

DIF tallentaa laskentataulukon sisällön ASCII-tekstitiedostoon, jonka avulla sitä voi tarkastella ja muokata tekstieditorilla. Formaatti omistaa paikkansa tietojen serialisointimuotojen luettelossa tiedonvaihdon ominaisuuksiensa vuoksi. DIF-tiedosto koostuu kahdesta osasta; otsikko ja tiedot.

Kaikkea DIF:ssä edustaa 2- tai 3-rivinen pala. Otsikoihin tulee 3-rivinen pala; tiedot, 2.

* Otsikkolohkot alkavat tekstitunnisteella, jossa on vain isoja kirjaimia, vain aakkosmerkkejä ja alle 32 kirjainta. Seuraavan rivin on oltava numeropari ja kolmannen rivin on oltava lainausmerkkijono.

* Tietopalat alkavat numeroparilla ja seuraava rivi on lainausmerkkijono tai avainsana.


### Arvot ###

Arvo sisältää kaksi riviä, joista ensimmäinen on numeropari ja toinen joko merkkijono tai avainsana. Parin ensimmäinen numero ilmaisee tyypin:

* −1 – directive type, the second number is ignored, the following line is one of these keywords:
** BOT – rivin alku (rivin alku)
** EOD – tietojen loppu
* 0 – numeric type, value is the second number, the following line is one of these keywords:
** V – voimassa
** NA – ei saatavilla
** ERROR – virhe
** TRUE – todellinen boolen arvo
** FALSE – väärä looginen arvo
* 1 – merkkijonotyyppi, toinen numero ohitetaan, seuraava rivi on merkkijono lainausmerkeissä


### DIF-otsikon osa ###

DIF-tiedoston otsikkolohko koostuu tunnisterivistä, jota seuraa kaksi arvon riviä. Otsikkopalojen numeeriset arvot käyttävät vain tyhjää merkkijonoa kelvollisuusavainsanojen sijaan. Näiden otsikkopalojen yksityiskohdat ovat seuraavat.

* TABLE - versiota seuraa numeerinen arvo, arvon käytöstä poistettu toinen rivi sisältää generaattorikommentin

* VEKTORIT - sarakkeiden lukumäärä seuraa numeerisena arvona

* TUPLES - rivien lukumäärä seuraa numeerisena arvona

* DATA - vale-0-numeerisen arvon jälkeen taulukon tiedot seuraavat, jokainen rivi ennen BOT-arvoa, koko taulukko päättyy EOD-arvoon


### DIF-esimerkki ###

Seuraava esimerkki näyttää yksinkertaisen laskentataulukon sisällön ja sitä vastaavan DIF-esityksen.


|Nimi|Ikä
---|---|
|Bob|34
|Arkki|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Viitteet ##

* [ DIF - Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)


