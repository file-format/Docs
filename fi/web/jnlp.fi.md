---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP-tiedostomuoto - Mikä on JNP-tiedostoe?
linktitle: JNLP
description: Lansaita JNLP-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata JNLP-tiedostons.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Mikä on JNLP-tiedosto?

JNLP-tiedosto on Java Web Start (JWS) -tiedosto, joka sisältää XML-tietoja Java-ohjelman käynnistämistä varten verkossa. Se on tallennettu Java Network Launching Protocol (JNLP) -muodossa. Sitä käyttää Java Web Start (JWS) -tekniikka, joka on sovellusten käyttöönottotekniikka sovelluksen lataamiseen ja suorittamiseen. JNLP-tiedosto sisältää sen palvelimen etäosoitteen, josta ohjelma ladataan ja käynnistetään paikallisella koneella.

## JNLP-tiedostomuoto - lisätietoja

JNLP-tiedostot tallennetaan **[XML](/web/xml/)**-tiedostoina, jotka on tallennettu ihmisen luettavassa tekstimuodossa. XML-tiedostossa on tiedot, joita käytetään Java-sovelluksen käynnistämiseen ja suorittamiseen verkossa. JWS:n avulla voit käynnistää sovelluksia napsauttamalla web-sivun linkkiä. Sovellus ladataan, jos sitä ei ole vielä ladattu käyttäjän tietokoneelle.

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. Tämän myötä JNLP-tiedostoja ei enää tueta.

### Kuinka avata JNLP-tiedostoja?

Sovelluksia, jotka voivat **avata JNLP-tiedostoja**, ovat **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** ja * *GitHub Atom**.

### JNLP-tiedostoesimerkki

```
<jnlp spec="1.0" codebase="http://localhost/jws" href="Notepad.jnlp">
   <information>
      <title>Notepad Demo</title>
      <vendor>Sun Microsystems, Inc.</vendor>
   </information>
   <resources>
      <property name="jnlp.publish-url" value="$$context/publish"/>
      <j2se version="1.3+" href="http://java.sun.com/products/autodl/j2se"/>
      <jar href="Notepad.jar"/>
   </resources>
   <application-desc main-class="Notepad"/>
</jnlp>
```
**Käyttö**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
   <TITLE>Java Web Start Demo</TTLE>    
</HEAD>
<BODY>

<H1>Java Web Start Demo</H1>
<a href="Notepad.jnlp">Lanuch Notepad Application</a>
This link is to the Notepad.jnlp file.
</BODY>
</HTML>
```
## Kuinka ajaa JNLP-tiedostoja?

JWS:n vanhentuessa JWS-teknologiaan perustuvia sovelluksia ei voida käyttää uusimmalla Java-versiolla. Näitä JNLP-pohjaisia ohjelmia voidaan kuitenkin ajaa OpenWebStartilla, joka on Java Web Start -teknologian avoimen lähdekoodin uudelleentoteutus. Se asennetaan rinnakkain uusimman Java-version kanssa ja tarjoaa Java Web Startin ja JNLP-standardin yleisimmin käytetyt ominaisuudet.

## Viitteet ##

* [Mikä Java Web Start on ja miten se käynnistetään?](https://www.java.com/en/download/help/java_webstart.html)

* [Aja JNLP Java uusimmalla versiolla](https://openwebstart.com/)

* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)


