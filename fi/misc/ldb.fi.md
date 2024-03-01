{
  "date": "2023-04-20",
  "keywords": [
"ldb-tiedosto",
"mikä on ldb-tiedosto",
"mitä tietoa ldb sisältää",
"mikä on ldb-tiedoston tarkoitus",
"ldb laajennus",
"tiedosto",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "LDB-tiedostomuoto - Microsoft Access Lock -tiedosto",
  "description": "Opi LDB-muodosta ja mitä tietoja se sisältää.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb-fi",
      "parent": "misc"
}
},
  "lastmod": "2023-04-20"
}

## Mikä on LDB-tiedosto?

LDB-tiedosto on Microsoft Accessin käyttämä lukkotiedosto estääkseen useita käyttäjiä muokkaamasta samaa tietokantaa samanaikaisesti. Kun käyttäjä avaa Access-tietokannan, Access luo vastaavan LDB-tiedoston samaan hakemistoon kuin tietokanta. Tämä tiedosto sisältää tietoja siitä, kuka tällä hetkellä käyttää tietokantaa ja mitä tietueita he muokkaavat.

Microsoft Access luo LDB-tiedoston automaattisesti, kun tietokanta avataan, ja se poistetaan, kun tietokanta suljetaan. On tärkeää huomata, että LDB-tiedostoa ei saa koskaan poistaa manuaalisesti, koska tämä voi aiheuttaa ongelmia tietokannan kanssa.

Jos kohtaat ongelmia Microsoft Access -tietokannan kanssa, yksi mahdollinen ratkaisu on yrittää poistaa kyseiseen tietokantaan liittyvä LDB-tiedosto. Tämä vapauttaa kaikki lukot, jotka saattavat estää sinua pääsemästä tietokantaan. Muista kuitenkin tehdä varmuuskopio tietokannasta ennen kuin yrität tätä, koska LDB-tiedoston poistaminen voi aiheuttaa tietojen menetyksen tai vioittumisen, jos se tehdään väärin.

## LDB-tiedostomuoto - lisätietoja

Microsoft Accessin LDB-tiedosto sisältää tietoja käyttäjistä, jotka tällä hetkellä käyttävät tietokantaa, kuten käyttäjänimen, tietokoneen nimen ja kirjautumisajan. LDB-tiedosto sisältää myös tietoa tietokantaan sijoitetuista lukoista, kuten mitä tietueita mikä käyttäjä muokkaa.

Tässä on tarkempi luettelo tiedoista, jotka löytyvät LDB-tiedostosta:

- **Käyttäjänimi** - sen käyttäjän nimi, joka tällä hetkellä käyttää tietokantaa
- **Tietokoneen nimi** - sen tietokoneen nimi, josta käyttäjä käyttää tietokantaa
- **Kirjautumisaika** - aika, jolloin käyttäjä avasi tietokannan ensimmäisen kerran
- **Tietueiden lukitukset** - tiedot siitä, mitä tietueita mikä käyttäjä parhaillaan muokkaa
- **Objekolukot** - tiedot siitä, mitä tietokantaobjekteja (kuten taulukoita, lomakkeita tai raportteja) mikä käyttäjä parhaillaan muokkaa
- **Yhteystiedot** - tiedot siitä, kuinka käyttäjä on yhteydessä tietokantaan (esimerkiksi, käyttääkö hän paikallista tai verkkoyhteyttä)

Microsoft Access käyttää LDB-tiedoston tietoja estääkseen useita käyttäjiä tekemästä ristiriitaisia muutoksia samaan tietokantaan samanaikaisesti. Kun käyttäjä yrittää muokata tietuetta tai objektia, jonka toinen käyttäjä on jo lukinnut, Microsoft Access näyttää viestin, joka osoittaa, että objekti on jo käytössä. LDB-tiedosto päivitetään, kun käyttäjät avaavat ja sulkevat tietokannan ja tekevät muutoksia lukittuihin objekteihin.

## Viitteet
* [What is an LDB File?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

