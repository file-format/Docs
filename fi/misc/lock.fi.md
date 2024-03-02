{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOCK-tiedostomuoto - mikä on lukitustiedosto?",
  "description": "Opi LOCK-tiedostomuodosta ja sen .",
  "linktitle": "LOCK",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-loc-fik"
}
},
  "lastmod": "2022-01-26"
}

## Mikä on LOCK-tiedosto?

**LUKITUS**-tiedosto on uudelleennimetty tiedosto, jota sovellukset ja käyttöjärjestelmät käyttävät tiedoston tai laitteen merkitsemiseen lukituksi. Tämä kehottaa muita sovelluksia olemaan käyttämättä tiedostoa, ellei se ole vapaa sitä käyttävästä sovelluksesta. Useimmissa tapauksissa nämä lukkotiedostot ovat tyhjiä, mutta muissa tapauksissa ne voivat sisältää lukkoon liittyviä tietoja, kuten ominaisuuksia ja asetuksia.

Joskus Microsoftin .NET Framework käyttää .lock-tiedostoa **lockeed**-kopioiden luomiseen tietokantatiedostosta. Siinä tapauksessa tietokantatiedoston kopio avautuu .lock-tunnisteella. Tämä ei salli käyttäjän tehdä muutoksia tiedostoon, kun se on toisen käyttäjän käytössä.

## LOCK tiedostomuoto - lisätietoja

Jokainen sovellus luo LOCK-tiedoston ja sen tiedostomuoto on sovelluskohtainen. Nämä lukkotiedostot voidaan tallentaa sekä teksti- että binääritiedostomuodossa.

Lukitustiedostojen olemassaolo estää resurssin samanaikaisen pääsyn useisiin tiedostoihin, jotka yrittävät käyttää kyseistä resurssia. Alkuperäisestä tiedostosta luodaan kopio, jonka nimeen on liitetty .lock-tunniste. Tämä kertoo muille sovelluksille, että niillä on vain luku -oikeus tiedostoon. Esimerkiksi tiedostosta resource.dat tulee resource.data.lock.

Ruby-ohjelmointikielessä saatat törmätä tiedostoon **gemfile.lock**. Täällä Bundler pitää kirjaa tarkat asennetut versiot. Siten kun projekti/kirjasto siirretään toiselle koneelle, käynnissä oleva paketti etsii Gemfile-tiedostosta tarkan asiaankuuluvan version.

## Lukitse tiedosto Linuxissa

Linux tukee kahden tyyppisiä tiedostojen lukituksia: neuvoa-antavia lukituksia ja pakollisia lukituksia.

 * **Advisory Locks**: Lukitustyyppi, jota ei pakoteta. Tässä tapauksessa osallistuvat prosessit tekevät yhteistyötä keskenään hankkien eksplisiittisesti lukkoja. Jos tämä ei ole mahdollista, neuvoa-antavat lukitukset jätetään huomioimatta.

 * **Pakolliset lukitukset**: Pakollisen lukituksen tapauksessa käyttöjärjestelmä pakottaa tiedostojen lukituksen estämällä muita prosesseja lukemasta tai kirjoittamasta tiedostoa. Tämä ei vaadi prosessien välistä yhteistyötä.

pakollinen lukitus ei vaadi osallistuvien prosessien välistä yhteistyötä. Kun pakollinen lukitus on aktivoitu tiedostossa, käyttöjärjestelmä estää muita prosesseja lukemasta tai kirjoittamasta tiedostoa.

## Viitteet

* [GemFile ja Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)

* [Lukitseminen Linuxissa](https://www.baeldung.com/linux/file-locking)
