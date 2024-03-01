{
  "date": "2021-05-24",
  "keywords": [
"zul",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"avata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZUL - ZK-käyttöliittymätiedosto",
  "description": "Opi ZUL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ZUL-tiedostoja.",
  "linktitle": "ZUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-zu-fil"
}
},
  "lastmod": "2021-05-24"
}

## Mikä on ZUL-tiedosto?

Tiedosto, jonka laajennus on .zul, on verkkotiedosto, joka on luotu ZUML (User Interface Markup Language) -kielellä ja sisältää määritelmiä käyttöliittymäelementeille. Ajax- ja Java-luokat tukevat [XML](/web/xml/)-pohjaisen ZUML:n käyttöä palvelinpuolen tiedostojen kehittämiseen. ZUL-tiedostomuodon on kehittänyt ZK, käyttöliittymäkehys, jonka avulla voit rakentaa verkko- ja mobiilisovelluksia ilman JavaScriptin tai AJAXin tuntemusta.

## ZUL tiedostomuoto

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### ZUL Esimerkki

Seuraavassa ZUML-koodin esimerkissä ensimmäinen rivi määrittää sivun otsikon, toinen rivi luo juurikomponentin otsikolla ja reunuksella ja kolmas rivi luo painikkeen, jossa on otsikko ja tapahtumakuuntelija.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL-skeeman voi ladata osoitteesta https://www.zkoss.org/2005/zul/zul.xsd.
## Viitteet

* [ZUL - kirjoittanut ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)

* [ZUL Schema](https://www.zkoss.org/2005/zul/zul.xsd)


