{
  "date": "2019-10-11",
  "keywords": [
"CGM",
"Tietokonegrafiikan metatiedosto",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Vektorigrafiikka",
"Metatiedoston kuvaaja"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CGM-tiedostomuoto",
  "description": "Opi CGM-tiedostomuodosta ja API:ista, jotka voivat luoda ja avata CGM-tiedostoja.",
  "linktitle": "CGM",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-cg-fim"
}
},
  "lastmod": "2021-04-23"
}

## Mikä on CGM-tiedosto? ##

Computer Graphics Metafile (CGM) on ilmainen, alustasta riippumaton, kansainvälinen standardi metatiedostomuoto vektorigrafiikan (2D), rasterigrafiikan ja tekstin tallentamiseen ja vaihtamiseen. CGM käyttää oliolähtöistä lähestymistapaa ja monia toimintosäännöksiä kuvien tuottamiseen. CGM käyttää näitä olio-ominaisuuksia graafisten elementtien uudelleenmuovaukseen kuvan renderöimiseksi. Metatiedosto sisältää tarvittavat tiedot, jotka määrittelevät muut tiedostot. CGM:ssä tekstipohjainen lähdetiedosto sisältää kaikki graafiset elementit, jotka voidaan myöhemmin kääntää binääritiedostoksi. Pohjimmiltaan CGM on tapa helpottaa 2D-graafista tiedonvaihtoa, riippumatta tietystä alustasta tai laitteesta.

CGM-muoto tarjoaa erilaisia elementtejä toimintojen suorittamiseen ja objektien merkitsemiseen geometristen primitiivien ja graafisten tietojen säätämiseksi. Vaikka CGM on korvattu muilla muodoilla grafiikan näyttämiseksi verkkosivuilla, koska verkkosivut eivät tue sitä hyvin, se on edelleen erittäin suosittu teollisuuden, ilmailun ja muiden teknisten sovellusten keskuudessa. Vaikka World Wide Web Consortium on kehittänyt WebCGM:n, vaihtoehtoisen lähestymistavan CGM:n käyttöön verkossa. Ensisijainen CGM-toteutus oli esimerkki graafisen ydinjärjestelmän (GKS) perustoimintojen järjestyksestä. Sitä ei ole juurikaan otettu käyttöön ammattimaisessa suunnittelussa, mutta se on suurelta osin syrjäytynyt muilla muodoilla, kuten DXF ja SVG.

## Historia ##

CGM osoittautui kansainväliseksi standardiksi vuonna 1987 (ISO 8632-1987), ja BSI hyväksyi sen myös kansalliseksi standardiksi Isossa-Britanniassa ja ANSI:ssa Yhdysvalloissa. Useiden vuonna 1991 tehtyjen muutosten jälkeen CGM:n tarkistettu standardi julkaistiin vuonna 1992 (ISO 8632:1992). Vuonna 2001 World Wide Web Consortium kehitti WebCGM:n, jolla on parannettu ominaisuus käytettäväksi verkkosivujen kanssa. Vuonna 2007 WebCGM:n toinen versio julkaistiin ja kolmas versio julkaistiin vuonna 2010 parannetuilla ominaisuuksilla.

## CGM-tiedostomuoto ##

Tietokonegrafiikan metatiedostot ovat pohjimmiltaan tietokanta graafiselle tiedolle ja tarjoavat välineet graafisen tiedon sieppaamiseen, tallentamiseen ja siirtoon. Tästä syystä tietokannan luomiseen samanaikaisesti metatiedostomuodossa olevan sovelluksen suorittamisen kanssa täytyy olla graafinen järjestelmäkomponentti. Useimmissa tapauksissa tämä komponentti on Metafile-generaattori. Sen lisäksi tarvitaan toinen komponentti, joka voi hakea, tulkita ja hahmontaa graafista dataa metatiedostossa. Tämä tarve täyttää metatiedostotulkin läsnäolo. Seuraava kuva esittää graafisen metatiedoston työympäristön.

CGM:n suhde tyypillisen grafiikkajärjestelmän muihin komponentteihin on havainnollistettu yllä olevassa kuvassa. Kuvasta käy myös ilmi, että metatiedoston toiminnallisuus ei ole riippuvainen lopullisesta laitteen lähdöstä.

Generally, there are two categories of metafile: **section capture** and **picture capture**. The primary functionality of picture capture metafile is the capturing of device-independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two-level structure.

1. Metatiedoston kuvaaja
1. Joukko loogisesti riippumattomia kuvia

Jokainen kuva on kokoelma kuvakuvaajia ja kuvarunko, joka sisältää kuvan määritelmän. metatiedoston deskriptor määrittelee kuvaavat tiedot, jotka koskevat yhtä lailla kaikkia kyseisen metatiedoston kuvia. Nämä tiedot auttavat tulkkia jäsentämään metatiedoston oikein ja tunnistamaan resurssit, joita tarvitaan kuvan oikeaan hahmontamiseen. Vaikka kuvakuvaaja sisältää myös kuvaavat tiedot, se voi tunnistaa vain kuvan, jossa kuvaaja sijaitsee. Tässä tiedostomuodossa jokainen kuvan määritelmä on itsenäinen ja loogisesti suvereeni. Ne ovat riippumattomia kaikista muista tiedoston kuvamääritelmistä. Heti metakuvaajan tulkinnan jälkeen kuviin pääsee käsiksi ja niitä voidaan tulkita satunnaisesti. Aikaisempien kuvien tilan muutoksella ei ole vaikutusta niiden seuraajiin. Tämä kuvan riippumattomuus on toinen CGM:n näkyvä ominaisuus. CGM koostuu koordinaattiavaruudesta, jotka ovat 2D-suorakulmaisia koordinaatteja, joita kutsutaan virtuaalilaitteen koordinaatteiksi ja jotka voidaan esittää numerolla tai tarkkuudella, jotka edustavat aluetta ja tarkkuutta. CGM määrittää sekä värien suoran valinnan että indeksipohjaisen valinnan. Edellisessä värin määrittäjä koostuu RGB-kolmoisesta, kun taas myöhemmin värimäärittäjä osoittaa indeksin väritaulukkoon.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
