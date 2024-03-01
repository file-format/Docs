{
  "date": "2019-10-11",
  "keywords": [
"j2c tiedosto",
"j2c tiedostomuoto",
"mikä on j2c-tiedosto",
"tiedosto",
"j2c esimerkki",
"j2c tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2C",
  "description": "Opi J2C-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata J2C-tiedostoja.",
  "linktitle": "J2C",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-fic"
}
},
  "lastmod": "2021-02-14"
}

## Mikä on J2C-tiedosto?

Tiedosto, jonka pääte on .j2c, on muunnelma JPEG-tiedostomuodosta, ja se on pakattu aallokepakkauksella. Siinä on lähes identtinen merkki- ja segmenttijärjestelmä JPEG 2000 -tiedostomuodon kanssa. J2C-tiedostomuoto on määritelty JPEG 2000 -telineen osassa 1, joka tukee sekä häviöllistä että häviötöntä pakkausta. JPEG 2000 -koodivirta on suunniteltu upotettavaksi {{HYPERLINKKI}}- tai muuhun tiedostomuotoon, vaikka se saattaa esiintyä tiedostossa sellaisenaan. J2C-tiedoston voi avata Adobe Photoshop 2020:lla, Adobe Illustrator 2020:lla ja Corel Paintshop Prolla.

## J2C tiedostomuoto

J2C-tiedostomuoto on sama kuin JPEG 2000, joka usein tallennetaan .jp2- ja .jpc-muodossa. Tämä saa J2C-tiedostot noudattamaan samaa lähestymistapaa metatietojen koodauksessa XML-muotoon, jossa standardia 12234-1 käytetään viitteenä Exif-tunnisteiden ja XML-komponenttien välillä. Sitä parantaa edelleen JPEG 2000 part-2 -laajennus, joka yhdistää animaatiomekanismin ja koodivirran kokoonpanot yhdeksi kuvaksi. Tällaiset laajennetut tiedostomuotoiset tiedostot tallennetaan nimellä {{HYPERLINKKI}}.

### JPEG2000-tiedoston asettelu

JPEG2000 tukee useita sovelluksia, jotka perustuvat laajennettavien tiedostomuotojen yhteensopivuuteen. Vaikka yksinkertaisin tyyppi voi sisältää yhden kuvan, monimutkaisempiin tyyppeihin voi kuulua sarja kuvia päällekkäin tai aikaperusteisesti sekvensoituja.

#### JP2 Box
Se on JP2-tiedostomuodon ylimmän tason rakennuspalikka, ja se sisältää otsikossa tyyppi- ja pituuskentät sekä tietolohkon. Merkittävin laatikkotyyppi on vierekkäinen koodivirtalaatikko. Tämä laatikko tallentaa tietoosioonsa JPEG2000-koodivirran.

#### JPEG2000 CodeStream

JPEG2000 CodeStream on tavusarja, joka tarvitaan JPEG2000-pakatun kuvan purkamiseen. Jos tiedostossa ei ole mitään muuta kuin tämä koodivirta, sitä kutsutaan raakakoodivirtatiedostoksi. Yleensä JPEG-koodivirta on JPEG2000-pakkausalgoritmin soveltaminen kuvaan, vaikka se ei ole ainoa tapa.

#### Laattaosat ####

JPEG2000-koodattu kuva on kokoelma datayksiköitä, joita kutsutaan paketeiksi. Näitä paketteja ylläpidetään koodivirrassa pakettiryhmissä, joita kutsutaan ruutuosiksi. Ennen kuvan koodaamista enkooderi jakaa kuvan suorakaiteen muotoiseksi lohkoiksi, joita kutsutaan laatoiksi ja joissa jokainen ruutu koodataan erikseen muista ruuduista riippumatta.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 tiedostomuoto" >}}

## J2C pakkaus
JPEG 2000 käyttää wavelet-pakkaustekniikkaa, mikä tekee siitä nopean perustuen siihen, että suhteellisen vähän pikseleitä näytetään missä tahansa katseluportissa tai ikkunassa, jonka katsoja näyttää. Tätä voi korostaa se, että näytölle tulee vain muutama megatavu pikseleitä erittäin suurikokoisissa kuvissa (gigatavuina). Tämä auttaa noutamaan ja hahmontamaan nopeasti vain sen osan kuvadatasta, joka tarvitaan näytön pikselien täyttämiseen. Tämä edellyttää myös nopeaa purkutekniikkaa, joka nopeuttaa kuvanhakumekanismia lennossa tarvittavien kuvien luomiseksi.

J2C hyödyntää nopeaa purkamista ja hakee vain tarpeelliset tiedot pikselidataa varten, jotta osa näkyvistä kuvista saadaan nopeasti näytöille. J2C on suunniteltu ensisijaisesti tietojen katseluun, ei sen muokkaamiseen.

## J2C-tunnistus
JPEG 2000 -tiedostoissa on allekirjoitustavut FF 4F FF 51.

### Mime-tyypit
JPEG 2000 -tiedostoille rekisteröityjä mime-tyyppejä ovat:
  * image/j2c
  * kuva/jpx
  * kuva/jpm
  * video/mj2

## Parannuksia JPEG-standardiin verrattuna
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

