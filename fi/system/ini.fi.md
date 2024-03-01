{
  "date": "2021-07-07",
  "keywords": [
"INI",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"Initiaatio",
"hakemiston laajennus",
"ohjelmia",
"tietokone",
"sovellus"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "INI - Aloitustiedostomuoto",
  "description": "Opi INI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata INI-tiedostoja.",
  "linktitle": "INI",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-in-fii"
}
},
  "lastmod": "2021-07-07"
}

## Mikä on INI-tiedosto? ##

INI-tiedosto on tietokoneohjelmien viestin konfigurointiasiakirja, joka sisältää julkisia avaimia ominaisuuksille ja osiolle, jotka järjestävät attribuutit puitteisiin ja kielioppiin. Nämä järjestelmätiedostomuotoiset määritysasiakirjat saavat nimensä MS-DOS-käyttöjärjestelmän hakemistopäätteestä INI, joka tarkoittaa aloitusta. Se teki tämän tyyppisen ohjelmiston asennuksen suosituksi. Monet muiden ohjelmistosovellusten ohjelmat käyttävät erilaisia tiedostonimien lisäyksiä, kuten CONF ja [CFG](/system/cfg/), vaikka muoto onkin muodostanut epävirallisen standardin monissa määritystilanteissa.

## INI-tiedostojen lyhyt historia##

Alun perin Windowsin pääasiallinen ohjelmamääritystekniikka oli tekstitiedostomuoto, joka koostui tekstiriveistä, joissa oli yksi tärkeä pari riviä kohden jaettuna osiin. Laiteohjaimet, kirjasintyypit ja käynnistyskäynnistimet tallennettiin kaikki tähän muotoon. Sovellukset tallensivat myös tavallisesti yksittäisiä asetuksia INI-tiedostoihin.
Windows 3.1x:ään asti muotoa tuettiin 16-bittisissä Microsoft Windows -alustoissa. Windows 95:stä lähtien Microsoft alkoi kannustaa kehittäjiä käyttämään Windowsin rekisteriä INI-tiedostojen sijaan konfigurointiin.

## INI-tiedosto - tiedostomuodon tekniset tiedot

### Avaimet/ominaisuudet ###

Avain/ominaisuus on INI-tiedoston peruselementti. Tasa-arvo (=) erottaa kunkin avaimen nimen ja arvon. Nimi näkyy yhtäläisyysmerkin vasemmalla puolella. Tasa-arvosymboli ja puolipiste ovat huomaamattomia kirjaimia Windows-järjestelmässä, joten niitä ei voida käyttää avaimessa. Arvossa voidaan käyttää mitä tahansa merkkiä.

```
name=value
```

### Osat ###

Osion kommentti näkyy hakasulkeissa ([]) omalla rivillään. Osion määrittelyn jälkeen kaikki avaimet on linkitetty kyseiseen osioon. Osat päättyvät aivan seuraavaan osion nimeämiseen tai asiakirjan loppuun; ei ole erityistä osion lopun erotinta. Osioita ei voi pinota; ne voidaan nimetä vain kerran, eikä niitä tarvitse linkittää.

```
[section]
a=a
b=b
```

### Muuttuvat ominaisuudet ###

INI-tiedostomuodolla ei ole maailmanlaajuisesti hyväksyttyä määritelmää. Monet tietokonesovellukset sisältävät toimintoja jo mainittujen lisäksi. Alla oleva luettelo sisältää joitain yleisiä ominaisuuksia, jotka voivat sisältyä tai olla sisällyttämättä mihinkään yksittäiseen ohjelmaan.

* Kommentit

* Pakohahmot 

* Päällekkäiset nimet 



## INI-esimerkki ##

Esimerkki INI-tiedostosta näyttää seuraavalta:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Viite ##

* [DMP – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


