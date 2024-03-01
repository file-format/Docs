{
  "date": "2019-12-12",
  "keywords": [
"EPUB",
"tiedosto",
"laajennus",
"muoto",
"E-kirja",
"Digitaalinen kirja"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi EPUB-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata EPUB-tiedostoja.",
  "title": "Mikä on EPUB-tiedosto?",
  "linktitle": "EPUB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-epu-fib"
}
},
  "lastmod": "2019-12-12"
}

## Mikä on EPUB-tiedosto?

.epub-tunnisteella varustetut tiedostot ovat e-kirjojen tiedostomuoto, joka tarjoaa julkaisijoille ja kuluttajille tavallisen digitaalisen julkaisumuodon. Muoto on ollut jo niin yleinen, että monet e-lukijat ja ohjelmistosovellukset tukevat sitä. Esimerkiksi Mac OS:ssä esiasennettu **Books**-ohjelmisto tukee tällaisten tiedostojen avaamista. Lisäksi saatavilla on paljon yhteensopivia ohjelmistoja älypuhelimille, tableteille ja tietokoneille. EPUB-tiedostostandardeja ylläpitää [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). EPUB 3 -versiota tukee myös Book Industry Study Group (BISG), joka on johtava kirjakaupan järjestö, joka tarjoaa standardoituja parhaita käytäntöjä, tutkimusta, tietoa ja tapahtumia sisällön pakkaamiseen.

## EPUB-tiedostomuodon lyhyt historia

* **Lokakuu 2007** – EPUB 2.0 hyväksyttiin

* **Syyskuu 2010** - Huoltopäivitys julkaistiin

* **Lokakuu 2011** – EPUB 3.0 -määritykset tulivat voimaan

* **Kesäkuu 2014** – Pieni huoltopäivitys julkaistiin 3.0-version korvaamiseksi

* **Tammikuu 2017** – EPUB 3.1 astui voimaan


## EPUB-tiedostomuoto

EPUB-tiedostomuoto on arkisto, joka voidaan nimetä uudelleen laajennukseksi [ZIP](/compression/zip/) ja sen sisältöä voi tarkastella purkamalla arkisto millä tahansa arkiston purkajalla. Se on avoin XML-pohjainen muoto, joka koostuu HTML-tiedostoista, kuvista, CSS-tyylisivuista ja muista elementeistä. Se voidaan myös muuntaa PDF-, Mobi- ja useisiin muihin tiedostomuotoihin useiden ohjelmistosovellusten ja API:iden kautta.

{{< figure src="../epub.png" alt="EPUB-tiedostomuoto" >}}

**EPUB-e-kirja avattu Mac OS Books -sovelluksella**

EPUB-tiedostomuoto perustuu seuraaviin kolmeen avoimeen standardiin.

### Avoin julkinen rakenne (OPS) ###

EPUB 2.0 -tiedosto käyttää XHTML 1.1:tä julkaisun sisällön rakentamiseen. Pohjimmiltaan tämä tarkoittaa, että EPUB-tiedosto koostuu yhdestä tai useammasta verkkosivusta. Vaikka voisit sisällyttää kirjan tai sanomalehden koko sisällön yhdelle sivulle, on parempi, että tällainen tiedosto ei ylitä 300 kt, sekä suorituskyky- että yhteensopivuussyistä. Kuten tavallisilla verkkosivuilla, tyyli ja asettelu määritetään CSS-tyylisivuilla. EPUB-tiedostoissa on käytettävä CSS2:n osajoukkoa (rajoitettu joukko komentoja). Monet CSS3:n uusista ominaisuuksista, kuten pyöristetyt laatikot tai varjot, eivät ole vielä saatavilla. Taaksepäin yhteensopivuuden takaamiseksi sisällöntuottaja voi myös käyttää DTBookia XHTML:n sijaan sisällön koodaamiseen.

### Open Packaging Format (OPF) ###

Tämä osa teknisistä tiedoista käsittelee rakenteellisia tietoja, kuten metatietoja (kuka on kirjoittaja ja kustantaja, mikä on nimi,...), manifestia (luettelo kaikista epub-tiedoston sisällä olevista tiedostoista) ja sisällysluetteloa. Kaikki nämä tiedot on upotettu XML:n avulla.

### Open Container Format (OCF) ###

As the above descriptions should have made it clear an EPUB document consists of a series of files. The OCF specs define how all those files end up being packaged in one single container file. ZIP compression is used for this.

## Tuetut kuvatiedostomuodot ##

EPUB-tiedostomuoto tukee seuraavia kuvatiedostomuotoja.

* [GIF](/image/gif/)

* [JPG](/image/jpeg/)

* [PNG](/image/png/)

* [SVG](/page-description-language/svg/)

## Viitteet ##

* [EPUB – Wikipedia](https://en.wikipedia.org/wiki/EPUB)


