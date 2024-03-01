{
  "date": "2019-10-11",
  "keywords": [
"jp2 tiedosto",
"jp2 tiedostomuoto",
"mikä on jp2-tiedosto",
"tiedosto",
"jp2 esimerkki",
"jp2 tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JP2 - Kuvatiedostomuoto",
  "description": "Opi JP2-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JP2-tiedostoja.",
  "linktitle": "JP2",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-fi2"
}
},
  "lastmod": "2020-08-10"
}

## Mikä on JP2-tiedosto? ##

JPEG 2000 (**JP2**) on kuvan koodausjärjestelmä ja huippuluokan kuvanpakkausstandardi. Se käyttää wavelet-tekniikkaa koodatakseen häviötöntä sisältöä missä tahansa laadussa kerralla. Lisäksi JPEG 2000:lla on kyky päästä käsiksi ja purkaa samaa sisältöä tehokkaasti useisiin muihin resoluutioihin ja ominaisuuksiin ilman merkittäviä rangaistuksia koodaustehokkuudesta. JPEG 2000:n koodivirrat ovat merkittävästi skaalautuvat, sillä niissä on kiinnostavia alueita, jotka tarjoavat mahdollisuuden avaruudelliseen satunnaiskäyttöön.

JPEG 2000 erottuu yhdestä skaalautuvimmista standardeista. Kuvan eri osia voidaan tallentaa käyttämällä erilaisia ominaisuuksia. Huomionarvoinen suorituskyvyn eskalaatio voidaan saavuttaa tilaamalla koodivirta useilla eri tavoilla. Tästä huolimatta JP2 vaatii monimutkaisia ja laskennallisesti haastavia lähettimiä/dekoodereita tämän joustavuuden seurauksena. JPEG:iin verrattuna JPEG 2000 tuottaa vain soivia artefakteja, jotka tekevät renkaat lähelle kuvan reunaa ja voivat olla epäselviä, kun taas JPEG käyttää 8 × 8 -kokoisia visuaalisia artefakteja, jotka voivat olla sekä soittoääniä että estäviä artefakteja. Jopa 16 384 erilaista komponenttia, joiden mitat ovat terapikseleja, ja tarkkuus, joka voi olla jopa 38 bittiä/näyte.

## Historia ##

Vuonna 2000 Joint Photographic Experts Group -komitea suunnitteli JP2:n tavoitteenaan parantaa omaa diskreetti kosinimuunnospohjaista JPEG-standardiaan tällä uudella aallokepohjaisella menetelmällä. JPEG-komitea pyrki tarjoamaan perusmenetelmänsä ilman lisenssimaksuja. JP2-lisenssissä kilpailussa 20 yritystä he voittivat voittoa. JPEG 2000 on julistettu ISO-standardiksi, vaikka useimmat verkkoselaimet eivät ole valmiita antamaan kättä JPEG 2000:lle vuoden 2017 jälkeen.

## JPEG 2000 -kuvakoodausjärjestelmän osia ##

Seuraavassa on tärkeimmät osat, jotka muodostavat täydellisen JPEG 2000 -standardisarjan.


|Osa|Nimi|Kuvaus|Numero
---|---|---|---|
|Osa 1|Ydinkoodausjärjestelmä| Määrittää koodivirran syntaksin. JPEG 2000 -kuvien purkamiseen liittyvät eri vaiheet. Selittää perustiedostomuodon JP2, metatiedot ja IP-oikeudet.|ISO/IEC 15444-1
|Osa 2|Laajennukset|Määrittää tiedostomuodon koodivirran laajennukset ja mahdollistaa HDR-esimerkkiesittelyt, väriavaruuden määrittelyn, rajauksen ja geometriset muunnokset. erilaisia animaatioita, metatietoja ja useita koodivirtoja.|ISO/IEC 15444-2
|Osa 3|Motion JPEG 2000 (MJ2 tai MJP2)|Ota käyttöön liikesarjoille tiedostomuoto, joka koodaa kuvat itsenäisenä koodivirtana.|ISO/IEC 15444-3
|Osa 4|Yhteensopivuus|Testi koodaus- ja dekoodaustekniikat ja tarkistaa tiedostot sekä bare code-virroille että JP2-tiedostoille.|ISO/IEC 15444-4
|Osa 5|Viiteohjelmisto|Sisältää kaksi lähdekoodipakettia (Java, C), jotka toteuttavat Core-koodausjärjestelmän ja ovat saatavilla avoimen lähdekoodin lisensseillä.|ISO/IEC 15444-5
|Osa 6|Yhdistelmäkuvatiedostomuoto|Määrittää JPM-tiedostomuodon ja mahdollistaa monisivuisten asiakirjojen kuvantamisen faksimaisissa sovelluksissa. Tukee JBIG2:n ja JPEG:n käyttöä.|ISO/IEC 15444-6
|Osa 8|JPEG 2000 Secured (JPSEC)|Varmistaa tapahtumien, sisällön ja tekniikoiden turvallisuuden ja sallii suojatut JPEG 2000 -bittivirrat.|ISO/IEC 15444-8
|Osa 9|JPIP|Määrittää työkalut verkkoympäristössä metadataan ja kuviin pääsyä varten ja toteaa Interaktiiviset ja tehokkaat protokollat|ISO/IEC 15444-9
|Osa 10|JP3D|Osan 1 tilavuuslaajennus ja esittelee Z-ulottuvuuden. Laajentaa ruutujen, koodilohkojen, alueiden ja 3D-alueen esteettömyysominaisuuksien käsitettä.|ISO/IEC 15444-10
|Osa 11|JPWL|Käsittelyssä hyvin organisoitu tiedonsiirto virhealttiissa langattomassa verkossa. Tämä laajennus on yhteensopiva dekooderien kanssa|ISO/IEC 15444-11
|Osa 13|Entry-level Encoder|Määrittää Core-koodausjärjestelmän lähtötason enkooderin toteutuksen.|ISO/IEC 15444-13
|Osa 14|JPXML|Esitys XML-muodossa ja selittää merkkisegmentit ja menetelmät kuvien sisäisten tietojen käyttämiseksi.|ISO/IEC 15444-14
|Osa 15|HTJ2K (Kehitysvaiheessa)|Määrittää vaihtoehtoisen lohkokoodausalgoritmin. Algoritmi tarjoaa kymmenen kertaa suuremman suorituskyvyn ja häviöttömän koodauksen/dekoodauksen.|

## JP2-tiedostomuoto ##

JPEG 2000 defines file format as well as code stream in the same way as JPEG-1. Vaikka kuvanäytteet on kuvattu yksinomaan JPEG 2000:lla, JPEG-1 sisältää kuitenkin muuta lisättyä tietoa väriavaruudesta ja kuvan koodaamisen kannalta oleellisesta resoluutiosta. Jos kuva on tallennettu JPEG 2000 -tiedostona, tiedostopääteenä käytetään **.jp2**. Tätä tiedostomuotoa parantaa edelleen JPEG 2000 part-2 -laajennus, joka määrittää animaatiomekanismit ja lukuisten koodivirtojen konfiguroinnin yhdeksi kuvaksi. **.jpx**-tunnistetta käytetään, kun kuvat tallennetaan tällä laajennetulla tiedostomuodolla. Koska koodivirtatietojen ei katsota tallennettavan ensisijaisesti tiedostoihin, tähän tarkoitukseen ei ole määritetty standardipäätettä. Vaikka testaustarkoituksiin se saa usein laajennuksen **.jpc** tai **.j2k**. Toisin kuin JPEG-1, JPEG 2000 valitsee erilaisen tavan koodata metatiedot XML-muodossa. Standardia 12234-1.4 (ISO TC42-komitean toimesta) käytetään viitteenä Exif-tunnisteiden ja XML-komponenttien välillä. JPEG 2000 voi sisältää ISO-standardin, XMP.

### Palat ###
JPEG 2000 -tiedostot koostuvat peräkkäisistä paloista. Jokaisessa palassa on 8-tavuinen otsikko: 4-tavuinen kappalekoko (big-endian, korkea tavu ensin) ja 4-tavuinen osatyyppi - yksi ennalta määritetyistä allekirjoituksista: jP tai jP2.

Second chunk must be of type "ftyp" and has a sub-type at offset 8. JPEG 2000 on määritetty alatyypin mukaan, jonka on oltava jokin seuraavista arvoista: jp2 (tiedostotyyppi \*.JP2), jp20 (tiedostotyyppi \*.JPA), jpm (tiedostotyyppi \*.JPM), jpx (tiedostotyyppi \*.JPX).

Toistamme paloja, kunnes tuntematon tyyppi havaitaan, muodostamme JPEG 2000 -kuva-/videotiedoston.

### Värinmuutos ###

Aluksi tarvitaan kuvien muuntamista RGB-väriavaruudesta toiseen väriavaruuteen. Tätä tarkoitusta varten on kaksi tapaa: Irreversible Color Transform (ICT) ja Reversible Color Transform (RCT). Edellinen käyttää YC,,B,,C,,R,,-väriavaruutta ja se tulee toteuttaa kiinteässä/liukupisteessä, kun taas myöhemmin modifioitu YUV-väriavaruus ja luonteeltaan käännettävä.// //Ei rajoitu RGB-malliin, JPEG 2000-kieli käyttää monikomponenttimuunnoksia.

### Laatoitus ###

Kun värimuunnos on tehty, kuva muunnetaan suorakaiteen muotoisiksi alueiksi, joita kutsutaan laatoiksi ja jotka voidaan muuntaa ja koodata erikseen. Kaikkien laattojen koko on sama tai koko kuvaa voidaan pitää yhtenä laatana. Dekooderi hyödyntää laatoitusta ja kuluttaa vähemmän muistia tai voi koodata joitain ruutuja osittain. Vaikka tämän tekniikan haittapuolena on kuvan laadun heikkeneminen.

### Wavelet-muunnos ###

Laatoituksen jälkeinen kuva on aallokemuunnos, joka voi olla joko irreversiibeli tai palautuva ja toteutettu käyttämällä konvoluutio- tai nostokaaviota.

### Puristussuhde ###

Kuvan fyysisistä ominaisuuksista riippuen saadaan 20 %:n pakkausvahvistus. JPEG 2000:n spatiaalinen redundanssiennuste on tärkeässä roolissa pakkausprosessissa, ja korkearesoluutioisilla kuvilla on taipumus saada eniten etua.

## Sovellukset, joita palvelee standardi ##

* Kehyspohjaisten HD-videoiden tallennus, editointi ja tallennus

* Lääketieteelliset kuvat ja biometriset tiedot

* satelliittikuvat, kaukokartoitus ja liiketunnistus

* Asiakas/palvelin-viestintä, verkkojakelu ja tallennus.

* Digitaalinen elokuva, suora HDTV-syöte, digitalisoitu audiovisuaalinen tavara


## Viitteet ##

* [JPEG 2000:n yleiskatsaus](https://jpeg.org/jpeg2000/)

* [JPEG 2000 -kuvakoodausjärjestelmä](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)


