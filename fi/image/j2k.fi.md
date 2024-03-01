{
  "date": "2019-10-11",
  "keywords": [
"j2k tiedosto",
"j2k tiedostomuoto",
"mikä on j2k-tiedosto",
"tiedosto",
"j2k esimerkki",
"j2k tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2K",
  "description": "Opi J2K-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata J2K-tiedostoja.",
  "linktitle": "J2K",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-fik"
}
},
  "lastmod": "2020-08-03"
}

## Mikä on J2K-tiedosto?

**J2K**-tiedosto on kuva, joka on pakattu käyttämällä wavelet-pakkausta DCT-pakkauksen sijaan. Tätä tiedostomuotoa käyttävät Joint Photographic Experts Group (JPEG) 2000 -tiedostot. J2K-tiedostot tallentavat metatiedot kuvatiedostosta XML-muodossa toisin kuin .jpeg tai .jpg, jotka käyttävät tähän tarkoitukseen EXIF-muotoa. J2K-tiedostot tukevat 15-bittistä väriä, alfaläpinäkyvyyttä ja häviötöntä pakkausta. JPEG 2000 -kuvien purkamiseen on olemassa useita kaupallisia API:ita, kuten J2K-Codec. J2K-tiedosto voidaan avata Windows-käyttöjärjestelmässä tavallisilla kuvankatseluohjelmilla.

## J2K-tiedostomuoto ##

J2K-tiedostomuoto on sama kuin JPEG 2000, joka usein tallennetaan .jp2- ja .jpc-muodossa. Tämä saa J2K-tiedostot noudattamaan samaa lähestymistapaa metatietojen koodauksessa XML-muotoon, jossa standardia 12234-1 käytetään viitteenä Exif-tunnisteiden ja XML-komponenttien välillä. Sitä parantaa edelleen JPEG 2000 part-2 -laajennus, joka yhdistää animaatiomekanismin ja koodivirran kokoonpanot yhdeksi kuvaksi. Tällaiset laajennetut tiedostomuotoiset tiedostot tallennetaan .jpx-muodossa.

### JPEG2000-tiedoston asettelu ###

JPEG2000 tukee useita sovelluksia, jotka perustuvat laajennettavien tiedostomuotojen yhteensopivuuteen. Vaikka yksinkertaisin tyyppi voi sisältää yhden kuvan, monimutkaisempiin tyyppeihin voi kuulua sarja kuvia päällekkäin tai aikaperusteisesti sekvensoituja.

#### JP2 Box ####
Se on JP2-tiedostomuodon ylimmän tason rakennuspalikka, ja se sisältää otsikossa tyyppi- ja pituuskentät sekä tietolohkon. Merkittävin laatikkotyyppi on vierekkäinen koodivirtalaatikko. Tämä laatikko tallentaa tietoosioonsa JPEG2000-koodivirran.

#### JPEG2000 CodeStream ####

JPEG2000 CodeStream on tavusarja, joka tarvitaan JPEG2000-pakatun kuvan purkamiseen. Jos tiedostossa ei ole muuta kuin tämä koodivirta, sitä kutsutaan raakakoodivirtatiedostoksi. Yleensä JPEG-koodivirta on JPEG2000-pakkausalgoritmin soveltaminen kuvaan, vaikka se ei ole ainoa tapa.

#### Laattaosat ####

JPEG2000-koodattu kuva on kokoelma datayksiköitä, joita kutsutaan paketeiksi. Näitä paketteja ylläpidetään koodivirrassa pakettiryhmissä, joita kutsutaan ruutuosiksi. Ennen kuvan koodaamista enkooderi jakaa kuvan suorakaiteen muotoiseksi lohkoiksi, joita kutsutaan laatoiksi ja joissa jokainen ruutu koodataan erikseen muista ruuduista riippumatta.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 tiedostomuoto" >}}

## J2K-pakkaus ##
JPEG 2000 käyttää wavelet-pakkaustekniikkaa, mikä tekee siitä nopean perustuen siihen, että suhteellisen vähän pikseleitä näytetään missä tahansa katseluportissa tai ikkunassa, jonka katsoja näyttää. Tätä voi korostaa se, että näytölle tulee vain muutama megatavu pikseleitä erittäin suurikokoisissa kuvissa (gigatavuina). Tämä auttaa noutamaan ja hahmontamaan nopeasti vain sen osan kuvadatasta, joka tarvitaan näytön pikselien täyttämiseen. Tämä edellyttää myös nopeaa purkutekniikkaa, joka nopeuttaa kuvanhakumekanismia lennossa tarvittavien kuvien luomiseksi.

J2K hyödyntää nopeaa purkamista ja hakee vain tarpeelliset tiedot pikselidataa varten, jotta osa näkyvistä kuvista saadaan nopeasti näytöille. J2K on suunniteltu ensisijaisesti tietojen katseluun, ei sen muokkaamiseen.

## J2K-tunniste ##
JPEG 2000 -tiedostoissa on allekirjoitustavut 6A 50 20 20.

### Mime-tyypit ###
JPEG 2000 -tiedostoille rekisteröityjä mime-tyyppejä ovat:
  * kuva/jp2
  * kuva/jpx
  * kuva/jpm
  * video/mj2

## Parannuksia verrattuna JPEG-standardiin ##
JPEG-standardiin verrattuna tehtyjä parannuksia ovat mm.
  * Ylivoimainen pakkausteho
  * Usean resoluution esitys
  * Progressiivinen lähetys pikselin mukaan ja resoluution tarkkuus
  * Valinta häviöttömäksi tai häviöttömäksi pakkaukseksi
  * Virheiden sietokyky, joustava tiedostomuoto
  * Korkean dynaamisen alueen tuki
  * Sivukanavan paikkatiedot

## Viitteet ##
  * [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

