{
   "date":"2023-11-09",
   "keywords":[
"eläintarha",
"eläintarhan tiedosto",
"zoopakattu tiedosto",
"kuinka avata eläintarhatiedosto",
"tiedosto",
"zoo tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"ZOO File - Mikä on .zoo-tiedosto ja kuinka avata se?",
   "description":"Opi ZOO-pakatuista tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata ZOO-tiedostoja.",
   "linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo-fi",
         "parent":"compression"
}
},
   "lastmod":"2023-11-09"
}

## Mikä on ZOO-tiedosto?

.zoo-tiedosto on arkistomuoto, jota käytetään tiedostojen ja hakemistojen pakkaamiseen ja tallentamiseen. on samanlainen kuin muut arkistomuodot, kuten .zip, .tar ja .rar. .zoo-muoto oli suosittu tietojenkäsittelyn alkuaikoina, mutta siitä on tullut vähemmän yleinen viime vuosina. Sen kehitti alun perin **Rahul Dhesi**, ja sitä käytettiin pääasiassa Unix- ja DOS-järjestelmissä.

.zoo-tiedosto sisältää yleensä yhden tai useamman tiedoston ja hakemiston, jotka on pakattu ja arkistoitu yhdeksi tiedostoksi. Voit luoda ja purkaa .zoo-tiedostoja käyttämällä erilaisia ohjelmistotyökaluja, jotka tukevat tätä muotoa.

ZOO-arkistoilla on ainutlaatuinen ominaisuus, jonka avulla ne voivat tallentaa useita versioita samasta tiedostosta edellyttäen, että jokaista versiota on muokattu eri päivämääränä. Tämä tarkoittaa, että ZOO-käyttäjät voivat tallentaa ja käyttää tiedoston aikaisempia iteraatioita suoraan ZOO-arkistosta. Tämän ominaisuuden avulla käyttäjät voivat palata tiedoston aikaisempaan versioon tai verrata vanhempaa versiota uudempaan, mikä tarjoaa kätevän tavan hallita tiedostoversioita ja muutoksia ajan myötä.

## ZOO-tiedostojen yleiset toiminnot

Tässä on joitain yleisiä .zoo-tiedostoihin liittyviä toimintoja:

1.  **.zoo-tiedoston luominen:** Voit luoda .zoo-tiedoston komentorivityökalulla, kuten zoo. Esimerkiksi seuraava komento luo `.zoo`-arkiston hakemistosta:
    
`zoo a -c arkisto.eläintarhahakemisto/`
    
Tässä komennossa a tarkoittaa add, -c määrittää pakkauksen ja archive.zoo on tulosarkiston nimi.
    
2.  **Tiedostojen purkaminen .zoo-tiedostosta:** Voit purkaa .zoo-arkiston sisällön käyttämällä seuraavaa komentoa:
    
`eläintarha ja arkisto.eläintarha`
    
Tämä komento purkaa tiedostot archive.zoo-tiedostosta.
    
3.  **.zoo-tiedoston sisällön luettelointi:** Voit luetella .zoo-arkiston sisällön purkamatta sitä käyttämällä l-vaihtoehtoa:
    
    
`zoo l archive.zoo`

## Kuinka avata ZOO -tiedosto?

Ohjelmat, jotka avaavat ZOO-tiedostoja, sisältävät

- **zoo** (ilmainen) (Windows, Linux)

## Viitteet
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
