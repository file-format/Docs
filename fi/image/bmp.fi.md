{
  "date": "2019-10-11",
  "keywords": [
"bmp tiedosto",
"bmp tiedostomuoto",
"mikä on bmp-tiedosto",
"tiedosto",
"bmp esimerkki",
"bmp tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BMP - Kuvatiedostomuoto",
  "description": "Opi BMP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BMP-tiedostoja.",
  "linktitle": "BMP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-bm-fip"
}
},
  "lastmod": "2019-09-10"
}

# Mikä on BMP-tiedosto? #

Tiedostot, joiden tunniste on .BMP, edustavat bittikarttakuvatiedostoja, joita käytetään bittikarttojen digitaalisten kuvien tallentamiseen. Nämä kuvat ovat näytönohjaimesta riippumattomia, ja niitä kutsutaan myös laiteriippumattomiksi bittikarttatiedostomuodoiksi (DIB). Tämä riippumattomuus palvelee tiedoston avaamista useilla alustoilla, kuten Microsoft Windows ja Mac. BMP-tiedostomuoto voi tallentaa tietoja kaksiulotteisina digitaalisina kuvina sekä yksivärisinä että värillisinä eri värisyvyyksineen.

## BMP-tiedostomuodon tekniset tiedot ##

Laitteesta riippumattomat bittikartat toimivat apuvälineenä bittikarttojen vaihtamisessa laitteiden ja sovellusten välillä. Tämän tiedostomuodon jatkuvan kehityksen vuoksi otsikoiden sisältämät tiedot voivat olla erilaisia Bitmap-version mukaan. Yksi bittikarttatiedosto koostuu kiinteistä sekä muuttuvan kokoisista rakenteista tietyssä järjestyksessä.

Bitmap-tiedoston rakenteet on järjestetty seuraavassa järjestyksessä:


|Rakenne|Valinnainen|Koko|Tarkoitus
---|---|---|---|
|Tiedoston otsikko|Ei|14|Tallenna yleisiä tietoja bittikarttakuvatiedostosta
|DIB-otsikko|Ei|Kiinteä koko| Yksityiskohtaisten tietojen tallentamiseen bittikarttakuvasta ja pikselimuodon määrittämiseen
|Extra Bit Masks|Kyllä|12 tai 16 tavua|Pikselimuodon määrittäminen
|Väripaletti|Puolivalinnainen|Vaihteleva koko|Määrittää bittikarttakuvatietojen käyttämät värit
|Auko1|Kyllä|Vaihtuvakokoinen|Rakenteen kohdistus
|Pixel Array|No|Variable-size|Pixel-muoto määritellään DIB-otsikossa tai Extra bit maskeissa.
|Auko2|Kyllä|Vaihtuvakokoinen|Rakenteen kohdistus
|ICC Color profile|Yes|Variable-size|Määrittää väriprofiilin värinhallintaa varten

Kun bittikarttakuva ladataan muistiin, siitä tulee DIB-rakenne, jota Windows käyttää GDI API:n kautta. Tiedoston otsikko ei ole osa tätä tietorakennetta. Väri voi koostua myös 16-bittisistä merkinnöistä, jotka muodostavat indeksejä tällä hetkellä viitattuun palettiin eksplisiittisten RGB-värimääritelmien sijaan. Katsotaanpa joitain näistä yksityiskohtaisesti, erityisesti otsikoita.

### Bittikarttatiedoston otsikko ###

Bitmap-tiedoston otsikko on samanlainen kuin muut tiedostotunnisteet, joita käytetään tiedoston tunnistamiseen. Koska BMP-tiedostomuodosta on erilaisia muunnelmia, BMP-tiedostomuodon 2 ensimmäistä tavua ovat merkki B ja sitten merkki M ASCII-koodauksessa. Kaikki kokonaislukuarvot tallennetaan little-endian-muodossa.

|Offset hex|Offset dec|Koko|Tarkoitus
---|---|---|---|
|00|0|2 bytes|The header field used to identify the BMP and DIB file is 0x42 0x4D in hexadecimal, same as BM in ASCII. It can following possible values.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – OS/2-rakennebittikarttataulukko * **CI** – OS/2-rakenteen värikuvake * **CP** – OS/2-väriosoitin * **IC** – OS/2-rakennekuvake * **PT** – OS/2-osoitin
|02|2|4 tavua|BMP-tiedoston koko tavuina
|06|6|2 tavua|Varattu; todellinen arvo riippuu kuvan luovasta sovelluksesta
|08|8|2 tavua|Varattu; todellinen arvo riippuu kuvan luovasta sovelluksesta
|0A|10|4 tavua|Siirtymä eli aloitusosoite tavusta, josta bittikarttakuvadata (pikselimatriisi) löytyy.

#### DIB-otsikko (bittikarttatietojen otsikko) ####

Yksityiskohtaiset tiedot kuvasta esitetään tässä otsikossa. Näiden tietojen perusteella määritetään sovellus, jota käytetään kuvan näyttämiseen näytöllä. Kaikki tällaiset otsikot sisältävät DWORD-kentän (32-bittinen), joka määrittää niiden koon, jotta sovellus voi helposti määrittää kuvassa käytetyn otsikon. Tämä johtuu pohjimmiltaan siitä, että DIB-muotoon on tehty useita laajennuksia. Seuraavassa on DIB-otsikko lueteltuine kenttineen.

#### Väripaletti ####

BMP-väripaletti on joukko rakenteita, jotka määrittävät kunkin värin RGB-intensiteettiarvot näyttölaitteen väripaletissa. Jokainen bittikarttatietojen pikseli tallentaa yhden arvon, jota käytetään indeksinä väripalettiin. Indeksin elementtiin tallennetut väritiedot määrittävät kyseisen pikselin värin. Värien saatavuus bittikarttatiedostossa vaihtelee seuraavasti:

* Yksi-, 4- ja 8-bittinen – oletetaan aina sisältävän väripaletin

* Kuusitoista, 24 ja 32-bittinen - eivät koskaan sisällä väripaletteja

* Kuusitoista ja 32-bittiset BMP-tiedostot - sisältävät bittikenttien peitearvot väripaletin sijasta


#### Pixel Storage ####

Bittikarttapikselit tallennetaan riveihin pakattuina bitteinä, joissa kunkin rivin koko pyöristetään 4 tavun kerrannaiseksi (32-bittinen DWORD) täyttämällä. Kuvan pikselien tallentamiseen tarvittavien tavujen kokonaismäärää ei voida suoraan laskea laskemalla vain bitit. Koska kyseessä on täyttö, tarvitaan jokaisen rivin koon pyöristäminen 4 tavun kerrannaiseksi. Täytetavut (ei välttämättä 0) on liitettävä rivien loppuun, jotta rivien pituus kasvaa neljän tavun kerrannaisiksi. Kun pikseliryhmä ladataan muistiin, jokaisen rivin tulee alkaa muistiosoitteesta, joka on neljän kerrannainen.

Kuvaa kuvaa itse asiassa pikselitaulukon 32-bittinen DWORD-esitys. Yleensä pikselit tallennetaan alhaalta ylös alkaen vasemmasta alakulmasta, siirtyen vasemmalta oikealle ja sitten rivi riviltä alhaalta ylös. Pikselimuodot ja niiden vaikutukset on lueteltu alla:

* 1-bit per pixel (1bpp) -muoto tukee kahta eri väriä (esimerkiksi: musta ja valkoinen).

* 2-bitt per pixel (2bpp) -muoto tukee 4 erilaista väriä ja tallentaa 4 pikseliä 1 tavua kohden, vasemmanpuoleisin pikseli on kahdessa merkittävimmässä bitissä. Jokainen pikseliarvo on 2-bittinen indeksi enintään 4 värin taulukkoon.

* 4 bitt per pixel (4bpp) -muoto tukee 16 erilaista väriä ja tallentaa 2 pikseliä 1 tavua kohden, vasemmanpuoleisin pikseli on merkittävämmässä nibblessä. Jokainen pikseliarvo on 4-bittinen indeksi enintään 16 värin taulukkoon.

* 8-bitt per pixel (8bpp) -muoto tukee 256 erilaista väriä ja tallentaa 1 pikselin 1 tavua kohden. Jokainen tavu on indeksi enintään 256 värin taulukkoon.

* 16 bitt per pixel (16 bpp) -muoto tukee 65 536 eri väriä ja tallentaa 1 pikselin 2-tavuista WORDia kohden. Jokainen WORD voi määrittää pikselin alfa-, puna-, vihreä- ja sininen näytteet.

* 24-bittinen pikselimuoto (24 bpp) tukee 16 777 216 eri väriä ja tallentaa 1 pikselin arvon 3 tavua kohti. Jokainen pikseliarvo määrittää pikselin punaisen, vihreän ja sinisen näytteen (8.8.8.0.0 RGBAX-merkinnällä). Tarkemmin sanottuna järjestyksessä: sininen, vihreä ja punainen (8 bittiä jokaista näytettä kohti).

* 32-bittinen pikseliä kohden (32bpp) -muoto tukee 4 294 967 296 eri väriä ja tallentaa yhden pikselin 4-tavuista DWORDia kohden. Jokainen DWORD voi määrittää pikselin alfa-, punainen-, vihreä- ja sininennäytteet.


## Viitteet ##

* [Windows MetaFile Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [BMP-tiedostomuoto](https://en.wikipedia.org/wiki/BMP_file_format)


