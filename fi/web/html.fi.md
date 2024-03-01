{
  "date": "2019-10-11",
  "keywords": [
"html",
"html-tiedosto",
"html-tiedostomuoto",
"html-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on html-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTML-tiedostomuoto",
  "description": "Opi HTML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata HTML-tiedostoja.",
  "linktitle": "HTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htm-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on HTML-tiedosto?

HTML (Hyper Text Markup Language) on laajennus web-sivuille, jotka on luotu näytettäväksi selaimissa. Verkkokielenä tunnettu HTML on kehittynyt uusien tietovaatimusten myötä, jotta se voidaan näyttää osana verkkosivuja. Uusin versio tunnetaan nimellä HTML 5, joka antaa paljon joustavuutta kielen kanssa työskentelyyn. HTML-sivut joko vastaanotetaan palvelimelta, jossa niitä isännöidään, tai ne voidaan ladata myös paikallisesta järjestelmästä. Jokainen HTML-sivu koostuu HTML-elementeistä, kuten lomakkeista, tekstistä, kuvista, animaatioista, linkeistä jne. Näitä elementtejä edustavat tagit ja monet muut, joissa jokaisella tagilla on alku ja loppu. Se voi myös upottaa sovelluksia, jotka on kirjoitettu komentosarjakielillä, kuten JavaScript ja Style Sheets (CSS), yleisen asettelun esittämiseksi.

## Lyhyt historia ##

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. Vuonna 2000 siitä tuli myös kansainvälinen standardi (ISO/IEC 15445:2000). Vuonna 1999 julkaistiin HTML 4.01. Vuonna 2004 Web Hypertext Application Technology Working Group (WHATWG) aloitti työskentelyn HTML5-version parissa, josta tuli yhteinen tulos W3C:n kanssa vuonna 2008. Se valmistui ja standardoitiin 28.10.2014.

## HTML-tiedostomuotorakenne ##

HTML 4 -dokumentti koostuu kolmesta osasta:

1. rivi, joka sisältää HTML-versiotiedot
1. ilmoittava otsikkoosio
1. runko, joka sisältää asiakirjan todellisen sisällön. Runko voidaan toteuttaa BODY-elementillä tai FRAMESET-elementillä sisältämään rungon kehyksissä

Jokaisen osion alussa tai perässä voi olla välilyöntejä, rivinvaihtoja, sarkaimia ja kommentteja. Esimerkki yksinkertaisesta HTML-asiakirjasta on seuraavanlainen:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML-tiedostomuoto</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Versiotiedot ###

Ensimmäinen koodirivi, \<!DOCTYPE html> , kutsutaan doctype-määritelmäksi ja se kertoo selaimelle, millä HTML-versiolla sivu on kirjoitettu. HTML-versiosta riippuen on olemassa useita erilaisia doctype-määrityksiä, jotka nimeävät asiakirjassa käytettävän asiakirjatyypin määritelmän (DTD). Jokainen DTD eroaa muista tuetuissa elementeissä ja eroaa seuraavasti:

* HTML 4.01 Strict – sisältää kaikki elementit ja attribuutit, joita ei ole [vanhentunut](https://www.w3.org/TR/html401/conform.html#deprecated) tai jotka eivät näy kehyssarjadokumenteissa

* HTML 4.01 Transitional - sisältää kaiken tiukan DTD:n sekä vanhentuneet elementit ja attribuutit (joista suurin osa koskee visuaalista esitystapaa

* HTML 4.01 Frameset - sisältää kaiken myös siirtymäkauden DTD plus -kehyksissä


**HTML5**:n versiotiedot ovat yksinkertaisesti alla mainitut.

```
<!DOCTYPE html>
```

### HTML-otsikon tiedot ###

HTML-dokumentin otsikko voi sisältää useita HTML-elementtejä, joita selain ei renderöi. Tällaiset elementit ovat joko metatietoja, jotka kuvaavat sivun tietoja, tai sisältävät osioita, joita käytetään tietojen hakemiseen ulkoisista resursseista, kuten CSS-tyylitaulukoista tai JavaScript-tiedostoista. Sivun otsikkoa edustaa head-tunniste.

Sivun otsikon asettamiseksi **title**-elementti on ainoa, joka vaaditaan<head> tunnisteet. Hakukoneet käyttävät samaa sivun otsikon tunnistamiseen.

### HTML-tekstitiedot ###

Tämä on tiedoston pääosio, joka sisältää kaiken tiedoston sisällön, jonka selaimet renderöivät. Html-teksti voi sisältää merkintöjä, jotka voivat viitata erilaisiin rakennuspalikoihin tagien muodossa. Se voi sisältää useita erityyppisiä tietoja, kuten tekstiä, kuvia, värejä, grafiikkaa jne. Lisäksi ääni- ja videoelementtejä voidaan myös upottaa html-tekstiin selainten renderöimiseksi. Nykyaikaisten visuaaliseen esittämiseen tarkoitettujen tyylisivusovellusten läsnä ollessa BODY:n esitysattribuutit, kuten taustaväri, linkin väri, tekstin väri jne., on poistettu käytöstä. Näin ollen samat tehosteet voidaan saavuttaa käyttämällä tyylitaulukoita, kuten alla on esitetty:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Sisäiset tyylisivut on helppo upottaa, ja visuaalisten tehosteiden nopeaa sovellusta varten ulkoiset tyylisivut tekevät niistä helpompaa ottaa käyttöön kerran ja käyttää useissa paikoissa.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML-elementit ###

Kuten aiemmin mainittiin, HTML-tekstin sisällä olevaa sisältöä edustavat tagit, jotka tunnetaan myös nimellä HTML-elementit. Jokaisella tunnisteella voi olla lisätietoja attribuuttien muodossa, jotka on kirjoitettu<tag attribute1#value1 attribute2#value2> , vaikka jokaisen tunnisteen kanssa ei tarvitse olla attribuutteja. Jos attribuutteja ei mainita, oletusarvoja käytetään jokaisessa tapauksessa. Seuraavassa on joitain esimerkkejä elementeistä:

#### Otsikko ####

```
<head>
  <title>The Title</title>
</head>
```

#### Otsikot ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Kappaleet ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Viitteet ##

* [HTML-dokumentin yleinen rakenne](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


