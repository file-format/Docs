{
  "date": "2021-08-11",
  "keywords": [
"vox",
"tiedosto",
"laajennus",
"muoto",
"audio",
"ADPCM",
"Dialoginen ADPCM",
"Xentec VOX Studio",
"vox laajennus",
"vox-tiedostoja"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Opi VOX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VOX-tiedostoja.",
  "title": "VOX - äänitiedostomuoto",
  "linktitle": "VOX",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-vo-fix"
}
},
  "lastmod": "2021-08-11"
}

## Mikä on VOX-tiedosto? ##

Pienellä näytteenottotaajuudella VOX-tiedostot on määritetty tallentamaan digitoitua äänidataa. Nämä ovat äänitiedostoja, joita käytetään yleisesti puhelinviestintään määritellyissä sovelluksissa. Tämäntyyppinen tiedostomuoto käyttää häviöllisen pakkauksen algoritmia, joka on optimoitu puheelle.

Puhesovelluksissa yleisesti käytetyt VOX-tiedostot sisältävät valmiiksi tallennettuja äänikehotteita. Tämän tyyppinen tiedostomuoto muunnetaan myös muihin suositumpiin muotoihin. Näitä voidaan käyttää Windows-käyttöjärjestelmässä ja macOS:ssä.

Sitä käytetään enimmäkseen äänitallenteisiin ja pakkaamiseen. Tässä muodossa polyfonista dataa ei voida tallentaa, koska se tukee vain homofobista dataa.



## Lyhyt historia ##

VOX-tiedostot liittyvät Dialogicin DMV- ja JCT-nimiin medialevyihin. Nämä kuuluvat VoxWarelle ja moniin muihin ohjelmistoihin. Sitä pidettiin aiemmin vanhentuneena muotona.

Vanhentuneena muotona sitä ei käytetty sen jälkeen. Muiden ADPCM-muotojen tapaan se pakattiin 4 bittiin. Näiden tiedostojen ominaisuudet ovat riittävän lähellä [WAV](/audio/wav/)-tiedoston määrityksiä.


## Muototiedot ##

Tämän tyyppinen tiedostomuoto on yhteensopiva Windows-käyttöjärjestelmän ohjelmien, kuten Xentec Vox Studio, kanssa. Sillä on erityispiirteitä, joita käytetään stimuloimaan ihmisten puhetta. Arcade-pelit käyttävät enimmäkseen tätä muotoa. VOX-tiedostopäätteessä on 32-tavuinen otsikko sekä 10-tavuiset indeksit ja kehykset. Varsinainen äänidata tallennetaan kehyksiin segmenttien muodossa yhteen tiedostoon. Jokaisessa kehyksessä on erilainen useiden tavujen muoto koodaustyypin mukaan.

Äänen selkeys säilyy alhaisella näytteenottotaajuudella, mikä on harvinaista useimmissa äänimuodoissa. Näissä käytetty algoritmi oli matemaattinen.

Tämä tiedosto on koodattu ADPCM:llä. Se oikosulkee 16-bittisen äänidatan ja 4-bittisen pakkauksen. On siis eduksi tallentaa suurempia äänitietoja kompaktissa muodossa käyttämällä VOX-tiedostoja.


## Viitteet ##

* [VOX - Wikipedia](https://en.wikipedia.org/wiki/Dialogic_ADPCM)


