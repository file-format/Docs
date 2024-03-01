{
  "date": "2019-10-11",
  "keywords": [
"AVI",
"Pakattu audio-video",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Multimediasäiliö",
"XVId",
"DivX",
"koodekit",
"Resurssien vaihdon tiedostomuoto",
"RIFF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AVI-tiedostomuoto - Audio-video-lomitustiedosto",
  "description": "Opi AVI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata AVI-tiedostoja.",
  "linktitle": "AVI",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-av-fii"
}
},
  "lastmod": "2021-04-23"
}

## Mikä on AVI-tiedosto? ##

**AVI**-tiedostomuoto on Audio Video -multimediasäilötiedostomuoto, jonka Microsoft esitteli. Se sisältää ääni- ja videodataa, joka on luotu ja pakattu useilla koodekeilla (kooderit/dekooderit), kuten **XVid** ja **DivX**. Koska AVI-sisällön koodaamiseen voidaan käyttää erilaisia koodekkeja, noutavien sovellusten eli AVI-soittimien pitäisi pystyä avaamaan ne vain, jos niille on asennettu tarvittavat koodekit, joilla AVI-sisältö luotiin. Muotoa tuetaan oletusarvoisesti kaikilla **Microsoft Windows** -alustoilla sekä melkein kaikilla muilla tärkeimmillä alustoilla. Useat sovellukset ja API:t tarjoavat mahdollisuuden luoda/tallentaa, lukea ja muuntaa AVI:ta muihin suosittuihin muotoihin, kuten MP4, MOV, WMV jne.

## AVI-tiedostomuoto ##

Tiedosto, jonka tunniste on .avi, on AVI-tiedosto. Se on RIFF:n (Resource Interchange File Format) alimuoto. RIFF järjestää tiedot lohkoiksi tai paloiksi, jotka tunnistetaan FourCC-tunnisteella. AVI-tiedosto on yksinkertaisesti yksi pala RIFF-muotoisessa tiedostossa.

Ensimmäisessä aliosassa tiedoston otsikko tunnistetaan hdrl-tunnisteella; sen sisältö sisältää videon leveyden, korkeuden ja kuvanopeuden. Toisessa alaosassa liiketunniste edustaa videon kuvanopeutta. AVI-video koostuu tämän osan todellisesta audio-/visuaalisesta tiedosta. On myös kolmas valinnainen aliosa, jossa on idx1-tunniste, joka osoittaa tiedostoon kuuluvien yksittäisten tietopalojen sijainnin tiedostossa.

### Rajoitukset ###

* Kuvasuhdetietoja ei voida koodata alkuperäiseen AVI-spesifikaatioon, vaikka uudempi OpenDML-spesifikaatio (AVI 2.0) tarjoaa standardoidun menetelmän

* Vaikka AVI-tiedostoja käytetään laajasti elokuvien ja television jälkituotannossa, erilaiset lähestymistavat aikakoodin lisäämiseksi niihin kilpailevat, mikä vaikuttaa muodon käytettävyyteen.

* AVI-koodattu videotiedosto ei voi käyttää pakkaustekniikkaa, joka edellyttää tulevien kehysten tietoja koodattavan kehyksen (B-kehys) lisäksi.

* On ongelmallista käyttää AVI-tiedostoja vaihtelevalla bittinopeudella (VBR) (kuten MP3-ääni alle 32 kHz:n näytetaajuudella)

* AVI-tiedosto, joka koodaa normaalitarkkuuksisia elokuvia normaalisti käytettynä, aiheuttaa todennäköisesti noin 5 megatavua tunnissa tiedoston käyttötavasta riippuen.

* Tekstitykset on koodattava videovirtaan tai jaettava erillisessä tiedostossa siltä varalta, että AVI-tiedostoihin ei voi sijoittaa liitteitä, kuten kirjasimia ja tekstityksiä


## Lyhyt historia ##

Microsoft esitteli AVI:n vuonna 1992 tavoitteenaan tarjota tehokkaampi ja kehittyneempi ääni- ja videotiedostomuoto. Formaatti tuli nopeasti suosituksi Internetin käytön myötä, jolloin ihmiset voivat jakaa videotiedostoja suoraan ja epäsuorasti pilvipohjaisen mediatallennustilan kautta.

## Viitteet ##

* [AVI - Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)


