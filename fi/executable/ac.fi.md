{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Opi AC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ACCDB-tiedostoja.",
  "title" : "AC-tiedostomuoto - Autoconf-komentosarjatiedosto",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-fi",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Mikä on AC-tiedosto?

AC-tiedosto on Autoconf-skriptitiedosto. **Autoconf** on laajennettava M4-makrojen paketti, joka tuottaa komentotulkkikomentosarjat ohjelmistojen lähdekoodipakettien automaattista konfigurointia varten. Nämä komentosarjat voivat mukauttaa paketteja monenlaisiin UNIX-tyyppisiin järjestelmiin ilman käyttäjän manuaalista puuttumista. Autoconf luo konfigurointikomentosarjan paketille mallitiedostosta, jossa luetellaan käyttöjärjestelmän ominaisuudet, joita paketti voi käyttää M4-makrokutsujen muodossa.

Producing configuration scripts using Autoconf requires GNU M4. Sinun tulee asentaa GNU M4 (vähintään versio 1.4.6, vaikka 1.4.13 tai uudempi on suositeltavaa) ennen Autoconfin määrittämistä, jotta Autoconfin asetusskripti löytää sen. Autoconfin tuottamat asetusskriptit ovat itsenäisiä, joten niiden käyttäjillä ei tarvitse olla Autoconfia (tai GNU M4:ää).

## Kuinka avata AC-tiedosto?

AC tulee sanoista Automatic Configuration. Se on GNU Autoconfin luoma komentosarja, jonka avulla ohjelmiston lähdekoodia voidaan mukauttaa erilaisiin Posix-tyyppisiin järjestelmiin testaamalla paketin tarvittavia ominaisuuksia. Skriptiä kutsutaan AC-tiedostoksi.

## Tärkeimmät Autotoolsin komponentit

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools on kokoelma toisiinsa liittyviä paketteja, jotka yhdessä käytettyinä poistavat suuren osan kannettavien ohjelmistojen luomiseen liittyvistä vaikeuksista. Näitä työkaluja yhdessä muutaman suhteellisen yksinkertaisen alkupään toimitetun syöttötiedoston kanssa käytetään paketin koontijärjestelmän luomiseen.

**Peruskatsaus automaattisten työkalujen tärkeimpien komponenttien yhteensopivuudesta.**

!{{HYPERLINKKI1}}

Yksinkertaisella asetuksella:

- Autoconf-ohjelma tuottaa konfigurointikomentosarjan joko configure.in- tai configure.ac-tiedostosta.
- Automake-ohjelma tuottaa Makefile.in-tiedoston Makefile.am-tiedostosta.
- Configure-skripti suoritetaan tuottamaan yksi tai useampi Makefile-tiedosto Makefile.in-tiedostoista.
- `make`-ohjelma käyttää Makefileä ohjelman kääntämiseen.

## Viitteet
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Autotoolsin perusteet](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



