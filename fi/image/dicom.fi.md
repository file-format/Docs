{
  "date": "2019-10-11",
  "keywords": [
"dicom-tiedosto",
"dicom-tiedostomuoto",
"mikä on dicom-tiedosto",
"tiedosto",
"dicom esimerkki",
"dicom tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DICOM - Digital Imaging and Communications File Format",
  "description": "Opi DICOM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DICOM-tiedostoja.",
  "linktitle": "DICOM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dico-fim"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on DICOM-tiedosto?

DICOM on lyhenne sanoista Digital Imaging and Communications in Medicine ja se liittyy lääketieteellisen informatiikan alaan. DICOMia käytetään eri valmistajien lääketieteellisten kuvantamislaitteiden, kuten tulostimien, palvelinten, skannerien jne. integrointiin, ja se sisältää myös jokaisen potilaan tunnistetiedot yksilöllisyyden vuoksi. DICOM-tiedostoja voidaan jakaa kahden osapuolen välillä, jos ne pystyvät vastaanottamaan kuvadataa DICOM-muodossa. DICOMin viestintäosa on sovelluskerroksen protokolla ja käyttää TCP/IP:tä kommunikoimaan entiteettien välillä. Verkkopalveluiden tukemat versiot ovat 1.0, 1.1, 2 tai uudemmat.

## Historia ##

DICOM was developed jointly by American College of Radiology (ACR) and National Electrical Manufacturers Association (NEMA) for the exchange and viewing of medical images like MRIs, CT scans and ultrasound images. Initially, it was hard to decode the images that the machines produced. Therefore, ACR and NEMA together formed a team in 1983 which released its first standard, ACR/NEMA 300 in 1985. Toinen versio julkaistiin vuonna 1988, ja se oli suositumpi myyjien keskuudessa, mutta pian huomattiin, että myös toinen versio kaipaa parannusta. Standardin kolmas versio julkaistiin vuonna 1993 nimellä DICOM. 3.0 on edelleen uusin versio, mutta sitä on päivitetty jatkuvasti vuodesta 1993 lähtien.

## DICOM-tiedostomuoto ##

DICOM on tiedostomuodon määrittelyn ja verkkoviestintäprotokollan yhdistelmä. DICOM käyttää .DCM-laajennusta. .DCM on olemassa kahdessa eri muodossa eli muodossa 1.x ja muodossa 2.x. DCM Format 1.x on lisäksi saatavilla kahdessa versiossa, normaalina ja laajennetussa muodossa. DICOMin verkkopalveluissa käytetään HTTP- ja HTTPS-protokollia.

### Tiedoston otsikko ###

Tiedoston otsikko sisältää 128-tavun tiedoston johdanto-osan ja 4-tavun DICOM-etuliitteen.

**Johdanto # 128 tavua**|**Etuliite # 4 tavua D, I, C, M**

**Johdantoa** käytetään DICOM-tiedoston kuvien ja muiden tietojen käyttämiseen, mikä takaa yhteensopivuuden yleisesti käytettyjen kuvatiedostomuotojen kanssa.

**Etuliite** sisältää merkkijonon DICM isoina kirjaimina.

### Tietojoukko ###

Jokaisen tiedoston on sisällettävä yksi tietojoukko, joka edustaa SOP-ilmentymää ja SOP-luokkaa siihen liittyvän IOD:n kanssa. Tietojoukko on reaalimaailman tiedon esitys. Tietojoukko sisältää tietoelementtejä ja tietoelementit sisältävät kyseisen objektin attribuuttien arvot. Attribuuttien rakenne on määritelty IOD:issa. DICOM-tietoobjekti koostuu useista attribuuteista, mukaan lukien kohteista, kuten nimi, ID jne., sekä yhdestä erikoisattribuutista, joka sisältää kuvan pikselitiedot.

### Tietoelementit ###

Tietoelementti koostuu tietoelementistä Tag, Arvon pituus ja tietoelementin arvo. Tietoelementtejä on 5 tyyppiä, nimittäin tyypin 1 pakolliset tietoelementit, tyypin 1C ehdolliset tietoelementit, tyypin 2 pakolliset tietoelementit, tyypin 2C ehdolliset tietoelementit ja tyypin 3 valinnaiset tietoelementit. Perus Kolme tietoelementtirakennetyyppiä ovat seuraavat.

**Tietoelementti, jossa on selkeä VR**

|Ryhmän numero|Elementin numero|Arvojen esitys|Varattu|Arvon pituus|Arvokenttä
---|---|---|---|---|---|
|2 tavua|2 tavua|2 tavua|2 tavua # 0x00, 0x00|4 tavua|arvon pituus tavua

**Tietoelementti, jossa on selkeä VR**

|Ryhmän numero|Elementin numero|Arvojen esitys|Arvon pituus|Arvokenttä
---|---|---|---|---|
|2 tavua|2 tavua|2 tavua|2 tavua|arvon pituus tavua

**Tietoelementti, jossa on implisiittinen VR**


|Ryhmän numero|Elementin numero|Arvon pituus|Arvokenttä
---|---|---|---|
|2 tavua|2 tavua|4 tavua|arvon pituus tavua

1. **Data Element Tag**: Järjestetty kokonaisluku, joka edustaa ryhmän numeroa ja elementin numeroa
1. **Arvojen esitys VR**: VR on merkkijono, joka edustaa tietoelementin VR:ää.
1. **Arvon pituus**: edustaako etumerkitön kokonaisluku arvokentän eksplisiittistä pituutta.
1. **Arvokenttä**: Kuvaa tietoelementtien arvot.

## Siirtosyntaksi ##

Siirtosyntaksi on joukko sääntöjä koodaukselle, joka edustaa yksiselitteisesti abstraktimpia syntakseja. Siirtosyntaksin avulla viestivät entiteetit neuvottelevat tukemistaan yleisistä koodaustekniikoista.

## SOP:t ##

IOD:n ja DIMSE:n liitto määrittelee SOP-luokan. SOP-luokan määritelmä sisältää säännöt ja semantiikan, jotka voivat rajoittaa DIMSE-palveluryhmän palvelujen käyttöä tai IOD:n attribuutteja. Esimerkkejä palveluelementeistä ovat Store, Get, Find, Move jne. Esimerkkejä objekteista ovat CT-kuvat, MR-kuvat, mutta ne sisältävät myös aikataululuettelot, tulostusjonot jne.

## Palvelut ##

DICOM tarjoaa erilaisia palveluita, jotka liittyvät pääasiassa tiedonsiirtoon. Jokainen niistä on kuvattu lyhyesti alla:


**Store:** DICOM Store -palvelu lähettää kuvia tai muita esineitä kuvien arkistointi- ja viestintäjärjestelmään (PACS) tai palvelimeen.


**Tallennussitoumus:** Tallennussitoumuspalvelua käytetään vahvistamaan, että kuva on tallennettu pysyvästi laitteeseen mille tahansa medialle.


**Kysely/haku:** Tämän palvelun avulla työasema voi etsiä kuvien tai muiden objektien luettelot ja hakea ne sitten PACS:sta.


**Modaliteettityölista:** Modality worklist -palvelu tarjoaa luettelon kuvantamistoimenpiteistä, jotka kuvanhankintalaite on ajoittanut suorittamaan.


**Tulosta:** Tämä palvelu lähettää kuvat tulostimelle.

## Porttinumerot IP:n kautta ##

DICOM käyttää seuraavia TCP- ja UDP-portteja:

1. 104
1. 2761
1. 2762
1. 11112

## Viitteet ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)

* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)

* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)

* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)


