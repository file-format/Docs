---
date: 2022-07-30
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP-bestandsindeling - Wat is een JNP-bestand?
linktitle: JNLP
description: "Meer informatie over de JNLP-bestandsindeling en API's die JNLP-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Wat is een JNLP-bestand?

Een JNLP-bestand is een Java Web Start (JWS)-bestand dat XML-informatie bevat voor het starten van een Java-programma via het netwerk. Het wordt opgeslagen in het Java Network Launching Protocol (JNLP) formaat. Het wordt gebruikt door de Java Web Start-technologie (JWS), een technologie voor applicatie-implementatie om een applicatie te downloaden en uit te voeren. Een JNLP-bestand bevat het externe adres van de server waarvan het programma is gedownload en gestart op de lokale computer.

## JNLP-bestandsindeling - Meer informatie

JNLP-bestanden worden opgeslagen als **[XML](/nl/web/xml/)**-bestanden die zijn opgeslagen in een voor mensen leesbare tekstindeling. Het XML-bestand bevat de informatie die wordt gebruikt om een Java-toepassing via het netwerk te starten en uit te voeren. Met de JWS kunt u toepassingen starten door op de koppeling naar de webpagina te klikken. De toepassing wordt gedownload voor het geval deze nog niet op de computer van de gebruiker is gedownload.

Oracle deprecieerde JWS met de release van Java Platform Standard Edition (JSE) 9. Hiermee worden JNLP-bestanden niet meer ondersteund.

### Hoe JNLP-bestanden openen?

Toepassingen die **JNLP-bestanden** kunnen openen** zijn onder meer **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** en * *GitHub-atoom**.

### JNLP-bestandsvoorbeeld

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
**Gebruik**

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
## Hoe JNLP-bestanden uit te voeren?

Met de afschaffing van JWS kunnen applicaties die zijn ontwikkeld op basis van JWS-technologie niet worden uitgevoerd met de nieuwste versie van Java. Deze op JNLP gebaseerde programma's kunnen echter worden uitgevoerd met OpenWebStart, een open source herimplementatie van de Java Web Start-technologie. Het wordt parallel met de nieuwste versie van Java geïnstalleerd en biedt de meest gebruikte functies van Java Web Start en de JNLP-standaard.

## Referenties ##

* [Wat is Java Web Start en hoe wordt het gelanceerd?](https://www.java.com/en/download/help/java_webstart.html)
* [Voer JNLP uit met de nieuwste versie van Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

