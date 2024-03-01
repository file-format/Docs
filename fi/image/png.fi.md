{
  "date": "2019-10-11",
  "keywords": [
"png-tiedosto",
"png-tiedostomuoto",
"mikä on png-tiedosto",
"tiedosto",
"png esimerkki",
"png tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PNG-tiedostomuoto - rasterikuvatiedosto",
  "description": "Opi PNG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PNG-tiedostoja.",
  "linktitle": "PNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pn-fig"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on PNG-tiedosto?

**PNG** (Portable Network Graphics) -tiedosto on rasterikuvatiedostomuoto, joka käyttää häviötöntä pakkausta. Tämä tiedostomuoto luotiin Graphics Interchange Formatin ([GIF](/image/gif/)) korvaamiseksi, eikä sillä ole tekijänoikeusrajoituksia. PNG-tiedostomuoto ei kuitenkaan tue animaatioita. PNG-tiedostomuoto tukee häviötöntä kuvanpakkausta, mikä tekee siitä suositun käyttäjiensä keskuudessa. Ajan myötä PNG on kehittynyt yhdeksi laajalti käytetyistä kuvatiedostomuodoista.

## PNG-tiedostomuodon lyhyt historia

The main reason behind the creation of PNG file format was the patented compression algorithm, Lempel-Ziv-Welch, used in the GIF file format. This along with other GIF limitations created a need for replacement of [**GIF**](/image/gif/) file format. The first proposal and name for PNG file format came in January 1995. Alla on lueteltu tärkeimmät PNG-tiedostomuotoihin liittyvät tapahtumat:

* Lokakuu 1996: PNG-spesifikaatioiden versio 1.0 julkaistiin ja ilmestyi myöhemmin nimellä [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Siitä tuli W3C-suositus lokakuussa 1996.

* Joulukuu 1998: Versio 1.1, jossa oli pieniä muutoksia ja lisätty kolme uutta osaa, julkaistiin.

* Elokuu 1999: Versio 1.2, johon lisättiin yksi ylimääräinen osa, julkaistiin.

* Marraskuu 2003: PNG:stä tuli kansainvälinen standardi (ISO/IEC 15948:2003). Tämä PNG-versio eroaa vain vähän versiosta 1.2, eikä se lisää uusia paloja.

* Maaliskuu 2004: ISO/IEC 15948:2004


## GIF:n ja PNG:n toiminnallinen vertailu

PNG-tiedostomuoto on suunniteltu yksinkertaiseksi ja kannettavaksi, laillisesti rasittamattomaksi, vaihdettavaksi, joustavaksi ja kestäväksi. Seuraavassa taulukossa luetellaan PNG-tiedostomuodon perimät GIF-ominaisuudet uusien ominaisuuksien lisäksi.

|Ominaisuus|GIF|PNG|
---|---|---|
|Indeksivärikuvat jopa 256 värillä|Kyllä|Kyllä|
|Suoratoiston tuki|Kyllä|Kyllä|
|Avoimuus|Kyllä|Kyllä|
|Lisätiedot|Kyllä|Kyllä|
|Laitteisto- ja alustariippumattomuus|Kyllä|Kyllä|
|Tehokas|Kyllä|Kyllä|
|Truecolor-kuvat jopa 48 bittiä pikseliä kohden|Ei|Kyllä|
|Harmaasävykuvat jopa 16 bittiä/pikseli|Ei|Kyllä|
|Täysi alfakanava (yleiset läpinäkyvyysmaskit)|Ei|Kyllä|
|Kuvan gammatiedot|Ei|Kyllä|
|Luotettavuus|Ei|Kyllä|
|Nopeampi alkuesitys|Ei|Kyllä|

## PNG-tiedostorakenne

Lähes kaikki käyttöjärjestelmät tukevat PNG-tiedostojen avaamista. Esimerkiksi Microsoft Windows Viewer pystyy avaamaan PNG-tiedostoja, koska käyttöjärjestelmällä on oletusarvoisesti tuki, joka on saatavana osana asennusta. PNG-tiedosto koostuu PNG allekirjoituksesta, jota seuraa sarja //chunks//.

### PNG-tiedoston otsikko

PNG-tiedoston ensimmäiset kahdeksan tavua sisältävät aina seuraavat (desimaali)arvot:

{{{137 80 78 71 13 10 26 10 }}}

Tämä allekirjoitus osoittaa, että tiedoston loppuosa sisältää yhden PNG-kuvan, joka koostuu sarjasta paloja, jotka alkavat IHDR-kappaleeseen ja päättyvät IEND-kappaleeseen.

### Palat ###

Jokainen pala koostuu neljästä osasta:

**Pituus:** 4-tavuinen etumerkitön kokonaisluku, joka ilmaisee tavujen määrän osan tietokentässä. Pituus laskee vain tietokentän, ei itseään, palatyypin koodia tai CRC:tä. Nolla on kelvollinen pituus. Vaikka kooderien ja dekooderien tulisi käsitellä pituutta etumerkittömänä, sen arvo ei saa ylittää 231 tavua.

**Chunk Type:** A 4-byte chunk type code. For convenience in description and in examining PNG files, type codes are restricted to consist of uppercase and lowercase ASCII letters (A-Z and a-z, or 65-90 and 97-122 decimal). However, encoders and decoders must treat the codes as fixed binary values, not character strings. For example, it would not be correct to represent the type code IDAT by the EBCDIC equivalents of those letters. Additional naming conventions for chunk types are discussed in the next section.

**Chunk Data:** Tietotavut, jotka vastaavat kappaletyyppiä, jos sellaisia on. Tämän kentän pituus voi olla nolla.

**CRC:** 4-tavuinen CRC (Cyclic Redundancy Check), joka lasketaan kappaleen edeltävistä tavuista, mukaan lukien kappaleen tyyppikoodi ja osatietokentät, mutta ei pituuskenttää. CRC on aina läsnä, myös osissa, jotka eivät sisällä tietoja.

Osan datan pituus voi olla mikä tahansa tavumäärä enimmäismäärään asti; siksi toteuttajat eivät voi olettaa, että palot on kohdistettu tavua suurempiin rajoihin.

Palat voivat näkyä missä tahansa järjestyksessä kullekin palatyypille asetettujen rajoitusten mukaisesti. (Yksi huomionarvoinen rajoitus on, että IHDR:n on näytettävä ensimmäisenä ja IEND:n on oltava näkyvissä viimeisenä; näin ollen IEND-kappale toimii tiedoston lopun merkkinä.) Useita samantyyppisiä paloja voi esiintyä, mutta vain, jos se on nimenomaisesti sallittu kyseiselle tyypille.

#### Palatyypit

Osatyypit luokitellaan **Kriittisiksi** ja **Lisäosiksi** lohkotyypeille määritetyn 4-tavun isot ja pienet kirjaimet huomioiden ASCII-arvon perusteella. Kaikkien toteutusten on ymmärrettävä ja suoritettava onnistuneesti standardit kriittiset palat. Kelvollisen PNG-kuvan tulee sisältää IHDR-kappale, yksi tai useampi IDAT-kappale ja IEND-osa.

### Puristus

PNG-pakkausmenetelmä 0 (ainoa tällä hetkellä PNG:lle määritetty pakkausmenetelmä) määrittää deflate/täytepakkauksen, jonka liukuikkuna on enintään 32768 tavua. Deflate-pakkaus on LZ77-johdannainen, jota käytetään zip-, gzip-, pkzip- ja vastaavissa ohjelmissa. Sen patenttivapaata asemaa on tuettu laajasti. Pakatut tiedot zlib-tietovirran sisällä tallennetaan sarjana lohkoja, joista jokainen voi edustaa raakadataa (pakkaamatonta), LZ77-pakattua dataa, joka on koodattu kiinteillä Huffman-koodeilla, tai LZ77-pakattua dataa, joka on koodattu mukautetuilla Huffman-koodeilla. Viimeisessä lohkossa oleva merkkibitti tunnistaa sen viimeiseksi lohkoksi, jolloin dekooderi voi tunnistaa pakatun tietovirran lopun.

#### Esipakkaussuodatus

Esipakkaussuodattimia käytetään kuvatietojen valmistelemiseksi optimaalista pakkausta varten. PNG-suodatinmenetelmä määrittelee viisi perussuodatintyyppiä seuraavasti:

|Suodattimen tyyppi|Nimi|Ennustettu arvo|
---|---|---|
|0|Ei mitään|Skannausviiva lähetetään muokkaamattomana|
|1|Sub|Lähettää kunkin tavun ja edellisen pikselin vastaavan tavun arvon välisen eron.|
|2|Ylös|Ylös()-suodatin on aivan kuten Sub()-suodatin, paitsi että pikseliä, joka on välittömästi nykyisen pikselin yläpuolella, eikä vain sen vasemmalla puolella, käytetään ennustajana.|
|3|Keskiarvo|Keskiarvo()-suodatin käyttää kahden vierekkäisen pikselin (vasemmalla ja yläpuolella) keskiarvoa pikselin arvon ennustamiseen.|
|4|Paeth|Paeth()-suodatin laskee yksinkertaisen lineaarifunktion kolmesta vierekkäisestä pikselistä (vasemmalla, yläpuolella, ylhäällä vasemmalla) ja valitsee sitten ennustajaksi naapuripikselin, joka on lähinnä laskettua arvoa.|

Suodatusalgoritmeja sovelletaan tavuihin, ei pikseleihin, kuvan bittisyvyydestä tai värityypistä riippumatta. Suodatusalgoritmit toimivat skannausviivan muodostamassa tavusekvenssissä. Jos kuva sisältää alfakanavan, alfa-data suodatetaan samalla tavalla kuin kuvadata.

Kun kuva on lomitettu, kutakin lomituskuvion kulkua käsitellään itsenäisenä kuvana suodatustarkoituksiin. Suodattimet toimivat tavusarjoissa, jotka muodostuvat todellisuudessa läpikulun aikana lähetetyistä pikseleistä, ja edellinen skannausviiva on se, joka on aiemmin lähetetty samalla passilla, ei koko kuvan vieressä oleva. Huomaa, että yhdellä siirrolla lähetetty osakuva on aina suorakaiteen muotoinen, mutta sen leveys ja/tai korkeus on pienempi kuin koko kuva. Suodatusta ei käytetä, kun tämä alakuva on tyhjä.

## Viitteet ##

* [PNG - Kotisivu](http://www.libpng.org/pub/png/)


