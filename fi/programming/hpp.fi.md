{
  "date": "2023-06-08",
  "keywords": [
"hpp tiedosto",
"mikä on hpp-tiedosto",
"mitä hpp-tiedosto sisältää",
"hpp-tiedosto esimerkki",
"mikä on hpp-tiedoston muoto",
"tiedosto",
"hpp tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "HPP-tiedostomuoto - C++-otsikkotiedosto",
  "description": "Opi HPP-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata HPP-tiedostoja.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp-fi",
      "parent": "programming"
}
},
  "lastmod": "2023-06-08"
}

## Mikä on HPP-tiedosto?

.hpp-tiedostomuotoa käytetään yleisesti otsikkotiedostoissa C++-ohjelmointikielellä. Otsikkotiedostot sisältävät yleensä funktioiden, luokkien, muuttujien ja vakioiden ilmoituksia ja määritelmiä, joita muut C++-projektin lähdekooditiedostot käyttävät.

Otsikkotiedostojen käytön tarkoituksena on tarjota tapa jakaa yhteistä koodia useiden lähdekooditiedostojen kesken ilman, että itse koodia kopioidaan. Kun C++-lähdetiedoston on päästävä käsiksi otsikkotiedoston ilmoituksiin tai määritelmiin, se sisältää otsikkotiedoston käyttämällä esiprosessorin käskyä #include.

.hpp-tiedostotunnistetta käytetään usein osoittamaan, että tiedosto on C++-otsikkotiedosto. Tämän nimenomaisen tunnisteen käyttäminen otsikkotiedostoissa ei ole pakollista, ja saatat myös törmätä otsikkotiedostoihin, joissa on .h tai muu tunniste. Laajennuksen valinta on pitkälti sopimuskysymys ja henkilökohtainen mieltymys.

Kun C++-lähdetiedosto sisältää otsikkotiedoston käyttämällä #include, kääntäjä yhdistää tehokkaasti otsikkotiedoston sisällön lähdetiedostoon ennen sen kääntämistä yksikkönä. Tämä mahdollistaa lähdetiedoston pääsyn otsikkotiedoston ilmoituksiin ja määritelmiin, mikä tarjoaa kääntäjälle tarvittavat tiedot tyypintarkistuksen ja koodin luomisen suorittamiseen.

## Mitä HPP-tiedosto sisältää?

Tässä on joitain yleisiä .hpp-tiedostojen sisältöä:

- **Funktioilmoitukset:** Otsikkotiedostot sisältävät usein funktiomäärittelyjä ilman niiden varsinaista toteutusta. Nämä ilmoitukset antavat tietoa funktion nimestä, palautustyypistä ja parametreista, jolloin muut lähdekooditiedostot voivat käyttää funktiota ilman, että niiden tarvitsee tietää toteutustietoja.
- **Luokkien ilmoitukset:** Otsikkotiedostot voivat sisältää luokkamäärityksiä, mukaan lukien luokan nimen, jäsenmuuttujat, jäsenfunktiot ja käyttöoikeusmääritykset. Sisällyttämällä luokan ilmoituksen otsikkotiedostoon muut lähdekooditiedostot voivat luoda kyseisen luokan objekteja ja käyttää sen jäseniä.
- **Vakioilmoitukset:** Otsikkotiedostot voivat määrittää vakioita, kuten yleisiä muuttujia tai enum-arvoja, jotka on tarkoitettu jaettavaksi useiden lähdekooditiedostojen kesken. Näitä vakioita voidaan käyttää sisällyttämällä otsikkotiedosto muihin lähdetiedostoihin, jolloin ne voivat käyttää määritettyjä vakioita.
- **Tyyppimääritykset:** Otsikkotiedostot voivat sisältää tyyppimääritelmiä typedef-avainsanalla tai tyyppialiaksia using-avainsanalla. Nämä määritelmät luovat uusia nimiä olemassa oleville tyypeille, mikä tekee koodista luettavamman ja ylläpidettävämmän.
- **Sisäiset funktiomääritykset:** Joissakin tapauksissa otsikkotiedostot voivat sisältää upotettuja funktiomääritelmiä. Sisäiset funktiot ovat pieniä toimintoja, joita laajennetaan puhelupaikassa sen sijaan, että niitä kutsuttaisiin erilliseksi funktioksi. Sisällyttämällä funktion määritelmän otsikkotiedostoon kääntäjä voi korvata funktiokutsun suoraan funktion rungolla, mikä saattaa parantaa suorituskykyä.

## Esimerkki HPP-tiedostosta

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Mikä on HPP-tiedoston muoto?

HPP on pelkkä tekstitiedosto, mutta noudattaa C++-ohjelmointikielen yleisiä sääntöjä ja syntaksia. Tässä on erittely .hpp-tiedoston yleisestä muodosta ja rakenteesta:

- **Otsikkosuojat:** Tyypillisesti .hpp-tiedosto alkaa otsikkosuojalla saman tiedoston useiden sisällyttämisen estämiseksi. Tämä saavutetaan käyttämällä esiprosessoriohjeita, kuten #ifndef, #define ja #endif. Otsikkosuoja varmistaa, että tiedoston sisältö sisällytetään vain kerran käännösprosessin aikana.
- **Sisällytä lausekkeet:** Otsikkosuojien jälkeen voit sisällyttää muita tarvittavia otsikkotiedostoja #include-käskyn avulla. Nämä voivat sisältää vakiokirjaston otsikoita tai muita koodisi edellyttämiä mukautettuja otsikoita.
- **Declarations and Definitions:** .hpp-tiedoston ensisijainen sisältö on määritykset ja joissakin tapauksissa luokkien, funktioiden, vakioiden, tyyppialiaksien ja muiden elementtien määritelmät. Voit esimerkiksi ilmoittaa luokat käyttämällä luokka-avainsanaa, funktioita käyttämällä niiden palautustyyppiä, nimeä ja parametriluetteloa ja vakioita käyttämällä const-avainsanaa ja niiden tyyppiä ja nimeä.
- **Sisäiset funktiomääritykset:** Tietyissä tapauksissa voit sisällyttää tekstin sisäisiä funktiomääritelmiä suoraan .hpp-tiedostoon. Inline-funktiot määritellään yleensä luokan rungon sisällä, mikä tarkoittaa, että funktion määritelmä sisältyy sen määrittelyyn. Tämä voidaan tehdä lisäämällä funktiomäärittelyn eteen inline-avainsana.
- **Nimitilan ilmoitukset:** Jos käytät koodissasi nimiavaruuksia, voit ilmoittaa ne .hpp-tiedostossa. Tämä tehdään käyttämällä nimiavaruuden avainsanaa, jota seuraa nimitilan nimi ja sulkemalla asiaankuuluva koodi nimiavaruuslohkoon.

## Viitteet
* [Otsikkotiedostot (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


