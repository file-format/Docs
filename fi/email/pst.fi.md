{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PST - Outlook Personal Information Store -tiedostomuoto",
  "description": "Opi PST-tiedostomuodosta ja API:ista, jotka voivat luoda ja avata PST-tiedostoja.",
  "linktitle": "PST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ps-fit"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on PST-tiedosto?

Tiedostot, joissa on .pst-tunniste, edustavat Outlookin henkilökohtaisia tallennustiedostoja (kutsutaan myös henkilökohtaiseksi tallennustaulukoksi), jotka tallentavat erilaisia käyttäjätietoja. Käyttäjätiedot tallennetaan erityyppisiin kansioihin, jotka sisältävät sähköpostiviestejä, kalenterimerkintöjä, muistiinpanoja, yhteystietoja ja useita muita tiedostomuotoja. PST-tiedostoja käytetään sähköpostitietojen arkistointiin offline-tilassa, jotka voidaan myöhemmin ladata ja tarkastella eri sovelluksissa.

## PST-tiedostomuodon tekniset tiedot

PST-tiedostomuoto [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) on saatavana Microsoftilta ilmaisina ja peruuttamattomina ilmaisina patenttilisenssinä Open Specification Promisen kautta.

### PST-muotojen tyyppi

PST-tiedostomuodot luokitellaan kahteen tyyppiin tiedostotyypin koodauksen perusteella. ANSI-koodatut PST-tiedostot ovat vanhempia tiedostomuotoja, ja vain Outlook 2002 ja aiemmat versiot tukevat niitä. Tällaisten tiedostojen enimmäiskoko on 2 Gt (2^^31^^ tavua), eivätkä ne tue Unicodea. Nykyaikaisempi tiedostomuoto, joka perustuu Unicode-koodaukseen, poistaa tiedostokokorajoituksen ja voi saavuttaa 50 Gt:n enimmäistietokoon.

### PST-tiedostomuodon looginen organisaatio

PST-tiedostomuodon pohjalla on B-Tree, joka pitää tiedot lajiteltuina ja mahdollistaa haut, peräkkäisen käytön, lisäykset, poistot jne. logaritmisajassa. PST-tiedoston yleinen rakenne on järjestetty kolmeen kerrokseen.

!{{HYPERLINKKI1}}

Solmutietokanta (NDB) Layer - Solmutietokantakerros sijaitsee PST-tiedoston alemmalla tasolla ja sisältää solmutietokannan. Nämä solmut edustavat itse asiassa PST-tiedostomuodon alemman tason tallennustiloja. NDB-kerros koostuu otsikoista, tiedostojen allokaatiotiedoista, lohkoista ja BT-puuista (Node BTree ja Block BTree) tallennuksen näkökulmasta. NDB-kerroksen solmut ja lohkot linkitetään Data BID:n kautta, joka on yksi neljästä solmuviittauksen ominaisuudesta eli NID (Node ID), Parent NID, Data BID (Block BID) ja SubNode BID.

`Listat, taulukot ja ominaisuustaso -` LTP-kerros tarjoaa loogisen ymmärryksen korkeamman tason käsitteistä NDB:n päällä. Muiden elementtien lisäksi LTP-kerros koostuu pääasiassa Property Contextistä (PC) ja Table Contextistä (TC). PC on kokoelma ominaisuuksia, kun taas TC edustaa kaksiulotteista matriisia ominaisuuksien kokoelmasta vs. näiden olemassaolosta. Tehokas PC- ja TC-toteutus, LTP-kerros käyttää seuraavia kahden tyyppisiä tietorakenteita NDB-solmun päällä:

* Heap On Node (HN) - mahdollistaa solmun datavirran aliallokoinnin pieniksi, muuttuvan kokoisiksi fragmenteiksi.

* BTree on Heap (BTH) - BTH tarjoaa kätevän ja käytännöllisen tavan etsiä data-PC:t, jotka on kuvattu yllä, on toteutettu BTH:ina ja siksi se toteutetaan rakentamalla HN-rakenteen sisään.


`Viestikerros -` Korkeamman tason säännöt ja liiketoimintalogiikka PST-tiedostojen kanssa työskentelyyn on toteutettu tässä tasossa. Tämän kerroksen looginen tulos on kansioobjekteja, viestiobjekteja, liiteobjekteja ja ominaisuuksia, mikä on mahdollista yhdistämällä LTP- ja NDB-kerrokset. Säännöt ja vaatimukset, joita on noudatettava PST-sisällön muuttamisessa, määritellään myös tässä tasossa.

### PST-tiedostomuodon fyysinen organisaatio

PST-tiedoston korkeatasoinen tiedostojärjestely on alla olevan kuvan mukainen. Tämä on vain yleiskatsaus eri käsitteistä PST-tiedoston loogisista elementeistä.

!{{HYPERLINKKI1}}


#### PST-otsikon tiedot

PST-tiedoston HEADER-rakenne sijaitsee aivan tiedoston alussa 0-siirrossa. Se sisältää metatietotiedot PST-tiedostosta ja ROOT-tiedot edellä kuvattujen NDB-kerroksen tietorakenteiden käyttämiseksi. HEADER-rakenne eroaa PST-tiedostomuodon Unicode- ja ANSI-versioissa.

Otsikko alkaa 4-tavuisella taikasanalla **!BDN**, jota edustavat tavut (0x21, 0x42, 0x44, 0x4E). Toinen 2-tavuinen maaginen numero, **SM** (0x53, 0x4D), sijaitsee offsetissa 8 tiedoston alusta. Versiotiedot (ANSI tai Unicode) ovat 10:n siirrossa tiedoston alusta. Hex-arvo (0x17) määrittää Unicode-PST-tiedoston, kun taas 0x0E tai 0x0F edustaa ANSI-tiedostomuotoa.

|Kenttä|Kuvaus
---|---|
|dwMagic (4 tavua)|PITÄÄ olla { 0x21, 0x42, 0x44, 0x4E } (!BDN)
|dwCRCPartial (4 tavua)|471 tavun datan 32-bittinen CRC-arvo alkaen wMagicClient-sovelluksesta (0ffset 0x0008)
|wMagicClient (2 tavua)|PITÄÄ olla { 0x53, 0x4D }.
|wVer (2 tavua)|Tiedostomuotoinen versio. Tämän arvon PITÄÄ olla 14 tai 15, jos tiedosto on ANSI PST-tiedosto, ja TÄYTYY olla 23, jos tiedosto on Unicode-PST-tiedosto.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. Tähän asiakirjaan perustuvan uuden PST-tiedoston luojien PITÄÄ alustaa tämä arvo arvoon 19.
|bPlatformCreate (1 tavu)|Tämän arvon PITÄÄ asettaa arvoon 0x01.
|bPlatformAccess (1 tavu)|Tämän arvon PITÄÄ asettaa arvoon 0x01.
|dwVarattu (8 tavua)|
|bidUnused (vain 8 tavua Unicode)|Käyttämätön täyte lisättiin, kun Unicode PST -tiedostomuoto luotiin.
|bidNextP (Unicode: 8 tavua; ANSI: 4 tavua)|Seuraava sivu BID. Sivuilla on erityinen laskuri bidIndex-arvojen jakamiseen. Sivujen BID-arvojen bidIndex-arvo allokoidaan tästä laskurista.
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Katso lisätietoja kohdasta 2.2.2.2.
|dwUnique (4 tavua)|Tämä on monotonisesti kasvava arvo, jota muutetaan aina, kun PST-tiedoston HEADER-rakennetta muutetaan. Tämän arvon tehtävänä on tarjota yksilöllinen arvo ja varmistaa, että HEADER CRC:t ovat erilaisia jokaisen otsikon muokkauksen jälkeen.
|rgnid[] (128 tavua)|Kiinteä 32 NID:n joukko, joista kukin vastaa yhtä 32 mahdollisesta NID_TYPE:stä (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_MESSAGE_)
|qwKäyttämätön (8 tavua)|Käyttämätön tila; TÄYTYY asettaa nollaan. Vain Unicode PST -tiedostomuoto.
|juuri (Unicode: 72 tavua; ANSI: 40 tavua)|ROOT-rakenne (osio 2.2.2.5).
|dwAlign (4 tavua)|Käyttämättömät tasaustavut; TÄYTYY asettaa nollaan. Vain Unicode PST -tiedostomuoto.
|rgbFM (128 tavua)|Käytöstä poistettu FMap. Tätä ei enää käytetä, ja se TÄYTYY täyttää arvolla 0xFF. Lukijoiden PITÄÄ jättää huomioimatta näiden tavujen arvo.
|rgbFP (128 tavua)|Käytöstä poistettu FPMap. Tätä ei enää käytetä ja se TÄYTYY täyttää arvolla 0xFF. Lukijoiden PITÄÄ jättää huomioimatta näiden tavujen arvo.
|bSentinel (1 tavu) | PITÄÄ asettaa arvoon 0x80.
|bCryptMethod (1 tavu)|Ilmoittaa kuinka PST-tiedoston tiedot on koodattu. PITÄÄ asettaa johonkin ennalta määritetyistä arvoista (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbVarattu (2 tavua)| Varattu; TÄYTYY asettaa nollaan.
|bidNextB (8 tavua)|Ilmoittaa seuraavan saatavilla olevan BID-arvon. Vain Unicode PST -tiedostomuoto.
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Katso lisätietoja kohdasta 2.2.2.2.
|dwCRCFull (4 tavua)|516 tavun datan 32-bittinen CRC-arvo alkaen wMagicClientistä bidNextB:hen, mukaan lukien. Vain Unicode PST -tiedostomuoto.
|ullVarattu (8 tavua)|Varattu; TÄYTYY asettaa nollaan. Vain ANSI PST -tiedostomuoto.
|dwVarattu (4 tavua)|Varattu; TÄYTYY asettaa nollaan. Vain ANSI PST -tiedostomuoto.
|rgbVarattu2 (3 tavua)|
|bVarattu (1 tavu) |
|rgbVarattu3 (32 tavua) |

### Datan suojelu ###

Turvallisuussyistä PST-tiedostot voidaan myös suojata salasanalla, mikä edellyttää, että lataussovellus käyttää salasanaa ennen kuin niitä voidaan tarkastella. PST-tiedostoon käytetty salasana tallennetaan viestisäilöön. Tämä ei kuitenkaan tarjoa vahvaa tietosuojaa, koska salasana voidaan poistaa käytettävissä olevilla työkaluilla. Myöskään käyttäjän määrittämää salasanaa ei käytetä salausalgoritmien koodaus- ja dekoodausavaimen osana. Siten ei ole mitään hyötyä suojata tietoja luvattomien osapuolten pääsyltä. Salasanan säilyttäminen alkuperäisen merkkijonon CRC-32-hajautusmuodossa tekee siitä myös heikon menetelmän tietoturvaan raakaa voimaa vastaan.

## Viitteet ##

* [Outlook Personal Folders (.pst) -tiedostomuoto](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [Henkilökohtaisen kansion tiedostomuodon tekniset tiedot](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


