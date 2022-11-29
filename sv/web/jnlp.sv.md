---
date: 2022-07-30
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP-filformat - Vad är en JNP-fil?
linktitle: JNLP
description: "Lär dig om JNLP-filformat och API:er som kan skapa och öppna JNLP-filer." 
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Vad är JNLP fil?

En JNLP-fil är en Java Web Start-fil (JWS) som innehåller XML-information för att starta ett Java-program över nätverket. Den sparas i formatet Java Network Launching Protocol (JNLP). Den används av Java Web Start-tekniken (JWS) som är en applikationsdistributionsteknik för att ladda ner och köra en applikation. En JNLP-fil innehåller fjärradressen till servern från vilken programmet laddas ner och startas på lokal maskin.

## JNLP-filformat - Mer information

JNLP-filer sparas som **[XML](/sv/web/xml/)**-filer som lagras i läsbart textformat. XML-filen har informationen som används för att starta och köra en Java-applikation över nätverket. JWS låter dig starta applikationer genom att klicka på länken till webbsidan. Applikationen laddas ner om den inte redan är nedladdad på användarens dator.

Oracle fasade ut JWS med lanseringen av Java Platform Standard Edition (JSE) 9. Med detta stöds inte längre JNLP-filer.

### Hur öppnar man JNLP-filer?

Applikationer som kan **öppna JNLP-filer** inkluderar **Microsoft Visual Studio Code**, **Anteckningar**, **Anteckningar++**, **Oracle Java Web Start**, **Karakun OpenWebStart** och * *GitHub Atom**.

### JNLP-filexempel

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
**Användande**

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
## Hur kör man JNLP-filer?

Med utfasningen av JWS kan applikationer utvecklade baserade på JWS-teknik inte köras med den senaste versionen av Java. Dessa JNLP-baserade program kan dock köras med OpenWebStart som är en återimplementering av Java Web Start-tekniken med öppen källkod. Den installeras parallellt med den senaste versionen av Java och tillhandahåller de mest använda funktionerna i Java Web Start och JNLP-standarden.

## Referenser ##

* [Vad är Java Web Start och hur det lanseras?](https://www.java.com/en/download/help/java_webstart.html)
* [Kör JNLP med senaste versionen av Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

