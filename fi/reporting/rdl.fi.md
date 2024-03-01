{
  "date": "2021-03-01",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDL - Raportin määritelmän kielitiedosto",
  "keywords": [
"rdl",
"raportin määrittelykieli",
"XmlTextWriter",
"XSD",
"RDL-elementti"
],
  "description": "Lisätietoja RDL-tiedostomuodosta, joka on SQL Server Reporting Services -raporttimäärittelyn XML-esitys.",
  "linktitle": "RDL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rd-fil"
}
},
  "lastmod": "2021-03-01"
}

## Mikä on RDL-tiedosto? ##

RDL (Report Definition Language) on Microsoftin asettama vertailukohta raporttien määrittelylle. RDL-tiedosto koostuu yhdestä tai useammasta RDL-elementistä. Kun taas RDL-elementti koostuu sen tietotyypistä ja kardinaalisuudesta. Elementti voi olla yksinkertainen tai monimutkainen. Yksinkertaisella elementillä ei ole alielementtejä tai attribuutteja, kun taas monimutkaisilla elementeillä on lapsia ja valinnaisia attribuutteja.

## RDL XML Schema Definition
XML Schema Definition (XSD) -tiedosto vahvistaa RDL-tiedoston. Kaava määrittelee säännöt, joissa RDL-elementit voivat esiintyä .rdl-tiedostossa. RDL-elementti voi olla yksinkertainen tai monimutkainen. Yksinkertaisella elementillä ei ole alielementtejä tai -attribuutteja, ja monimutkaisilla elementeillä on lapsia ja valinnaisesti attribuutteja.

## RDL:n luominen
Koska RDL on luonteeltaan avoin ja laajennettavissa, voidaan rakentaa monia sovelluksia ja työkaluja, jotka luovat RDL-tiedostoja sen XML-skeeman perusteella. Yksi yksinkertaisimmista tavoista luoda RDL sovelluksesta on käyttää Microsoft .NET Framework -luokkia **System.Xml**-nimiavaruudessa ja System.Linq-nimiavaruudessa. Erityisesti **XmlTextWriter**-luokkaa voidaan käyttää RDL:n kirjoittamiseen. Voit luoda täydellisen raportin määrittelyn alusta loppuun missä tahansa .NET Framework -sovelluksessa käyttämällä **XmlTextWriter** -ohjelmaa. Kehittäjät voivat myös lisätä mukautettuja raporttikohteita mukautetuilla ominaisuuksilla laajentaakseen RDL:ää.

## RDL-tyypit
Seuraavassa taulukossa on lueteltu RDL-elementeissä käytetyt tyypit ja attribuutit.

|Tyyppi|Kuvaus|
---|---|
|Binaari |Ominaisuus, jonka kanta-64-koodattu binääriarvo.|
|Boolean| Ominaisuus, jonka kohteen arvo on tosi tai epätosi. Ellei toisin mainita, pois jätetyn valinnaisen Boolen objektin arvo on False.|
|Date	|A property with a fully specified date or datetime value specified in ISO8601 date format: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Ominaisuus, jonka merkkijonotekstiarvo on oltava yksi määritettyjen arvojen luettelosta.|
|Kellua |Kiinteistö, jolla on kelluva arvo. Pistettä (.) käytetään valinnaisena desimaalierottimena.|
|Integer |Ominaisuus, jonka arvo on kokonaisluku (int32).|
|Language |Ominaisuus, jonka tekstiarvo sisältää kieli- ja kulttuurikoodin, kuten en-us Yhdysvaltain englannin kielellä. Arvon on oltava joko tietty kieli tai neutraali kieli, jolle oletuskieli on määritetty Microsoft .NET Frameworkissa.|
|Nimi |Ominaisuus, jolla on merkkijonotekstiarvo. Nimien on oltava yksilöllisiä kohteen nimiavaruudessa. Jos sitä ei ole määritetty, kohteen nimiavaruus on sisin sisältävä objekti, jolla on nimi.|
|NormalizedString |Ominaisuus, jonka merkkijonotekstiarvo on normalisoitu.|
|Koko |Kokoelementin tulee sisältää numero (ja pistemerkkiä käytetään valinnaisena desimaalierottimena). Numeron perässä on oltava CSS-pituusyksikön tunnus, kuten cm, mm, in, pt tai pc. Välilyönti numeron ja tunnuksen välissä on valinnainen. Lisätietoja kokomerkinnöistä on kohdassa CSS-arvojen ja yksiköiden viite. RDL:ssä koon enimmäisarvo on 160 tuumaa. Pienin koko on 0 tuumaa.|
|String |Ominaisuus, jolla on merkkijonotekstiarvo.|
|UnsignedInt |Ominaisuus, jolla on etumerkitön kokonaisluku (uint32).|
|Variant |Ominaisuus missä tahansa yksinkertaisessa XML-tyypissä.|

## RDL-tietotyypit
RDL:ssä DataType Enumeration määrittää attribuutin, lausekkeen tai parametrin tietotyypin. Seuraava taulukko näyttää, kuinka CLR-tietotyypit vastaavat RDL-tietotyyppejä.

|CLR-tyyppi(t) |Vastaava tietotyyppi|
---|---|
|Boolean| Boolen|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, tavu, SByte |Kokonaisluku|
|Single, Double |Float|
|merkkijono, merkki, GUID, aikaväli | merkkijono|


## Viitteet ##

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

