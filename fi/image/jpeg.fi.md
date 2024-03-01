{
  "date": "2019-11-25",
  "keywords": [
"jpeg tiedosto",
"jpeg tiedostomuoto",
"mikä on jpeg-tiedosto",
"tiedosto",
"jpeg esimerkki",
"jpeg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPEG - Kuvatiedostomuoto",
  "description": "Opi JPEG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JPEG-tiedostoja.",
  "linktitle": "JPEG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jpe-fig"
}
},
  "lastmod": "2020-08-08"
}

## Mikä on JPEG-tiedosto? ##

JPEG on eräänlainen kuvamuoto, joka tallennetaan häviöllisen pakkauksen menetelmällä. Pakkaamisen seurauksena tulostettu kuva on kompromissi tallennuskoon ja kuvanlaadun välillä. Käyttäjät voivat säätää pakkaustasoa halutun laatutason saavuttamiseksi ja samalla pienentää tallennustilaa. Kuvan laatu heikkenee merkityksettömästi, jos kuvaa käytetään 10:1-pakkaussuhteessa. Mitä korkeampi pakkausarvo, sitä enemmän kuvanlaatu heikkenee.

## Tiedostomuodon tiedot ##

Joint Photographic Experts Group on standardoinut JPEG-kuvatiedostomuodon ja tästä syystä nimen JPEG. Formaattina on ollut valokuvakuvien tallentaminen ja siirtäminen verkkoon. Lähes kaikissa käyttöjärjestelmissä on nyt katseluohjelmia, jotka tukevat JPEG-kuvien visualisointia, jotka usein tallennetaan myös JPG-laajennuksella. Jopa verkkoselaimet tukevat JPEG-kuvien visualisointia. Ennen kuin siirryt JPEG-tiedostomuotomäärittelyihin, on mainittava JPEG:n luomiseen liittyvien vaiheiden yleinen prosessi.

### JPEG-pakkausvaiheet ###

**Transformaatio:** Värikuvat muunnetaan RGB:stä luminanssi/krominanssikuvaksi (silmä on herkkä luminanssille, ei krominanssille, joten krominanssiosa voi menettää paljon tietoa ja siten pakata voimakkaasti.

**Alasnäytteistys:** Alasnäytteistys tehdään värilliselle komponentille, ei luminanssikomponentille. Alasnäytteistys tehdään joko suhteessa 2:1 vaakasuunnassa ja 1:1 pystysuunnassa (2h 1 V). Siten kuvan koko pienenee, koska 'y'-komponenttiin ei kosketa, kuvanlaadussa ei ole havaittavissa olevaa heikkenemistä.

**Järjestäminen ryhmiin:** Kunkin värikomponentin pikselit on järjestetty 8 × 2 pikselin ryhmiin, joita kutsutaan tietoyksiköiksi, jos rivien tai sarakkeen lukumäärä ei ole 8:n kerrannainen, alin rivi ja oikeanpuoleiset sarakkeet kopioidaan.

**Diskreetti kosinimuunnos:** Diskreetti kosinimuunnos (DCT) sovelletaan sitten jokaiseen tietoyksikköön 8 × 8 -kartan luomiseksi muunnetuista komponenteista. DCT:hen liittyy jonkin verran tietojen menetystä tietokoneen aritmeettisen tarkkuuden vuoksi. Tämä tarkoittaa, että jopa ilman karttaa kuvanlaatu heikkenee jonkin verran, mutta se on yleensä pieni.

**Kvantisointi:** Jokainen tietoyksikön 64 muunnetusta komponentista jaetaan erillisellä luvulla, jota kutsutaan sen kvantisointikertoimeksi (QC) ja pyöristetään sitten kokonaisluvuksi. Tämä on paikka, jossa tiedot menetetään peruuttamattomasti, suuri laadunvalvonta aiheuttaa enemmän menetyksiä. Yleisesti ottaen useimmat JPEG-laitteet sallivat JPEG-standardin suosittelemien QC-taulukoiden käytön.

**Koodaus:** Kunkin tietoyksikön 64 kvantisoitua muunnettua kerrointa (jotka ovat nyt kokonaislukuja) koodataan käyttämällä RLE- ja Huffman-koodauksen yhdistelmää.

**Ylätunnisteen lisääminen:** Viimeisessä vaiheessa lisätään otsikko ja kaikki käytetyt JPEG-parametrit ja tulostetaan tulos.

JPEG-dekooderi käyttää käänteisiä vaiheita luodakseen alkuperäisen kuvan pakatusta kuvasta.

### Tiedostorakenne ###

JPEG-kuva esitetään segmenttien sarjana, jossa jokainen segmentti alkaa merkillä. Jokainen merkki alkaa 0xFF-tavulla, jota seuraa merkkilippu edustamaan merkin tyyppiä. Hyötykuorma, jota seuraa merkki, on erilainen merkkityypin mukaan. Yleiset JPEG-merkkityypit on lueteltu alla:

|Lyhyt nimi|tavua|Payload|Nimi|Kommentit
---|---|---|---|---|
|SOI|0xFF, 0xD8|ei mitään|Kuvan alku|
|S0F0|0xFF, 0xC0|muuttuva koko|Kehyksen alku|
|S0F2|0xFF, 0xC2|muuttuva koko|Aloita kehykselle|
|DHT|0xFF, 0xC4|muuttuva koko|Määritä Huffman-taulukot|
|DQT|0xFF, 0xDB|muuttuva koko|Määritä kvantisointitaulukko(t)|
|DRI|0xFF, 0xDD|4 tavua|Määritä uudelleenkäynnistysväli|
|SOS|0xFF, 0xDA|muuttuva koko|Skannauksen aloitus|
|RSTn|0xFF, 0xD//n//(//n//#0..7)|ei mitään|Käynnistä uudelleen|
|APPn|0xFF, 0xE//n//|muuttuva koko|Sovelluskohtainen|
|COM|0xFF, 0xFE|muuttuva koko|Kommentoi|
|EOI|0xFF, 0xD9|ei mitään|Kuvan loppu|

Entropiakoodatuissa tiedoissa, minkä tahansa 0xFF-tavun jälkeen, kooderi lisää 0x00-tavun ennen seuraavaa tavua, jotta ei näytä olevan merkkiä, jos sellaista ei ole tarkoitettu, mikä estää kehystysvirheet. Dekoodereiden on ohitettava tämä 0x00 tavu. Tätä tekniikkaa, jota kutsutaan nimellä [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (katso JPEG-spesifikaatiota F.1.2.3), sovelletaan vain entropiakoodattuihin tietoihin, ei merkitsijän hyötykuormatietoihin. Huomaa kuitenkin, että entropiakoodatulla tiedolla on muutama oma merkki; erityisesti nollausmerkit (0xD0 - 0xD7), joita käytetään eristämään itsenäisiä entropiakoodatun datan osia rinnakkaisen dekoodauksen mahdollistamiseksi, ja kooderit voivat vapaasti lisätä näitä nollausmerkkejä säännöllisin väliajoin (vaikka kaikki lähettimet eivät tee tätä).

