{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-tiedosto",
"cfg celestia -määritystiedosto",
"mikä on cfg-tiedosto",
"kuinka avata cfg-tiedosto",
"tiedosto",
"cfg tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG-tiedostomuoto - Celestia-määritystiedosto",
  "description": "Opi CFG Celestia Configuration File -muodosta ja API:ista, jotka voivat luoda ja avata CFG-tiedostoja.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia-fi",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Mikä on CFG-tiedosto?

Celestia-määritystiedosto on pelkkä tekstitiedosto, jota käyttää Celestia, 3D-universumin simulointiohjelma. Nämä tiedostot ovat elintärkeitä mukautettaessa, miten Celestia käyttäytyy, mitä taivaankappaleita näytetään ja miten ohjelma näyttää. Näiden tiedostojen muokkaaminen vaatii kuitenkin huolellista huomiota, koska väärät muutokset voivat häiritä Celestian latausprosessia ja estää sitä toimimasta oikein.

## Celestia

Celestia on ilmainen avoimen lähdekoodin 3D-astronomian simulointiohjelmisto, jonka avulla käyttäjät voivat tutkia ja visualisoida maailmankaikkeutta erittäin realistisella ja interaktiivisella tavalla. Sen on kehittänyt Chris Laurel, ja se julkaistiin ensimmäisen kerran 2000-luvun alussa. Celestia on saatavilla Windows-, macOS- ja Linux-käyttöjärjestelmille.

Celestian tärkeimmät ominaisuudet ja näkökohdat ovat:

- **Realistinen 3D-visualisointi:** Celestia tarjoaa yksityiskohtaisen ja tarkan esityksen aurinkokunnastamme sekä tähdistä, galakseista ja muista taivaankappaleista. Se käyttää korkealaatuisia 3D-malleja ja tekstuureja visuaalisesti mukaansatempaavan kokemuksen luomiseen.

- **Laaja taivaallinen tietokanta:** Ohjelmiston mukana tulee laaja sisäänrakennettu tietokanta tunnetuista taivaankappaleista, mukaan lukien tähdet, planeetat, kuut, asteroidit, komeetat ja avaruusalukset. Käyttäjät voivat helposti paikantaa ja tutkia näitä kohteita.

- **Tieteellinen tarkkuus:** Vaikka Celestia on visualisointityökalu, sen tavoitteena on esittää taivaankohteet ja -ilmiöt mahdollisimman tarkasti käytettävissä olevien tieteellisten tietojen perusteella.

## Celestian käyttämät tiedostomuodot

Celestia hyödyntää erilaisia tiedostomuotoja 3D-astronomian simulaatioissaan. Tässä on joitain Celestian käyttämiä keskeisiä tiedostomuotoja:

1. **Asetustiedostot (.cel)**
- *Kuvaus*: Pelkkä tekstitiedostot, joiden avulla käyttäjät voivat mukauttaa Celestian käyttäytymistä, ulkonäköä ja sisältöä.
- *Tarkoitus*: Asetusten mukauttaminen, sijaintien määrittäminen ja taivaankappaleiden määrittäminen.

2. **3D-mallit ja -verkot**
- *Muodot*: [.3ds](/3d/3ds/), [.obj](/3d/obj/), [.dae](/3d/dae/), .ac
- *Kuvaus*: Tuetut 3D-mallitiedostomuodot, joita käytetään taivaankappaleiden ja avaruusalusten hahmontamiseen.
- *Tarkoitus*: 3D-objektien näyttäminen Celestiassa.

3. **Tekstuuritiedostot**
- *Muodot*: [.jpg](/image/jpeg/), [.png](/image/png/), [.dds](/image/dds/)
- *Kuvaus*: Nämä tiedostot tarjoavat pintakuvioita taivaankappaleille.
- *Tarkoitus*: Mappaa pintakuvioita 3D-malleihin realistisen ulkonäön saamiseksi.

4. **Tähtiluettelot ja datatiedostot**
- *Muodot*: Muokatut muodot, [.csv](/spreadsheet/csv/), [.tsv](/spreadsheet/tsv/)
- *Kuvaus*: Datatiedostot, joita käytetään edustamaan tähtiä ja muita taivaankappaleita, mikä takaa tarkan simulaation.
- *Tarkoitus*: Tarkka esitys taivaankappaleista.

5. **Tektuurikuutiokartat**
- *Kuvaus*: Kuutiokarttoja käytetään simuloimaan kaukaisten taivaankappaleiden, kuten galaksien, esiintymistä.
- *Tarkoitus*: Kaukaisten kohteiden renderöiminen realistisilla pintakuvioilla.

6. **Skriptitiedostot**
- *Kuvaus*: Nämä tiedostot sisältävät mukautettuja skriptejä, jotka on kirjoitettu Celestian komentosarjakielellä.
- *Tarkoitus*: Mahdollistaa käyttäjien luoda dynaamisia tapahtumia ja animaatioita Celestian universumissa.

## Celestia-määritystiedosto

Tässä on peruskatsaus siitä, mitä voit tehdä Celestia-määritystiedostolla:

1. **Sijainnin asettaminen**: Voit määrittää sijaintisi maan päällä käyttämällä leveys-, pituus- ja korkeusparametreja. Tämän ansiosta Celestia voi näyttää yötaivaan tarkasti sijainnistasi käsin.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Katseluasetusten mukauttaminen:** Voit säätää erilaisia katseluasetuksia, kuten näkökenttää, aikaasetuksia ja renderöintiasetuksia.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Ladataan taivaankohteita:** Voit lisätä simulaatioosi taivaankappaleita, kuten tähtiä, planeettoja, asteroideja, avaruusaluksia ja paljon muuta. Jokainen objekti määritellään asetustiedostossa ominaisuuksineen.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Avaruusalusten määrittäminen:** Voit luoda omia kuvitteellisia avaruusaluksiasi tai käyttää aitoja määrittämällä niiden parametrit, kuten sijainnin, suunnan ja 3D-mallit.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Skriptien luominen:** Voit kirjoittaa skriptejä Celestian mukautetulla komentosarjakielellä luodaksesi dynaamisia tapahtumia ja animaatioita.

## Kuinka avata CFG -tiedosto?

Ohjelmat, jotka avaavat CFG-tiedostoja tai viittaavat niihin

- Celestia (ilmainen) (Windows, Mac, Linux)

## Muut CFG-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.cfg**-tiedostotunnistetta.

**Asetukset**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Peli**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Järjestelmä ja muut**
- {{HYPERLINKKI}}
- {{HYPERLINKKI1}}

## Viitteet
* [Celestia](https://en.wikipedia.org/wiki/Celestia)


