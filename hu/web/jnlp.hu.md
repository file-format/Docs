---
date: 2022-07-30
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP fájlformátum - Mi az a JNP fájl?
linktitle: JNLP
description: "Ismerje meg a JNLP fájlformátumot és az API-kat, amelyek JNLP fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Mi az a JNLP fájl?

A JNLP fájl egy Java Web Start (JWS) fájl, amely XML információkat tartalmaz Java programok hálózaton keresztüli indításához. Java Network Launching Protocol (JNLP) formátumban van elmentve. Ezt a Java Web Start (JWS) technológia használja, amely egy alkalmazástelepítési technológia egy alkalmazások letöltésére és futtatására. A JNLP fájl tartalmazza annak a kiszolgálónak a távoli címét, amelyről a program letöltődik, és elindul a helyi gépen.

## JNLP fájlformátum - További információ

A JNLP-fájlok **[XML](/hu/web/xml/)**-fájlokként kerülnek mentésre, amelyeket ember által olvasható szövegformátumban tárolnak. Az XML-fájl tartalmazza a Java-alkalmazások hálózaton keresztüli elindításához és futtatásához használt információkat. A JWS lehetővé teszi alkalmazások indítását a weboldal hivatkozására kattintva. Az alkalmazás letöltődik, ha még nincs letöltve a felhasználó számítógépére.

Az Oracle a Java Platform Standard Edition (JSE) 9 kiadásával elavult JWS-t. Ezzel a JNLP-fájlok már nem támogatottak.

### Hogyan lehet megnyitni a JNLP fájlokat?

A **JNLP-fájlok megnyitására** alkalmas alkalmazások közé tartozik a **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** és * *GitHub Atom**.

### JNLP fájl példa

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
**Használat**

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
## Hogyan kell futtatni a JNLP fájlokat?

A JWS megszűnésével a JWS technológián alapuló alkalmazások nem futtathatók a Java legújabb verziójával. Ezek a JNLP alapú programok azonban futtathatók az OpenWebStart segítségével, amely a Java Web Start technológia nyílt forráskódú újramegvalósítása. A Java legújabb verziójával párhuzamosan települ, és biztosítja a Java Web Start és a JNLP szabvány leggyakrabban használt szolgáltatásait.

## Referenciák ##

* [Mi az a Java Web Start, és hogyan indul?](https://www.java.com/en/download/help/java_webstart.html)
* [Futtassa a JNLP-t a Java legújabb verziójával](https://openwebstart.com/)
* [Java Web Start – Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

