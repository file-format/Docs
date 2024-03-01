{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OST - Outlookin tallennustiedostomuoto",
  "description": "Opi OST-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OST-tiedostoja.",
  "linktitle": "OST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-os-fit"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on OST-tiedosto?

OST- tai offline-tallennustiedostot edustavat käyttäjän postilaatikon tietoja offline-tilassa paikallisella koneella rekisteröityessä Exchange Serveriin Microsoft Outlookin avulla. Se luodaan automaattisesti, kun Microsoft Outlookia käytetään ensimmäistä kertaa, kun yhteys palvelimeen on muodostettu. Kun tiedosto on luotu, tiedot synkronoidaan sähköpostipalvelimen kanssa, jotta ne ovat käytettävissä myös offline-tilassa, jos yhteys sähköpostipalvelimeen katkeaa. OST-tiedostot voivat käyttää postilaatikon kohteita, kuten sähköposteja, yhteystietoja, kalenteritietoja, muistiinpanoja, tehtäviä ja muita vastaavia tietoja. Käyttäjät voivat luoda sähköposteja ja muita tietokohteita OST-tiedostoon myös ilman yhteyttä palvelimeen, mutta niitä ei synkronoida palvelimen kanssa. Kun yhteys on muodostettu, paikallinen tiedosto synkronoidaan uudelleen palvelimen kanssa niin, että sekä palvelin että paikallinen kopio ovat samalla tietotasolla.

## OST-tiedostomuoto

The OST (Offline Storage Table) and [PST](/email/pst/) (Personal Storage Table) file format consist of the Personal Folder File (PFF) format that corresponds to storing user's emails, contacts and appointments. Data in a PFF file is stored in little-endian with all dates and times represented as FILETIME in UTC. [MS-PST] defines two types of PFF:

* 32-bittinen ANSI-muoto

* 64-bittinen Unicode-muoto


PST-tiedostomuoto [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), sellaisena kuin se on saatavilla Microsoftilta, soveltuu myös OST-tiedostomuotoon ilmaisena ja peruuttamattomana patenttilisenssinä Open Specification Promisen kautta. Se koostuu seuraavista erotettavissa olevista elementeistä:

* Fle otsikko

* Tiedoston otsikkotiedot

* Indeksin haarasolmu

* Indeksilehtisolmu

* (Tiedosto) offset-indeksi

* (Tuote)kuvaajaindeksi

* Paikalliset kuvaukset

* Tuotetaulukkotyyppi


### Otsikkotiedot

OST-tiedoston HEADER-rakenne sijaitsee aivan tiedoston alussa 0-siirrossa. Se sisältää metatietotiedot OST-tiedostosta ja ROOT-tiedot edellä kuvattujen NDB-kerroksen tietorakenteiden käyttämiseksi. HEADER-rakenne eroaa OST-tiedostomuodon Unicode- ja ANSI-versioissa.

Otsikko alkaa 4-tavuisella taikasanalla **!BDN**, jota edustavat tavut (0x21, 0x42, 0x44, 0x4E). Toinen 2-tavuinen maaginen numero, **SM** (0x53, 0x4D), sijaitsee offsetissa 8 tiedoston alusta. Versiotiedot (ANSI tai Unicode) ovat 10:n siirrossa tiedoston alusta. Hex-arvo (0x17) määrittää Unicode-OST-tiedoston, kun taas 0x0E tai 0x0F edustaa ANSI-tiedostomuotoa.

|Kenttä|Kuvaus
---|---|
|dwMagic (4 tavua)|PITÄÄ olla { 0x21, 0x42, 0x44, 0x4E } (!BDN)
|dwCRCPartial (4 tavua)|471 tavun datan 32-bittinen CRC-arvo alkaen wMagicClient-sovelluksesta (0ffset 0x0008)
|wMagicClient (2 tavua)|PITÄÄ olla { 0x53, 0x4D }.
|wVer (2 tavua)|Tiedostomuotoinen versio. Tämän arvon PITÄÄ olla 14 tai 15, jos tiedosto on ANSI PST-tiedosto, ja TÄYTYY olla 23, jos tiedosto on Unicode-PST-tiedosto.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. Tähän asiakirjaan perustuvan uuden PST-tiedoston luojien PITÄISI alustaa tämä arvo arvoon 19.
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
|rgbFM (128 tavua)|Käytöstä poistettu FMap. Tätä ei enää käytetä ja se TÄYTYY täyttää arvolla 0xFF. Lukijoiden PITÄÄ jättää huomioimatta näiden tavujen arvo.
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

## Viitteet

* [Outlook Personal Folders (.ost) -tiedostomuoto](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [Henkilökohtaisen kansion tiedostomuodon tekniset tiedot](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


