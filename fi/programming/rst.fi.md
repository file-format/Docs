{
  "date": "2022-04-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RST-tiedostomuoto - reStructuredText-tiedosto",
  "description": "Opi RST-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RST-tiedostoja.",
  "linktitle": "RST",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-rs-fit"
}
},
  "lastmod": "2022-04-11"
}

## Mikä on RST-tiedosto?

RST-tiedosto on teknisen dokumentaation tiedostomuoto, jota käytetään pääasiassa Python-ohjelmointiyhteisössä. Se on reStructuredText-kuvauskielellä kirjoitettu tekstitiedosto, joka soveltaa tyylejä ja muotoiluja pelkkää tekstiä koskeviin asiakirjoihin dokumentaation luomiseksi. RST-tiedostot käyttävät Python-ohjelmakoodin kommentteja ja muita tietoja sovelluksen teknisen dokumentaation luomiseen. Nämä voivat kuitenkin sisältää myös tekstiä, joka voidaan muuntaa yksinkertaisiksi verkkosivuiksi ja {{HYPERLINKKI}}. RST-tiedostojen avaamiseen voidaan käyttää tekstieditoreja, kuten Github Atom, GNU Emacs (monialustaiset), Microsoft Notepad (Windows), Apple TextEdit (Mac) ja Vim (Linux).

## RST-tiedostomuoto

RST-tiedostot sisältävät koodia, joka on kirjoitettu reStructuredText-kuvauskielellä. Se on osa Python Doc-SIG:n (Documentation Special Interest Group) Docutils-projektia, joka tarjoaa Pythonille samanlaisia työkaluja kuin Javadoc for Java. RST-tiedostomuodon jäsentäjä on upotettu Docutilsiin, ja se voi poimia tietoja Python-ohjelmista muotoillakseen ne ohjelman dokumentaatioon.

### reStructuredText RST Esimerkki

Otetaan esimerkkiteksti, joka on kirjoitettu RST-tiedostomuodossa seuraavasti.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Kun tämä teksti syötetään rST-prosessoriin, kuten Docutilsiin, tulos on seuraava.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Viite ##

* [reStructuredText - Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)


