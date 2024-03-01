{
  "date": "2021-06-16",
  "keywords": [
"LZO",
"Pakattu",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Lempel-Ziv-Oberhume"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LZO tiedostomuoto",
  "description": "Opi LZO-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LZO-tiedostoja.",
  "linktitle": "LZO",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-fio"
}
},
  "lastmod": "2021-06-16"
}

## Mikä on LZO-tiedosto? ##

.lzo-tunnisteella varustettu tiedosto on yhdistetty tiedostojen arkistointiominaisuuksiin, jotka voivat pienentää pakatun tiedoston kaikkien tiedostojen kokoa. Kaikki pakatut tiedostot voivat sisältää yhdestä tai useammasta tiedostosta tai jopa sideaineryhmistä useita erityyppisiä ja -kokoisia tiedostoja. Pakatun tiedoston koko on pienempi verrattuna kaikkien LZO-pakattuun tiedostoon tallennettujen tiedostojen ja kansioiden yhteiskokoon. Kaikki LZO-pakatut tiedostot tallennetaan LZO-muodossa ja ne suoritetaan erityisesti LZOP-tiedostojen pakkaus- ja purkuohjelmiston pakkausominaisuuksilla. Kaikki pakkausmääritykset on yhdistetty tähän tiedostojen pakkaus- ja purkuohjelmaan, joka on peräisin Lempel-Ziv-Oberhume-tiedostojen pakkauskirjastosta. Nopeampi purkunopeus ja kehittyneet pakkaussuhteet yhdistetään myös näihin LZO-tiedostoihin.

## LZO-määritys ##

Markus Franz Xaver Johannes Oberhumer developed the original "lzop" algorithm, based on earlier algorithms by Abraham Lempel and Jacob Ziv, in 1996. Tämä kirjasto toteuttaa useita algoritmeja, joilla on seuraavat ominaisuudet:

* Nopeampi pakkaus kuin DEFLATE

* Nopea dekompressio

* Pakkauksen aikana tarvittavat lisäpuskurit (8kt tai 64kt pakkaustasosta riippuen)

* Lähde- ja kohdepuskurit ovat kaikki pakkauksen purkamiseen tarvittava muisti

* Tarjoaa sekä pakkaussuhteen että pakkausnopeuden hallinnan


Lohkojen pakkausalgoritmina LZO suorittaa päällekkäistä pakkausta sekä paikan päällä tapahtuvaa purkamista. Päällekkäisen pakkauksen saavuttamiseksi sekä pakkauksen että purkamisen lohkokoon on oltava sama. LZO-pakkausalgoritmi jakaa syötetiedot osumiin (liukuva sanakirja) ja kirjaimeen, jotka eivät täsmää, jolloin saadaan hyviä tuloksia erittäin redundanttisilla tiedoilla ja hyväksyttäviä tuloksia ei-pakkaamattomilla tiedoilla, mikä lisää vain pakkaamatonta dataa 1/64:llä alkuperäisestä. koko.

## Ongelmia LZO-tiedoston avaamisessa ##

Seuraavassa on muutamia ongelmia, jotka voivat aiheuttaa LZO-tiedostomuodon huonoa toimintaa:
  
* Tiedosto saattaa olla vioittunut. Voit ratkaista tämän ongelman lataamalla tiedoston uudelleen tai pyytämällä lähettäjää lähettämään tiedoston uudelleen
* Toinen syy on tartunnan saanut tiedosto, tässä tapauksessa skannaa tiedosto oikein
* Väärät linkit LZO-tiedostoon
  *	 Removal of the description of the LZO 
* Ei tarpeeksi laitteistoresursseja
* Laitteen vanhentuneet ajurit
  
## Viitteet ##

* [LZO - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)


