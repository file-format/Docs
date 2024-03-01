{
  "date": "2023-03-22",
  "keywords": [
"cnf tiedosto",
"mikä on cnf-tiedosto",
"kuinka avata cnf-tiedosto",
"tiedosto",
"cnf tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CNF-tiedostomuoto - MySQL-määritystiedosto",
  "description": "Opi CNF-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata CNF-tiedostoja.",
  "linktitle": "CNF",
  "menu": {
    "docs": {
      "identifier": "settings-cnf-fi",
      "parent": "settings"
}
},
  "lastmod": "2023-03-22"
}

## Mikä on CNF-tiedosto?

CNF-tiedostoa (tunnetaan myös nimellä määritystiedosto) MySQL:ssä käytetään MySQL-palvelimen määritysasetusten tallentamiseen. CNF-tiedoston sijainti voi vaihdella käytettävän käyttöjärjestelmän ja asennustavan mukaan. Kokoonpano sisältää tyypillisesti erilaisia asetuksia, kuten oletusmerkkikoodauksen, aikakatkaisut, välimuisti- ja puskurimääritykset, joita voidaan säätää optimoimaan tietokannan suorituskyky käytön perusteella.

## CNF-tiedostomuoto – lisätietoja

Voit luoda CNF:n seuraavilla vaiheilla MySQL:ssä:

1. Avaa tekstieditori esim. Muistio ja luo uusi tiedosto.
2. Lisää tiedostoon haluamasi määritysasetukset, yksi kullekin riville. Tässä on esimerkki:

```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
symbolic-links=0

[client]
user=root
password=password123
```

3. Tallenna tiedosto .cnf-tunnisteella, esimerkiksi mysql.cnf.
4. Siirrä tiedosto sopivaan hakemistoon. Esimerkiksi Linux-järjestelmissä hakemisto voi olla /etc/mysql/conf.d/ tai /etc/mysql/.
5. Käynnistä MySQL-palvelin uudelleen, jotta uudet kokoonpanoasetukset tulevat voimaan.

Muista testata kaikki CNF-tiedostoon tehdyt muutokset muussa kuin tuotantoympäristössä ennen niiden käyttöönottoa tuotantoympäristössä.

## Kuinka avata CNF-tiedosto?

CNF-tiedosto on tekstitiedosto, ja se voidaan avata helposti millä tahansa tekstieditorilla, kuten Notepadilla. Voit avata sen myös napsauttamalla hiiren oikeaa painiketta ja valitsemalla valikosta Avaa sovelluksella. Kun tiedosto on avattu, voit muokata kokoonpanoasetuksia tarpeen mukaan. CNF sisältää erilaisia MySQL-palvelimeen liittyviä asetuksia, kuten portin numeron, lokiasetukset ja puskurin koot. Kun olet muokannut asetuksia, tallenna muutokset ja sulje tekstieditori. Lopuksi käynnistä MySQL-palvelin uudelleen, jotta muutokset tulevat voimaan.

Huomaa, että on tärkeää olla varovainen, kun muokkaat MySQL-määritystiedostoa, koska virheelliset asetukset voivat aiheuttaa sen, että palvelin käyttäytyy arvaamattomasti tai ei käynnisty ollenkaan. On suositeltavaa tehdä varmuuskopio alkuperäisestä tiedostosta ennen muutosten tekemistä, jotta voit tarvittaessa palauttaa sen.

## Viitteet
* [MySQL](https://en.wikipedia.org/wiki/MySQL)


