{
  "date": "2020-03-02",
  "keywords": [
"SVG",
"tiedosto",
"tiedosto muoto",
"Sivu Kuvaus Kieli",
"Skalaari"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi SVG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SVG-tiedostoja.",
  "title": "Mikä on SVG-tiedosto?",
  "linktitle": "SVG",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sv-fig"
}
},
  "lastmod": "2020-03-02"
}

## Mikä on SVG-tiedosto? ##

An SVG file is a Scalar Vector Graphics file that uses XML based text format for describing the appearance of an image. The word Scalable refers to the fact that the SVG can be scaled to different sizes without losing any quality. Text-based description of such files makes them independent of resolution. It is one of the most used formats for building a website and print graphics in order to achieve scalability. The format can only be used for two-dimensional graphics though. SVG files can be viewed/opened in almost all modern browsers including Chrome, Internet Explorer, Firefox, and Safari.

## Lyhyt historia ##

SVG specifications are available as open standard by World Wide Web Consortium (W3C) since 1999. Tätä ennen W3C:lle toimitettiin samankaltaisia tiedostomuotomäärityksiä kuudessa eri muodossa vuoteen 1998 asti. Teknisiin tietoihin tehtiin päivitys vuonna 2011 ja se versioittiin 1.1. Vuonna 2016 SVG 2 julkaistiin uudempana versiona, joka sisältää ominaisuuksia SVG 1.1:n ominaisuuksien lisäksi.

## Tiedostomuodon tiedot ##

SVG Document Object Model (DOM) luo perustan kaikille spesifikaatioille ja rajapinnoille, jotka vastaavat spesifikaatioiden tiettyjä osia. SVG-katseluohjelmien on otettava käyttöön SVG DOM -liitännät W3C-spesifikaatioiden mukaisesti. Sen DOM paljastaa useita rajapintoja eri tietotyypeille ja elementeille.

### SVG-muodot ###

SVG:ssä on joitain ennalta määritettyjä muotoelementtejä, joita kehittäjät voivat käyttää:

* Suorakulmio<rect>

* Ympyrä<circle>

*Ellipsi<ellipse>

* Linja<line>

* Polyline<polyline>

* Monikulmio<polygon>

* Polku<path>


Näiden muotojen ja eritelmien perusteella SVG:n toiminnalliset alueet ovat seuraavat.

**Paths** - Polkuja käytetään edustamaan yksinkertaisia sekä yhdistetyn muotoisia ääriviivoja. Koodauksia käytetään määrittelemään toiminnan luonne. Esimerkiksi M:tä käytetään Siirrä kohteeseen, L:tä Line To, Z:tä käytetään polun sulkemiseen ja niin edelleen.

**Perusmuodot** – Voidaan piirtää suoria polkuja ja polkuja, jotka koostuvat sarjasta yhdistettyjä suoria segmenttejä (polylinjoja), sekä suljettuja polygoneja, ympyröitä ja ellipsejä. Suorakulmiot ja pyöreäkulmaiset suorakulmiot ovat myös vakioelementtejä.

**Teksti** - Tekstin esitysmuoto ilmaistaan XML-merkkitietona, jossa tekstiin voidaan soveltaa monia visuaalisia tehosteita. Tekniset tiedot mahdollistavat kaksisuuntaisen tekstin, pystysuuntaisen tekstin ja merkkien käsittelyn kaarevalla polulla.

**Maalaus** - Muodot voidaan täyttää ja/tai rajata väreillä, gradienteilla tai kuvioilla, jolloin niistä voidaan tehdä läpinäkymätön tai läpinäkyvyys. Viivanpään piirteitä, kuten nuolenpäitä tai monikulmion kärjessä olevia symboleja, edustavat merkit.

**Väri** - SVG-spesifikaatioiden avulla värejä voidaan käyttää kaikkiin näkyviin SVG-elementteihin joko suoraan tai täytön, viivan ja muiden ominaisuuksien kautta. Eri värikoodeja voidaan käyttää määrittämään, kuten musta tai sininen, hex-esitys, desimaali tai prosentteina muotoa RGB.

**Liukuvärit ja kuviot** - SVG-tiedoston muodot voidaan täyttää tai rajata yhtenäisillä väreillä, liukuväreillä tai toistuvilla kuvioilla.

**Suodatustehosteet** - Se on itse asiassa sarja grafiikkatoimintoja, joita sovelletaan tiettyyn lähdevektorigrafiikkaan muokatun tuloksen tuottamiseksi.

**Vuorovaikutteisuus** - Käyttäjät voivat olla vuorovaikutuksessa SVG-tiedostojen kanssa muuttamalla tarkennusta, hiiren napsautuksia, vierittämällä tai zoomaamalla kuvaa. Interaktiivisuus mahdollistaa SVG-kuvien vuorovaikutuksen käyttäjien kanssa monilla eri tavoilla, kuten edellä mainittiin.

**Linkitys** - SVG-kuvissa voi olla hyperlinkkejä muihin asiakirjoihin. Tämä saavutetaan XML-linkityskielellä tai XLinkillä. Tämä mahdollistaa tiettyjen näkymätilojen luomisen, joita käytetään tietyn alueen lähentämiseen/pienentämiseen tai näkymän rajoittamiseen tiettyyn elementtiin.

**Komentosarjat** – Kuten HTML:ssä, kaikki SVG-dokumentin osat ovat käytettävissä komentosarjojen avulla tapahtuvaa käsittelyä varten. SVG DOM -objektit tarjoavat ohjeet tämän saavuttamiseen SVG-elementin ja -attribuutin avulla. Skriptit on suljettu script -tunnisteelementteihin ja niitä voidaan suorittaa vastauksena osoittimen, näppäimistön tai asiakirjan tapahtumiin tarpeen mukaan.

**Animaatio** - DOM-elementit<animate> ,<animateMotion> ja<animateColor> voit sisällyttää animaatioita SVG-sisältöön. Tämä ei tietenkään ole saavutettavissa ilman komentosarjoja ja sisäänrakennettuja ajastimia. Nämä animaatiot voivat olla jatkuvia ja niitä voidaan laittaa silmukalle tai toistolle samalla kun ne vastaavat käyttäjän tapahtumiin.

**Fontit** - SVG:n teksti voi viitata ulkoisiin fonttitiedostoihin, kuten järjestelmäkirjasimiin. Jos tällaisia fontteja ei ole, SVG-tekstiä ei hahmonneta tulosteeseen. Tämä voidaan ratkaista sisällyttämällä vaaditut kuviot sellaiseen tiedostoon fonttina, joka sitten hahmonnetaan käyttämällä<text> elementti.

## Esimerkkejä ##
Seuraavat rivit osoittavat, kuinka ympyrä esitetään SVG-skriptillä.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Seuraavat koodirivit osoittavat, kuinka käyttää<text> lohko tekstin renderöimiseksi SVG-muotoon.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Viitteet ##

* [W3C SVG:n tekniset tiedot](https://www.w3.org/TR/SVG2/Overview.html)

* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)


