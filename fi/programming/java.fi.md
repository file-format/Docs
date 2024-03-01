---
date: 2019-10-11
keywords: java, .java, java file format, how to open java files, how to run java files, java file, java sample code
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java tiedostolomakeat
linktitle: Java
description: Lansaita Java-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata Java-tiedostojas.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Mikä on Java-tiedosto? ##
Java-lähdekoodia sisältävä tiedosto, joka on tallennettu .java-tiedostotunnisteella, tunnetaan Java-tiedostona. Java on yksi laajimmin käytetyistä tekniikoista pelien, mobiili-, web- ja työpöytäsovellusten kehittämiseen. Koska Java on alustariippumaton, se toimii virheettömästi Windowsissa, Macissa, Linuxissa, Raspberry Pi:ssä jne. Java on hyvin samanlainen kuin C# ja C++, joten näiden kielten välillä on helpompi vaihtaa.

## Lyhyt historia ##

Java-projektin aloittivat kesäkuussa 1991 James Gosling, Mike Sheridan ja Patrick Naughton. Java oli alun perin nimeltään Oak. Myöhemmin se nimettiin uudelleen Greeniksi ja lopulta Javaksi. James Gosling suunnitteli Java-syntaksin, joka oli samanlainen kuin C/C++. Ensimmäisen julkisen Java-version julkaisi vuonna 1996 Sun Microsystems. Se voisi toimia kaikissa suosituissa järjestelmissä, mikä sai Javasta suositun nopeasti. Java 2:n julkaisun myötä joulukuussa 1998 rakennettiin useita kokoonpanoja erityyppisille alustoille. Versiot olivat seuraavat

- J2EE (Java EE): Yritysratkaisuille
- J2ME (Java ME): Mobiilisovelluksiin
- J2SE (Java SE): Työpöytäsovelluksiin

19. marraskuuta 2006 Sun julkaisi Java Virtual Machinen (JVM) ilmaisena ja avoimen lähdekoodin ohjelmistona. Oracle Corporationin ostettua Sun Microsystemsin vuosina 2009–2010 James Gosling erosi Oraclen palveluksesta 2. huhtikuuta 2010.

## Java-koodin ## suorittaminen/suorittaminen

Java-koodin suorittamiseksi se on ensin käännettävä. Tätä varten tarvitaan Java SDK. Java SDK kokoaa Java-koodin tavukoodiluokkatiedostoksi. On olemassa IDE:itä, kuten Eclipse ja IntelliJ Idea, jotka helpottavat Java-tiedostojen käsittelyä tarjoamalla koodin täydennyksen ja helppokäyttöisen käyttöliittymän Java-koodin kääntämiseen ja suorittamiseen.

## Java-tiedostomuoto ##

Java-syntaksiin vaikuttivat suuresti C ja C++, mutta toisin kuin C++, Java rakennettiin lähes yksinomaan olio-kieleksi. Javassa kaikki koodi kirjoitetaan luokkiin ja jokainen tietoyksikkö on objekti. Toisin kuin C++, Java ei tue operaattorin ylikuormitusta tai moninkertaista periytymistä.

### Java-esimerkkikoodi ###

Seuraavassa on esimerkki Java-syntaksista.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
Yllä olevassa koodissa **julkinen**-avainsana tarkoittaa pääsyn muokkaajaa. Siinä todetaan, että luokkahierarkian ulkopuoliset luokat voivat käyttää tätä luokkaa. Pääsymuunnin voi olla myös **suojattu** (pääsee samassa paketissa) tai **yksityinen** (metodeihin pääsee vain sama luokka). Metodin edessä oleva **staattinen** osoittaa, että menetelmä voidaan kutsua ilman tiettyä luokan esiintymää. **void** osoittaa, että menetelmä ei palauta mitään. Merkkijonon tulostaminen konsoliin. System.out.println-komentoa käytetään. Tässä komennossa *System*-luokassa on staattinen kenttä *out*, joka on *println*-menetelmän sisältävän *PrintStream*-luokan esiintymä.

Java-tiedostojen tiedostonimen tulee olla sama kuin luokan nimi. Joten esimerkkikoodin Java-tiedoston nimi olisi *ExampleApp.java*.

## Viitteet ##

- {{HYPERLINKKI}})

