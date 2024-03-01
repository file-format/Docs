{
  "date": "2019-10-11",
  "keywords": [
"dcm tiedosto",
"dcm tiedostomuoto",
"mikä on dcm-tiedosto",
"tiedosto",
"dcm esimerkki",
"dcm tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DCM-tiedostomuoto – digitaalinen lääketieteellinen tietotiedosto",
  "description": "Lue lisää DCM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DCM-tiedostoja.",
  "linktitle": "DCM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dc-fim"
}
},
  "lastmod": "2021-07-03"
}

## Mikä on DCM-tiedosto?

Tiedostot, joiden laajennus on .dcm, edustavat digitaalista kuvaa, joka tallentaa potilaiden lääketieteellisiä tietoja, kuten magneettikuvauksia, CT-skannauksia ja ultraäänikuvia. DCM-tiedostot käyttävät [DICOM](/image/dicom/) (Digital Imaging and Communications in Medicine) -kuvatiedostomuotoa ja voivat sisältää potilastietoja viitteeksi. Sen on kehittänyt [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA), ja sen tarkoituksena oli standardoida kuvantamistiedostomuoto lääketieteellisten kuvien jakelua ja katselua varten.

## DCM-tiedostomuoto

DCM-tiedostot tallentavat tiedot DICOM-kuvamuodossa. Nämä tiedostot tallentavat tietojoukon, joka on todellista tietoa, joka edustaa DICOM IOD:iin liittyvää SOP-esiintymää. DICOM-tiedoston metatiedot tallennetaan tiedostoon, jota seuraa todellisen tietojoukon tavuvirta.

### DICOM-tiedoston metatiedot ##

Jokainen DICOM-tiedosto sisältää tunnistetietojen otsikon kapseloidulle tietojoukolle, joka koostuu:
   * 128-tavuinen tiedoston johdanto
   * 4-tavuinen DICOM-etuliite
   * Tiedoston metaelementit

Tämä otsikko on pakollinen jokaiselle DICOM-tiedostolle.

### Tiedoston metaelementit ###
|Attribuutin nimi|Tunniste|Tyyppi| Attribuutin kuvaus
---|---|---|---|
|Tiedoston johdanto|Ei tunniste- tai pituuskenttiä|1|Kiinteä 128 tavun kenttä saatavilla sovellusprofiilin tai toteutuksen määrittämää käyttöä varten. Jos sovellusprofiili tai tietty toteutus ei käytä sitä, kaikki tavut on asetettava arvoon 00H. Tiedostosarjan lukijat tai päivittäjät eivät saa luottaa tämän johdannon sisältöön määrittääkseen, onko tämä tiedosto DICOM-tiedosto vai ei.
|DICOM-etuliite|Ei tunniste- tai pituuskenttiä|1|Neljä tavua, jotka sisältävät merkkijonon DICM. Tätä etuliitettä on tarkoitus käyttää tunnistamaan, onko tämä tiedosto DICOM-tiedosto vai ei.
|Tiedoston metatietoryhmän pituus|(0002,0000)|1|Tätä tiedoston metaelementtiä seuraavien tavujen määrä (Arvo-kentän loppu) ryhmän 2 viimeiseen tiedoston metaelementtiin asti. Tiedoston metatiedot
|File Meta Information Version|(0002,0001)|1|This is a two byte field where each bit identifies a version of this File Meta Information header. In version 1 the first byte value is 00H and the second value byte value is 01H.Implementations reading Files with Meta Information where this attribute has bit 0 (lsb) of the second byte set to 1 may interpret the File Meta Information as specified in this version of PS3.10. Kaikkia muita bittejä ei saa tarkistaa.
|Media Storage SOP Class UID|(0002,0002)|1|Tunnistaa yksilöllisesti tietojoukkoon liittyvän SOP-luokan. Mediatallennusta varten sallitut SOP-luokan UID:t on määritelty kohdassa PS3.4 - Media Storage Application Profiles.
|Media Storage SOP Instance UID|(0002,0003)|1|Tunnistaa yksilöllisesti tiedostoon sijoitettuun tietojoukkoon liittyvän SOP-esiintymän, joka seuraa tiedoston metatietoja.
|Siirtosyntaksin UID|(0002,0010)|1|Tunnistaa yksilöllisesti siirtosyntaksin, jota käytetään seuraavan tietojoukon koodaamiseen. Tämä siirtosyntaksi ei koske tiedoston metatietoja.
|Toteutusluokka UID|(0002,0012)|1|Tunnistaa yksilöllisesti tämän tiedoston kirjoittaneen toteutuksen ja sen sisällön. Se tarjoaa yksiselitteisen tunnisteen toteutustyypistä, joka viimeksi kirjoitti tiedoston, jos vaihto-ongelmia ilmenee.
|Toteutusversion nimi|(0002,0013)|3|Tunnistaa toteutusluokan UID:n (0002,0012) version, joka sisältää enintään 16 merkkiä ohjelmistosta.
|Lähdesovellusentiteetin otsikko|(0002,0016)|3|AE:n DICOM-sovellusentiteetin nimi, joka kirjoitti tämän tiedoston sisällön (tai viimeksi päivitti sen). Jos sitä käytetään, se mahdollistaa virheiden lähteen jäljittämisen median vaihto-ongelmien sattuessa.
|Yksityistietojen luojan UID|(0002,0100)|3|Yksityisten tietojen luojan UID (0002,0102).
|Yksityiskohtaiset tiedot|(0002,0102)|1C|Sisältää tiedoston metatietoihin sijoitettuja yksityisiä tietoja. Tekijä on tunnistettava numerolla (0002,0100). Pakollinen, jos Private Information Creator UID (0002,0100) on olemassa.

### Tietojoukon kapselointi ###

DICOM-tiedosto sisältää yhden tietojoukon, joka edustaa yhtä SOP-ilmentymää, joka liittyy yhteen SOP-luokkaan. DICOM-tiedoston metatietojen siirtosyntaksin UID määrittää tietojoukon koodaamiseen käytettävän siirtosyntaksin.

### Tiedostonhallintatietojen tuki ###

Mediamuotokerros tarjoaa seuraavat tiedostonhallintatiedot, jos ne ovat tarpeen tietylle DICOM-sovellusprofiilille.

  * Tiedoston sisällön omistajan tunnistaminen

  * Tiedostojen käyttötilastot (esim. luontipäivämäärä ja -aika)

  * Sovellustiedostojen pääsynhallinta

  * Fyysisen median pääsynhallinta (esim. kirjoitussuojaus)

## Viitteet ##
  * [DICOM-standardi](https://www.dicomstandard.org/current/)
  * [DICOM-tiedostomuoto](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

