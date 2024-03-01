{
  "date": "2019-10-11",
  "keywords": [
"gif-tiedosto",
"gif-tiedostomuoto",
"mikä on gif-tiedosto",
"tiedosto",
"gif esimerkki",
"gif tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GIF - Kuvatiedostomuoto",
  "description": "Opi GIF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GIF-tiedostoja.",
  "linktitle": "GIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gi-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on GIF-tiedosto? ##

GIF tai Graphical Interchange Format on erittäin pakatun kuvan tyyppi. Unisysin omistama GIF käyttää LZW-pakkausalgoritmia, joka ei heikennä kuvanlaatua. Jokaiselle kuvalle GIF sallii tyypillisesti enintään 8 bittiä pikseliä kohden ja jopa 256 väriä kuvassa. Toisin kuin [JPEG](/image/jpeg/)-kuvassa, joka voi näyttää jopa 16 miljoonaa väriä ja koskettaa melkoisesti ihmissilmän rajoja. Kun Internet syntyi, GIF-kuvat olivat paras valinta, koska ne vaativat pientä kaistanleveyttä ja olivat yhteensopivia tasaisia värialueita kuluttavan grafiikan kanssa. Animoitu GIF yhdistää useita kuvia tai kehyksiä yhdeksi tiedostoksi ja näyttää ne järjestyksessä animoidun leikkeen tai lyhyen videon luomiseksi. Värirajoitukset ovat jopa 256 jokaisessa ruudussa, ja ne ovat todennäköisesti vähiten sopivia muiden kuvien ja valokuvien toistamiseen värigradientilla.

## GIF-tiedostomuoto ##

Käsitteellisesti GIF-tiedostoissa on kiinteäkokoinen graafinen alue, joka on täytetty nollalla tai useammalla kuvalla. Jotkut GIF-tiedostot jakavat kiinteän kokoisen graafisen alueen tai lohkot osakuviksi, jotka voivat toimia animoituina kehyksinä animoidun GIF:n tapauksessa. GIF-muoto käyttää 1-8 bitin pikselisyvyyttä bittikarttatietojen tallentamiseen. RGB-värimalli- ja palettitietoja käytetään aina kuvien tallentamiseen. Versiosta riippuen kiinteäpituinen otsikko (GIF87a tai GIF89a) määrittää tyypillisen GIF-tiedoston alun.

Tällä hetkellä GIF:stä on saatavilla kaksi versiota: 87a ja 89a. Ensimmäinen on alkuperäinen GIF-muoto, kun taas jälkimmäinen on uusi GIF-muoto. Tässä tiedostomuodossa lohkojen ominaisuudet ja pikselimitat mainitaan kiinteäpituisessa Loogisessa näytön kuvauksessa. Globaalin väritaulukon olemassaolo ja koko voidaan määrittää näytön kuvaajan avulla, joka seuraa mahdollisia lisätietoja. Traileri on tiedoston viimeinen tavu, joka sisältää yhden tavun ASCII-puolipisteestä. Tyypillinen GIF87a-tiedoston asettelu on seuraava:

### Otsikko ###

Otsikko sisältää kuusi tavua, ja sitä käytetään määrittämään tiedostotyyppi GIF-muodossa. Vaikka Looginen näytön kuvaaja on erotettu todellisesta otsikosta, sitä joskus pidetään toisena otsikkona. Sama rakenne, jota käytetään otsikon tallentamiseen, voi tallentaa Loogisen näytön kuvaajan. Kaikki GIF-tiedostot alkavat 3-tavuisella allekirjoituksella ja käyttävät merkkejä GIF tunnisteena. Versio on myös kolme tavua kooltaan ja ilmoittaa GIF-tiedoston version.

### Looginen näytön kuvaus ###

Kiinteäpituinen Image Descriptor määrittää GIF-kuvan luomiseen tarvittavat näytön ja väritiedot. Korkeus- ja Leveys-kentät sisältävät näytön tarkkuuden pienimmän arvon, joka on pakollinen kuvatietojen näyttämiseksi. Jos näyttölaite ei pysty näyttämään määritettyä resoluutiota, tarvitaan skaalaus kuvan näyttämiseksi sopivasti. Näytön ja värikartan tiedot näytetään alla olevan taulukon neljässä alikentässä (kun taas bitti 0 on vähiten merkitsevä bitti):


|Bitit|Alikentät
---|---|
|0-2|Yleisen väritaulukon koko
|3|Väritaulukon lajittelulippu
|4-6|Väriresoluutio
|7|Maailmanlaajuinen väripöytälippu

#### Yleinen väritaulukko ####

Valinnainen yleinen väritaulukko sijoitetaan heti Loogisen näytön kuvaajan jälkeen. Tämä taulukko on kartoitettu indeksoimaan kuvatietojen sisällä olevat pikselien väritiedot. Yleisen väritaulukon puuttuessa jokainen GIF-tiedoston kuva käyttää paikallista väriään. On parempi toimittaa oletusväritaulukko, jos sekä yleinen että paikallinen väritaulukko puuttuvat. Sarja kolmetavuisia kolmioita muodostaa väritaulukon elementit. Jokainen tavu kuvaa RGB-väriarvoa. Punaista, vihreää ja sinistä värejä käytetään kunkin väritaulukon elementin arvoina. Yleisen väritaulukon merkinnät osuvat enintään 256 merkintään ja edustavat aina kahdella potenssilla.

#### Kuvatiedot ####

Kuvadata tallentaa tavun koodaamattomia symboleja, joita seuraa linkitetty aliluettelo sekä LZW-koodattu data.

#### Traileri ####

Trailer edustaa yhtä datatavua, joka on tiedoston viimeinen merkki. Tämän tavun arvo on pysyvästi 3Bh ja määrittää datavirran lopun. Jokaisen GIF-tiedoston viimeisenä on oltava traileri.

## Viitteet ##

* [GIF-tiedostomuoto](https://en.wikipedia.org/wiki/GIF)


