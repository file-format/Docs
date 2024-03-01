{
  "date": "2020-03-16",
  "keywords": [
"IFC tiedosto",
"Muoto",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi IFC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata IFC-tiedostoja.",
  "title": "IFC tiedostomuoto",
  "linktitle": "IFC",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-if-fic"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on IFC-tiedosto?

IFC-laajennuksella varustetut tiedostot viittaavat Industry Foundation Classes (IFC) -tiedostomuotoon, joka määrittää kansainväliset standardit rakennusobjektien ja niiden ominaisuuksien tuontia ja vientiä varten. Tämä tiedostomuoto tarjoaa yhteentoimivuuden eri ohjelmistosovellusten välillä. BuildingSMART International kehittää ja ylläpitää tämän tiedostomuodon tekniset tiedot tietostandardinaan. IFC-tiedostomuodon perimmäisenä tavoitteena on parantaa viestintää, tuottavuutta, toimitusaikoja ja laatua rakennuksen koko elinkaaren ajan.

Rakennusteollisuuden yleisille kohteille vakiintuneiden standardien ansiosta se vähentää tiedon menetystä siirrettäessä sovelluksesta toiseen. IFC voi sisältää tietoja geometriasta, laskennasta, määristä, kiinteistönhallinnasta, hinnoittelusta jne. useille eri ammattialoille (arkkitehti, sähkö, LVI, rakenne, maasto jne.).

## Lyhyt historia ##

Autodesk teki IFC-aloitteen vuonna 1994 tukeakseen integroitua sovelluskehitystä, ja siihen kuului muun muassa Honeywell, Butler Manufacturing ja AT&T. Vuonna 1995 jäsenyys avattiin kaikille ja nimi muutettiin International Alliance for Interoperability -järjestöksi. Voittoa tavoittelemattoman järjestön tarkoituksena oli julkaista Industry Foundation Class (IFC) AEC-tuotemallina. Vuonna 2005 nimi muutettiin jälleen, ja buildSMART ylläpitää sitä nyt.

## IFC-tiedostomuoto ##

The IFC file format has undergone several changes over the past to reach the file format specifications v4. Ajoittain tapahtui useita pieniä muutoksia, jotka on sisällytetty spesifikaatioihin lisäyksinä. Seuraavassa on luettelo eri versioista tiedostomäärityksistä, jotka on julkistettu aiemmin.

* IFC4 Add2 (2016)IFC4 Add1 (2015)

* IFC4 (maaliskuu 2013) ifcXML2x3 (kesäkuu 2007)

* IFC2x3 (helmikuu 2006) ifcXML2 for IFC2x2 add1 (RC2)

* IFC2x2 Addendum 1 (heinäkuu 2004) ifcXML2 for IFC2x2 (RC1)

* IFC 2x2IFC 2x Addendum 1ifcXML1 IFC2x:lle ja

* IFC2x-lisäys 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5


Viimeisimmät versiot IFC-tiedostomuotomäärityksistä ovat aina saatavilla buildingSMART-verkkosivustolla, ja kehittäjän tulee tutustua niihin kaikentyyppisissä sovelluksissa, joita he aikovat kehittää. Tätä artikkelia kirjoitettaessa version 4 tekniset tiedot ovat uusimmat saatavilla verkossa.

### IFC-tietotiedostomuodot ###

IFF-tiedostomuoto tukee tiedonvaihtoa sovellusten välillä käyttämällä eri muotoja, kuten alla on lueteltu:

**IFC:**  This is the default IFC exchange format and uses the STEP physical file structure according to ISO 10303-21. Tällä tiedostomuodolla on .ifc-tiedostotunniste, ja se on eniten käytetty IFC-muoto.

**IFC-XML:** Se on IFC:n XML-tiedostomuotoinen versio, jonka lähettävä sovellus voi luoda suoraan ISO 10303-28 -rakenteen mukaisesti, jota kutsutaan myös STEP-XML:ksi. IFC-XML-tiedostomuotoa pidetään sopivana XML-työkalujen yhteentoimivuuteen. Verrattuna IFC-tiedostomuotoon, IFC-XML on kooltaan 300-400 % suurempi.

**IFC-ZIP:** Se on [ZIP](/compression/zip/)-pakattu IFC- tai IFC-XML-versio, jossa yksi näistä tiedostoista on zip-arkiston päähakemisto. Tämä muoto pakkaa .ifc-tiedoston 60-80 % ja .ifc XML-tiedoston 90-95 %.

### IFC-arkkitehtuuri ###

IFC-spesifikaatio sisältää termejä, käsitteitä ja dataspesifikaatioita, jotka ovat peräisin rakennus- ja kiinteistöalan tieteenalojen, ammattien ja ammattien käytöstä. Termit ja käsitteet käyttävät yksinkertaisia englanninkielisiä sanoja, tietomäärittelyn tietokohteet noudattavat nimeämiskäytäntöä.

tyyppien, entiteettien, sääntöjen ja funktioiden tietokohteiden nimet alkavat etuliitteellä Ifc ja jatkuvat englanninkielisillä sanoilla CamelCasen nimeämiskäytännössä (ei alaviivaa, sanan ensimmäinen kirjain isoilla kirjaimilla); entiteetin attribuuttien nimet noudattavat CamelCasen nimeämiskäytäntöä ilman etuliitettä; ominaisuusjoukon määritelmät, jotka ovat osa tätä standardia, alkavat etuliitteellä Pset_ ja jatkuvat englanninkielisillä sanoilla CamelCasen nimeämiskäytännössä; tähän standardiin kuuluvat määräjoukon määritelmät alkavat etuliitteellä Qto_ ja jatkuvat englanninkielisillä sanoilla CamelCasen nimeämiskäytännössä.

IFC:n tietoskeema-arkkitehtuuri määrittelee neljä käsitteellistä kerrosta, joista kukin yksittäinen skeema on määritetty täsmälleen yhdelle käsitteelliselle tasolle.

**Resurssikerros** — alin kerros sisältää kaikki yksittäiset resurssimääritelmät sisältävät skeemat. Nämä määritelmät eivät sisällä maailmanlaajuisesti yksilöivää tunnistetta, eikä niitä saa käyttää ylemmän kerroksen määritelmistä riippumatta.

**Ydinkerros** — seuraava kerros sisältää ytimen skeeman ja ydinlaajennusskeemat, jotka sisältävät yleisimmät entiteettimääritykset. Kaikilla ydinkerroksessa tai ylemmällä määritellyillä entiteetillä on globaalisti yksilöllinen tunnus ja valinnaisesti omistaja- ja historiatiedot.

**Yhteentoimivuuskerros** — seuraava kerros sisältää skeemoja, jotka sisältävät kokonaisuuden määritelmiä, jotka ovat ominaisia yleiselle tuotteelle, prosessille tai resurssien erikoistumiselle, jota käytetään useilla eri aloilla. Näitä määritelmiä käytetään tyypillisesti toimialueiden väliseen vaihtoon ja rakennustietojen jakamiseen.

**Domain-kerros** — ylin kerros sisältää skeemoja, jotka sisältävät entiteettimääritelmiä, jotka ovat tietylle tieteenalalle spesifisiä tuotteiden, prosessien tai resurssien erikoisuuksia. Näitä määritelmiä käytetään tyypillisesti verkkotunnuksen sisäiseen vaihtoon ja tiedon jakamiseen.

## Viitteet ##

* [Industry Foundation Classes - Wikipedia](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)


