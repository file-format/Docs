{
  "date": "2019-10-11",
  "keywords": [
"mpkg tiedosto",
"mpkg tiedostomuoto",
"mikä on mpkg-tiedosto",
"tiedosto",
"mpkg esimerkki",
"mpkg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPKG-tiedostomuoto - Meta-pakettitiedosto",
  "description": "Opi MPKG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MPKG-tiedostoja.",
  "linktitle": "MPKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-mpk-fig"
}
},
  "lastmod": "2021-04-02"
}

## Mikä on MPKG-tiedosto?

Tiedosto, jonka laajennus on .mpkg, on arkiston asennustiedosto, joka löytyy useimmiten MacOS-käyttöjärjestelmistä. Se sisältää kaikki tarvittavat sovelluksen asennustiedostot ilman, että niihin liittyviä tiedostoja tarvitsee säilyttää erikseen. Yksi MPKG-tiedosto voi sisältää pakettitiedostoja [PKG](/compression/pkg/) yhtenä asennustiedostoista muiden tiedostojen lisäksi. MPKG-tiedostoja ei voi avata millään yleisellä ohjelmistolla, ja ne suoritetaan automaattisesti MacOS:ssä Apple Installerin avulla.

## MPKG tiedostomuoto

MPKG-tiedosto sisältää erityyppisiä tiedostoja, joita tarvitaan useiden sen sisältämien pakettien asentamiseen. Tämä näkyy alla olevasta kuvasta, joka on esimerkki-MPKG-tiedoston puurakenne. Tämä puurakenne viedään käyttämällä `tree` -komentoa MacOS-päätteessä.

{{< figure src="../mpkg.png" alt="MPKG tiedostomuoto" >}}

The description of different elements in the image is as follow.

`Packages Directory` - tallentaa luettelon pkg-tiedostoista, eli luettelon alipaketteista
Resurssihakemisto - tallentaa pkg:n käyttämät resurssit, kuten lokalisoidut resurssit ja kuvat, Rtf-dokumentit, pdf-dokumentit jne.
Distribution.dist-tiedosto - Xml-dokumentti, joka sisältää tietoja, kuten asennettavat alipaketit ja ajonaikaiset komentosarjat

Esimerkki XML-tiedostosta MPKG-tiedostolle voi näyttää seuraavalta riippuen siihen liittyvistä alipaketeista.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
app.pkg - on asennettava alipaketti. Se on Bundle-rakenteen hakemisto pkg-muodossa. Se sisältää Sisältö-alihakemiston.

## Viitteet

* [OSX Flat Packages](https://matthew-brett.github.io/docosx/flat_packages.html)

* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)


