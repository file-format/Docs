{
  "date": "2019-10-11",
  "keywords": [
"tar-tiedosto",
"tar-tiedostomuoto",
"mikä on tar-tiedosto",
"tiedosto",
"terva esimerkki",
"tar tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TAR - Unix-arkistotiedostomuoto",
  "description": "Opi TAR-tiedostosta ja sovellusliittymistä, jotka voivat luoda ja avata TAR-tiedostoja.",
  "linktitle": "TAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ta-fir"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on TAR-tiedosto?

Tiedostot, joiden tiedostotunniste on .tar, ovat arkistoja, jotka on luotu Unix-pohjaisella apuohjelmalla yhden tai useamman tiedoston keräämiseen. Useita tiedostoja tallennetaan pakkaamattomassa muodossa tiedostojen ja kansioiden lisäämisen tuella arkistoon. Unixin TAR-apuohjelma on komentopohjainen, mutta useimmat tiedostojen arkistointijärjestelmät tukevat näin luotuja tiedostoja lähes kaikissa käyttöjärjestelmissä. Sen loi ensimmäisen kerran vuonna 1979 AT&T Bell Laboratories, ja myöhemmät versiot julkaistiin ajan myötä.

## TAR-tiedostomuoto

TAR is an open file format with full specifications available for developer's reference. Its file structure was standardized in POSIX.1-1988 and later in POSIX.1-2001. Tar:n luomat tietojoukot säilyttävät tietoja tiedostojärjestelmän parametreista, kuten:

* Nimi

* Aikaleimat

* Omistajuus

* Tiedostojen käyttöoikeudet

* Hakemistoorganisaatio


TAR-tiedostolla ei ole taikanumeroa. Se sisältää sarjan lohkoja, joissa jokainen lohko on BLOCKSIZE tavua.

Jokaista arkistoitua tiedostoa edustaa otsikkolohko, joka kuvaa tiedostoa, jota seuraa nolla tai useampi lohko, joka ilmoittaa tiedoston sisällön. Arkistotiedoston lopussa on kaksi 512-tavuista lohkoa, jotka on täytetty binäärinollalla tiedoston loppumerkintänä. Kohtuullisen järjestelmän tulisi kirjoittaa tällainen tiedoston loppumerkki arkiston loppuun, mutta se ei saa olettaa, että tällainen lohko on olemassa, kun arkistoa luetaan. Erityisesti GNU tar antaa aina varoituksen, jos se ei kohtaa sitä.

Lohkot voidaan estää fyysisiä I/O-toimintoja varten. Jokainen n lohkon tietue (jossa n on asetettu estokerroin = 512-size-vaihtoehdolla tar:ksi) kirjoitetaan yhdellä write()-operaatiolla. Magneettinauhalla tällaisen kirjoituksen tulos on yksi tietue. Arkistoa kirjoitettaessa viimeinen lohkotietue tulee kirjoittaa täysikokoisena, ja nollalohkon jälkeiset lohkot sisältävät kaikki nollat. Arkistoa luettaessa järkevän järjestelmän tulee käsitellä oikein arkistoa, jonka viimeinen tietue on muita lyhyempi tai joka sisältää roskatietueita nollalohkon jälkeen.

### TAR-tiedoston otsikko

Kuten kaikki muutkin tiedoston otsikot, tar-tiedoston otsikkotietue sisältää metatietoja tiedostosta, ja se näkyy seuraavassa taulukossa.

|Kentän siirtymä|Kentän koko (tavuja)|Kenttä
---|---|---|
|0|100|Tiedoston nimi
|100|8|Tiedostotila
|108|8|Omistajan numeerinen käyttäjätunnus
|116|8|Ryhmän numeerinen käyttäjätunnus
|124|12|Tiedoston koko tavuina (oktaalikanta)
|136|12|Viimeinen muokkausaika numeerisessa Unix-aikamuodossa (oktaali)
|148|8|Otsikkotietueen tarkistussumma
|156|1|Linkin ilmaisin (tiedostotyyppi)
|157|100|Linkitetyn tiedoston nimi

Käyttämättömät kentät täytetään NUL-tavuilla. Otsikko koostuu 257 tavusta, joka on täytetty NUL-tavuilla, jotta se täyttää 512 tavun tietueen.

## Kuinka luoda TAR-tiedosto

### Luo TAR-tiedosto Windowsissa

Windowsissa voit käyttää Windows-alijärjestelmää Linuxille (WSL) tai kolmannen osapuolen työkaluja, kuten 7-Zipiä, luodaksesi TAR-tiedostoja. Näin teet sen WSL:n avulla:

 1. Asenna WSL, jos et ole jo tehnyt sitä. Voit asentaa sen Windowsin ominaisuuksien asetuksista.

 1. Avaa WSL-pääte ja käytä samaa tar-komentoa kuin Linux- tai Unix-järjestelmissä TAR-tiedoston luomiseen.

### Luo TAF-tiedosto Linuxissa komentoriviltä

Jos haluat luoda TAR-tiedoston komentorivillä Linux- tai Unix-pohjaisissa järjestelmissä, avaa pääte ja käytä tar-komentoa. Voit luoda TAR-tiedoston useissa pakkausmuodoissa (esim. .tar.gz, .tar.bz2, .tar.xz), mutta tässä luomme tavallisen .tar-tiedoston:

Voit luoda TAR-tiedoston yhdestä tiedostosta tai hakemistosta käyttämällä seuraavaa komentoa:

```
tar -cvf archive.tar file_or_directory
```

## Kuinka avata TAR-tiedosto

### Avaa TAR-tiedosto Windowsissa

Sinun on asennettava purkuapuohjelma Windows-käyttöjärjestelmään, kuten 7-Zip. Se on ilmainen arkistointiapuohjelma, jota voidaan käyttää erilaisten pakattujen tiedostomuotojen luomiseen ja purkamiseen. Napsauta hiiren kakkospainikkeella TAR-tiedostoa ja valitse **Pura**.

### Avaa TAR-tiedosto Macissa

Macissa kaksoisnapsauta TAR-, TGZ- tai TAR.GZ-tiedostoa sen purkamiseksi.

### Avaa TAR-tiedosto Linuxissa

Jos käytät Linuxia tai Mac Terminal -sovellusta, käytä tar -xvf -merkkiä TAR-tiedostoille tai tar -xvzf tiedostoille, joiden pääte on TGZ tai TAR.GZ.

## Viitteet ##

* [TAR - Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))

* [TAR-perusmuoto](https://www.gnu.org/software/tar/manual/html_node/Standard.html)


