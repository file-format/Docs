---
date: 2022-07-30
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fișier JNLP - Ce este un fișier JNP?
linktitle: JNLP
description: "Aflați despre formatul de fișier JNLP și despre API-urile care pot crea și deschide fișiere JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Ce este un fișier JNLP?

Un fișier JNLP este un fișier Java Web Start (JWS) care conține informații XML pentru lansarea unui program Java în rețea. Este salvat în format Java Network Launching Protocol (JNLP). Este folosit de tehnologia Java Web Start (JWS), care este o tehnologie de implementare a aplicațiilor pentru a descărca și rula o aplicație. Un fișier JNLP conține adresa de la distanță a serverului de pe care programul este descărcat și lansat pe mașina locală.

## Format de fișier JNLP - Mai multe informații

Fișierele JNLP sunt salvate ca fișiere **[XML](/ro/web/xml/)** care sunt stocate în format text care poate fi citit de om. Fișierul XML conține informațiile care sunt utilizate pentru a lansa și executa o aplicație Java prin rețea. JWS vă permite să lansați aplicații făcând clic pe linkul paginii web. Aplicația se descarcă în cazul în care nu este deja descărcată pe computerul utilizatorului.

Oracle a depreciat JWS odată cu lansarea Java Platform Standard Edition (JSE) 9. Prin aceasta, fișierele JNLP nu mai sunt acceptate.

### Cum se deschide fișierele JNLP?

Aplicațiile care pot **deschide fișierele JNLP** includ **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** și * *GitHub Atom**.

### Exemplu de fișier JNLP

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
**Utilizare**

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
## Cum să rulați fișierele JNLP?

Odată cu deprecierea JWS, aplicațiile dezvoltate pe baza tehnologiei JWS nu pot fi rulate cu cea mai recentă versiune de Java. Aceste programe bazate pe JNLP, totuși, pot fi rulate folosind OpenWebStart, care este o reimplementare open source a tehnologiei Java Web Start. Se instalează în paralel cu cea mai recentă versiune de Java și oferă cele mai frecvent utilizate caracteristici ale Java Web Start și standardul JNLP.

## Referințe ##

* [Ce este Java Web Start și cum este lansat?](https://www.java.com/en/download/help/java_webstart.html)
* [Rulează JNLP cu cea mai recentă versiune de Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

