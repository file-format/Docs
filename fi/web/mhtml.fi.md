{
  "date": "2019-10-11",
  "keywords": [
"mhtml",
"mhtml-tiedosto",
"mhtml-tiedostomuoto",
"mhtml-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on mhtml-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHTML - MIME HTML -tiedosto",
  "description": "Opi MHTML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MHTML-tiedostoja.",
  "linktitle": "MHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mhtm-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on MHTML-tiedosto?

MHTML-laajennuksella varustetut tiedostot edustavat verkkosivun arkistomuotoa, joka voidaan luoda useilla eri sovelluksilla. Muotoa kutsutaan arkistomuodoksi, koska se tallentaa verkko-**[HTML](/web/html/)**-koodin ja siihen liittyvät resurssit yhteen tiedostoon. Nämä resurssit sisältävät mitä tahansa verkkosivulle linkitettyä sisältöä, kuten kuvia, sovelmia, animaatioita, äänitiedostoja ja niin edelleen. MHTML-tiedostoja voidaan avata useissa sovelluksissa, kuten Internet Explorerissa ja Microsoft Wordissa. Microsoft Windows käyttää MHTML-tiedostomuotoa sellaisten ongelmien skenaarioiden tallentamiseen, jotka on havaittu käytettäessä mitä tahansa ongelmia aiheuttavaa Windows-sovellusta. MHTML-tiedostomuoto koodaa sivun sisällön samaan tapaan kuin message/rfc822:ssa, joka on pelkkä tekstisähköpostiin liittyvät tiedot. Varsinaiset muodon tekniset tiedot ovat {{HYPERLINKKI}}:n mukaan.

## MHTML-tiedostomuoto

MHTML tunnetaan myös nimellä MIME Encapsulation of Aggregate HTML -dokumentit, koska se pystyy koodaamaan HTML-web-sivuja ja sen resursseja yhteen verkkoarkistoon. RFC 2557 -spesifikaatioiden mukaan koontidokumentti on MIME-koodattu viesti, joka sisältää pääresurssin (objektin) sekä muita resursseja, jotka on linkitetty siihen URI:iden kautta. Tällaisia muita resursseja voivat olla upotetut kuvat, tyylisivut, sovelmat jne. Lisäksi nämä voivat olla muiden multimediadokumenttien juuria. Täydelliset MHTML-tiedostomuodon asiakirjan tekniset tiedot ovat [RFC 2557](https://tools.ietf.org/html/rfc2557):ssa, ja niihin tulee viitata minkä tahansa tämän tiedostomuodon lukemista/kirjoittamista varten kehitettäessä. Standardi määrittelee, että viitattavat kehon osat voidaan tunnistaa joko Content-ID:n tai Content-Location -tunnuksen avulla.

### MIME-sisällön otsikot

MIME-sisällön otsikko, Content-Location, on määritetty ratkaisemaan URI-viittaukset muiden kehon osien resursseihin. Tämä otsikko voi esiintyä missä tahansa viestin tai sisällön otsikossa.

### Sisältö-sijaintiotsikko

Sisältö-sijainti on esitys URI:sta, joka merkitsee sen ruumiinosan sisällön, johon se on sijoitettu. Sen arvo voi olla absoluuttinen tai suhteellinen URI. Sitä voidaan käyttää merkitsemään resurssi, jota jotkut tai kaikki viestin vastaanottajat eivät voi hakea. Yhdellä viestillä saa olla vain yksi Content-Location-otsikko. Esimerkki moniosaisesta/liittyvästä rakenteesta, joka sisältää kehon osia sekä Content-Location- että Content-ID-tunnisteilla:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### MHTML-aggregaattien URI:t

MHTML-aggregaatin URI on erilainen kuin sen juuri-URI:n. Sisältö-sijainti-otsikkokenttää tulee soveltaa koko aggregaattiin, jos sitä käytetään moniosaisen/liittyvän otsikon otsikossa. Vastaavasti haettu resurssijoukko voi olla erilainen kuin resurssien joukko, joka on haettu osien sisältösijainteja käyttämällä, kun MHTML-aggregaattiin viittaavaa URI:tä käytetään tämän aggregaatin hakemiseen. Esimerkiksi MHTML-aggregaatin noutaminen voi palauttaa vanhan version, kun taas juuri-URI:n ja sen sisäisten linkitettyjen objektien haku voi palauttaa uudemman version.

## Viitteet

* [Aggregate Documents MIME Encapsulation - RFC 2557](https://tools.ietf.org/html/rfc2557)

* [MHTML-tiedostomuoto - Wikipedia](https://en.wikipedia.org/wiki/MHTML)


