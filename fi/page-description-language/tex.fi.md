{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TEX-tiedostomuoto",
  "description": "Opi TEX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TEX-tiedostoja.",
  "linktitle": "TEX",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-te-fix"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on TEX-tiedosto? ##

**TeX** on kieli, joka koostuu ohjelmoinnista sekä merkintäominaisuuksista ja jota käytetään asiakirjojen ladatmiseen. Donald Knuth Stanfordin yliopistosta on tämän nerokkaan ladontajärjestelmän luoja. TeX on kaikkialla maailmassa tekijöiden ja kustantajien paras valinta korkealaatuisten teknisten asiakirjojen tuottamiseen. TeX tekee erinomaista työtä monimutkaisten matemaattisten lausekkeiden muotoilussa. TeX kilpailee yhdessä laadukkaan valoladontalaitteen kanssa parhaiden perinteisten ladontajärjestelmien tuottamien tulosten kanssa. Siksi sitä pidetään tyylikkäimpinä digitaalisina typografisina järjestelminä.

TeX-syöttötiedostot perustuvat ASCII-koodiin, mikä mahdollistaa käsikirjoitusten jakamisen kirjoittajien, julkaisujohtajien ja kriitikkojen kesken. Laaja valikoima laskentaympäristöjä, lähes kaikki modernit alustat ja monet vanhemmat alustat tukevat TeX:ää. Lisäksi TeX on ilmainen ohjelmisto, joka on saatavilla laajalle kuluttajajoukolle. Monet UNIX-asennukset käyttävät sekä UNIX troff- että TeX-muotoilujärjestelmäänsä eri tarkoituksiin. Muut ladontatehtävät suoritetaan valtavasti LaTeX-, ConTeXt- ja muiden makropakettien muodossa.

## Lyhyt historia ##

TeX was designed and written by Donald Knuth in 1978. Guy Steele Massachusetts Institute of Technologysta muutti TeX:n syöttöä/tulostusta, jotta se toimisi yhteensopimattomassa käyttöjärjestelmässä, kuten Timesharing System (ITS) -järjestelmässä. Ensimmäinen TeX-versio kehitettiin Stanfordin WAITS-käyttöjärjestelmässä ohjelmointikielellä (SAIL) ja testattiin toimimaan PDP-10:ssä. Knuth esitteli ajatuksen lukutaitoisesta ohjelmoinnista edistyneille versioille. Lukutaito ohjelmointi on tapa luoda käännettävää lähdekoodia ja ladostusta (TeX:ssä) ristiin linkitettyä dokumentaatiota varten alkuperäisen tiedoston avulla. Näiden kehittyneiden TeX-versioiden kehittämiseen käytetty kieli on WEB, joka on sekoitus DEC PDP-10 Pascal -ohjelmia siirrettävyyden varmistamiseksi.

A revised new version of TeX published in 1982 and was called TeX82. Suurin muutos on alkuperäisen tavutusalgoritmin korvaaminen Frank Liangin äskettäin kirjoittamalla algoritmilla. Siirrettävyyden varmistamiseksi eri alustoilla TeX82 käyttää liukupisteen sijaan kiinteän pisteen aritmetiikkaa sekä todellista, turing-täydellistä ohjelmointikieltä. Vuonna 1989 TeX:stä ja Metafontista julkaistiin uudet versiot. Joten TeX:n versio 3.0 mahdollistaa 8-bittiset syötteet sallien 256 erilaista merkkiä tekstissä. Version 3 jälkeen päivitykset merkitään lisäämällä ylimääräinen numero desimaalien loppuun, esim. TeX:n nykyinen versio merkitään 3.14159265. Tämä versio on viimeksi päivitetty 12.1.2014.

## TeX-syöttö ##

Syötetiedosto TEXiin voidaan valmistaa tekstieditorilla tavallisella tekstillä. Toisin kuin tyypillinen tekstinkäsittelyohjelma, tämä syöttötiedosto ei salli näkymättömiä ohjausmerkkejä. Yksi tiedosto voidaan upottaa toiseen tiedostoon, joka sisältää makromäärityksiä ja apumääritelmiä, jotka parantavat TeX:n ominaisuuksia. Jos TeX-asennuksen mukana tulee makrotiedostoja, paikalliset TeX-tiedot osoittavat makrotiedostojen käytön. TeX:n vakiomuoto integroi makrojen ja muiden määritelmien yhdistelmän, joka tunnetaan nimellä plain TEX.

Kaikkien merkkien ja symbolien kokojen tarkan tietämyksen perusteella se laskee kirjainten optimaalisen järjestyksen riviä ja riviä kohden. Asiakirjan käsittelyn yhteydessä tuotetaan .dvi-tiedosto, jossa dvi tarkoittaa laiteriippumatonta. Dvi-laajennuksella varustetun asiakirjan tulostamiseen tai esikatseluun tarvitaan laiteohjainohjelmia. Nykyään dvi-sukupolvi ohitetaan yleisesti käytetyllä pdf-TeX:llä. TeX-asennuksessa ei ole saatavilla aiempaa tietoa fonteista, joten ulkoisia fonttitiedostoja, jotka ovat osa paikallista TeX-ympäristöä, käytetään tiedon hankkimiseen asiakirjaa varten.

## Kirjoitusjärjestelmä ##

Noin 300 primitiiviä (komentoa) voidaan ymmärtää TeX-perusjärjestelmällä. Primitiivit ovat matalan tason komentoja, joten tavallinen käyttäjä käytti niitä harvoin suoraan ja useimmat toiminnot suoritetaan muototiedostoilla. Nämä tiedostomuotoiset tiedostot ovat valmiiksi ladattuja TeX-muistikuvia, joita seuraa suurten makrokokoelmien lataaminen. Kielen alkuperäinen oletusmuoto eli plain TeX lisää noin 600 komentoa.

Aaltosulkeisiin ryhmitelty kenoviiva tarkoittaa TeX-komentojen alkamista. Koska TeX on makro- ja merkkipohjainen kieli, lähes kaikki TeX:n syntaktiset ominaisuudet voidaan muuttaa ajon aikana, mukaan lukien käyttäjän määrittämät, paitsi laajennettavissa olevat tunnukset, jotka sitten suoritetaan. Laajentaminen itsessään on käytännössä ongelmatonta. Joidenkin komentojen on tultava argumenttien jälkeen, jotka auttavat selittämään komennon toiminnan. Esimerkiksi \vskip-komento ohjaa TEXin ohittamaan sivua alas/ylöspäin, mitä seuraa argumentti, joka määrittää, kuinka paljon tilaa ohitetaan.

## Versiot ##

LaTeX on yleisimmin käytetty formaatti, jonka alun perin on kehittänyt Leslie Lamport. LaTeX integroi erilaisia dokumenttityylejä tiedostoille, kirjeille, kirjoille ja dioille ja tarjoaa viittauksen ja automaattisen numeroinnin eri osioihin ja matemaattisiin lausekkeisiin. AMS-TeX on toinen suosittu muoto, jonka on kehittänyt American Mathematical Society.

AMS-TeX tarjoaa paljon käyttäjäystävällisempiä komentoja, jotka lehdet voivat määrittää uudelleen sopimaan paikalliseen tyyliinsä. LaTeX voi hyödyntää AMS-TeX:n edut käyttämällä AMS:n paketteja, joita sitten kutsutaan nimellä AMS-LaTeX. ConTeXt on toinen Hans Hagenin kirjoittama muoto, jota käytetään pääasiassa tietokonejulkaisuun.

TeX-ohjelmisto tarjoaa useita ominaisuuksia, jotka eivät olleet saatavilla tai olivat huonolaatuisempia muissa ladontajärjestelmissä sen luomishetkellä. Jotkut tämän kielen innovatiivisista ominaisuuksista perustuvat mielenkiintoisiin algoritmeihin, jotka on johdettu Knuthin opiskelijoiden opinnäytteistä. Vaikka muut ladontaohjelmat ovat nyt sisällyttäneet TeX:n hyödyllisiä ominaisuuksia ohjelmiinsa.

## Viitteet ##

* [TeX-tyyppinen kirjoitusjärjestelmä](https://en.wikipedia.org/wiki/TeX)


