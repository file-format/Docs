{
  "date": "2019-12-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIM-tiedostomuoto - OpenZIM-arkistotiedosto",
  "description": "Opi ZIM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ZIM-tiedostoja.",
  "linktitle": "ZIM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-fim"
}
},
  "lastmod": "2019-12-09"
}

## Mikä on ZIM-tiedosto? ##

Tiedostot, joiden laajennus on .zim, ovat arkistoja, jotka on luotu Wiki-sisällön tallentamiseen offline-tilassa. Sitä pidetään sopivimpana avoimena tiedostomuotona Wikipedian tallentamiseen USB:lle. Se tallentaa sivuston sisällön kompaktissa muodossa. Sen nimi tulee sanasta Zeno IMproved, joka oli aikaisempi Zeno-tiedostomuoto. ZIM:ää ylläpitää [openZIM ](https://openzim.org/)projekti, jota sponsoroi Wikimedia CH ja jota tukee Wikimedia Foundation. ZIM-tiedostoja voidaan avata sovelluksilla, kuten Kiwix ja ZIMReader. OpenZIM-projekti on isännöinyt ZIM-tiedostomuodon käyttöönottoa osoitteessa [Github](https://github.com/openzim) OpenSource-yhteisön osallistumista varten.

## ZIM-tiedostomuodon tekniset tiedot

ZIM-tiedostomuoto kehitettiin [Zeno file format](https://openzim.org/wiki/Zeno_file_format):n päälle, eikä se ole taaksepäin yhteensopiva. ZIM-tiedostomuodon muotomääritykset ovat openZIM:n [available online](https://openzim.org/wiki/ZIM_file_format) kehittäjien tiedoksi. OpenZIM on tarjonnut C++ avoimen lähdekoodin toteutuksen, [LibZim](https://openzim.org/wiki/Zimlib), ZIM-tiedostojen lukemiseen ja kirjoittamiseen.

ZIM-tiedostomuoto käyttää LZMA2-pakkausta sisällön tiivistämiseen.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM-tiedostomuoto" >}}


### ZIM-otsikko

A ZIM file starts with a header that is at offset 0. Kaikki osatekijät perustuvat little-endianiin ja kaikki kokonaisluvut ovat etumerkittömiä kokonaislukuja eli uint_16, uint_32, uint_64.

|Kentän nimi |Tyyppi| Offset| Pituus| Kuvaus|
---|---|---|---|---|
|magicNumber| kokonaisluku| 0| 4| Maaginen numero tiedostomuodon tunnistamiseksi on 72173914 (0x44D495A)|
|pääversio| kokonaisluku| 4| 2| ZIM-tiedostomuodon pääversio (5 tai 6)|
|alaversio| kokonaisluku| 6| 2| Pieni versio ZIM-tiedostomuodosta|
|uuid| kokonaisluku| 8| 16| tämän zim-tiedoston yksilöllinen tunnus|
|articleCount| kokonaisluku| 24| 4| artikkelien kokonaismäärä|
|clusterCount| kokonaisluku| 28| 4| klustereiden kokonaismäärä|
|urlPtrPos| kokonaisluku| 32| 8| URL|:n mukaan järjestetyn hakemiston osoitinlistan sijainti
|titlePtrPos| kokonaisluku| 40| 8| hakemiston osoitinlistan sijainti Title|:n mukaan
|klusteriPtrPos| kokonaisluku| 48| 8| klusterin osoitinluettelon sijainti|
|mimeListPos| kokonaisluku| 56| 8| MIME-tyyppiluettelon sijainti (myös otsikon koko)|
|pääsivu| kokonaisluku| 64| 4| pääsivu tai 0xffffffff, jos pääsivua ei ole|
|layoutPage| kokonaisluku| 68| 4| asettelusivu tai 0xffffffffff, jos asettelusivua ei ole|
|checksumPos| kokonaisluku| 72| 8| osoitin tämän tiedoston md5checksumiin ilman itse tarkistussummaa. Tämä osoittaa aina 16 tavua ennen tiedoston loppua.|

## Viitteet ##

* [OpenZIM](https://openzim.org/)

* [C++ LibZim](https://openzim.org/wiki/Zimlib)


