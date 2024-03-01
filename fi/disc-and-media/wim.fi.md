{
  "date": "2021-08-11",
  "keywords": [
"wim-tiedosto",
"wim-tiedostomuoto",
"mikä on wim-tiedosto",
"tiedosto",
"wim esimerkki",
"wim tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lue lisää WIM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WIM-tiedostoja.",
  "title": "WIM - Windowsin kuvantamismuototiedosto",
  "linktitle": "WIM",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-wi-fim"
}
},
  "lastmod": "2021-08-11"
}

## Mikä on WIM-tiedosto?
Tiedostot, joissa on .wim-tunniste, nähtiin ensimmäistä kertaa Windows Vistassa. WIM kuuluu tiedostopohjaiseen kuvantamismuotoon, joka otettiin tyypillisesti käyttöön Microsoft Windows Vistassa. Se mahdollistaa yhden levykuvan käyttöönoton eri tietokonealustoilla. WIM-tiedostoja käytetään tiedostojen, kuten päivitysten, ohjainten ja komponenttien, hallintaan ilman käyttöjärjestelmän näköistiedoston uudelleenkäynnistystä. AQ WIM -tiedosto sisältää joukon tiedostoja ja niihin liittyviä metatietoja, jotka ovat hyvin samanlaisia kuin muut levytiedostomuodot.

## WIM-tiedostomuodot
WIM-tiedostomuoto ei ole kuin sektoripohjaiset muodot, kuten VHD tai IS, itse asiassa se on tiedostopohjainen, mikä tarkoittaa, että WIM:n tiedon perusyksikkö on tiedosto. Tiedostopohjaisuuden perusetu on se, että tiedostojärjestelmäpuussa viitataan useaan kertaan yksittäiseen tiedostoon ja laitteistoriippumattomuuteen. Se vähentää eri tiedostojen yksitellen avaamisen ja sulkemisen ylimääräistä rasitusta, koska tiedostot tallennetaan yhteen WIM:iin. tiedosto. WIM-tiedostot voivat tallentaa useita levykuvia, joihin viitataan joko niiden ainutlaatuisella nimellä tai numeerisella indeksillä.
### Pakkausalgoritmien tuki
WIM tukee seuraavia pakkausalgoritmien perheitä laskevalla nopeudella ja nousevalla suhteella:
- XPRESS
- LZX
- LZMS
- Kiinteä puristus.
Kolme ensimmäistä perhettä ovat LZ77-pohjaisia, kun taas Solid-pakkaus otettiin käyttöön LZMS:n kanssa WIMGAPI Windows 8:ssa ja DISM Windows 8.1:ssä.
### Työkalut WIM-tiedostomuodolle
Seuraavat työkalut tukevat yleensä WIM-tiedostomuotoa:

- **ImageX**: komentorivityökalu, jolla muokataan, luodaan ja otetaan käyttöön Windows-levykuvia Windows Imaging Formatissa. Yhdessä asiaankuuluvan WIMGAPI:n kanssa se jaetaan osana ilmaista Windowsin automaattista asennuspakettia. Windows Vistasta alkaen Windowsin asennusohjelma käyttää WAIK-sovellusliittymää Windowsin asentamiseen.
- **DISM**: Windows 7:ssä ja Windows Server 2008 R2:ssa käyttöön otettu työkalu, joka voi suorittaa palveluun liittyviä tehtäviä Windowsin asennuskuvassa, olipa kyseessä sitten online-kuva tai offline-kuva kansiossa tai WIM-tiedostossa. tällä työkalulla pystyi asentamaan ja poistamaan kuvia, lisäämään laiteohjaimen offline-kuvaan ja kyselemään asennettuja laiteajureita offline-kuvassa.
 



## Viitteet 

* [Windows Imaging Format - Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



