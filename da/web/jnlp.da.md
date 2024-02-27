---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP-filformat - Hvad er en JNP-file?
linktitle: JNLP
description: Ltjene om JNLP filformat og API'er, der kan oprette og åbne JNLP fils.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Hvad er JNLP fil?

En JNLP-fil er en Java Web Start-fil (JWS), der indeholder XML-information til at starte et Java-program over netværket. Det er gemt i Java Network Launching Protocol (JNLP) format. Den bruges af Java Web Start-teknologien (JWS), som er en applikationsimplementeringsteknologi til at downloade og køre en applikation. En JNLP-fil indeholder fjernadressen på den server, hvorfra programmet downloades og startes på den lokale maskine.

## JNLP-filformat - flere oplysninger

JNLP-filer gemmes som **[XML](/web/xml/)**-filer, der er gemt i et menneskeligt læsbart tekstformat. XML-filen har de oplysninger, der bruges til at starte og udføre en Java-applikation over netværket. JWS lader dig starte applikationer ved at klikke på websidelinket. Applikationen downloades, hvis den ikke allerede er downloadet på brugerens computer.

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. Med dette understøttes JNLP-filer ikke længere.

### Hvordan åbner man JNLP filer?

Programmer, der kan **åbne JNLP-filer** inkluderer **Microsoft Visual Studio Code**, **Notesblok**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** og * *GitHub Atom**.

### JNLP-fileksempel

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
**Brug**

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
## Hvordan kører jeg JNLP filer?

Med udfasningen af JWS kan applikationer udviklet baseret på JWS-teknologi ikke køres med den nyeste version af Java. Disse JNLP-baserede programmer kan dog køres ved hjælp af OpenWebStart, som er en open source-genimplementering af Java Web Start-teknologien. Den installeres parallelt med den nyeste version af Java og giver de mest almindeligt anvendte funktioner i Java Web Start og JNLP-standarden.

## Referencer ##

* [Hvad er Java Web Start, og hvordan lanceres det?](https://www.java.com/en/download/help/java_webstart.html)

* [Kør JNLP med den nyeste version af Java](https://openwebstart.com/)

* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)


