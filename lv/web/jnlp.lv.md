---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP faila formāts — kas ir JNP failse?
linktitle: JNLP
description: Lnopelniet par JNLP faila formātu un API, kas var izveidot un atvērt JNLP failus.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Kas ir JNLP fails?

JNLP fails ir Java Web Start (JWS) fails, kas satur XML informāciju Java programmas palaišanai tīklā. Tas tiek saglabāts Java tīkla palaišanas protokola (JNLP) formātā. To izmanto Java Web Start (JWS) tehnoloģija, kas ir lietojumprogrammu izvietošanas tehnoloģija, lai lejupielādētu un palaistu lietojumprogrammu. JNLP failā ir tā servera attālā adrese, no kura programma tiek lejupielādēta un palaista vietējā datorā.

## JNLP faila formāts — vairāk informācijas

JNLP faili tiek saglabāti kā **[XML](/web/xml/)** faili, kas tiek saglabāti cilvēkiem lasāmā teksta formātā. XML failā ir informācija, kas tiek izmantota Java lietojumprogrammas palaišanai un izpildei tīklā. JWS ļauj palaist lietojumprogrammas, noklikšķinot uz tīmekļa lapas saites. Lietojumprogramma tiek lejupielādēta, ja tā vēl nav lejupielādēta lietotāja datorā.

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. Tādējādi JNLP faili vairs netiek atbalstīti.

### Kā atvērt JNLP failus?

Lietojumprogrammas, kas var **atvērt JNLP failus**, ietver **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** un * *GitHub Atom**.

### JNLP faila piemērs

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
**Lietošana**

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
## Kā palaist JNLP failus?

Līdz ar JWS novecošanos lietojumprogrammas, kas izstrādātas, pamatojoties uz JWS tehnoloģiju, nevar palaist ar jaunāko Java versiju. Tomēr šīs uz JNLP balstītās programmas var palaist, izmantojot OpenWebStart, kas ir Java Web Start tehnoloģijas atvērtā koda atkārtota ieviešana. Tā tiek instalēta paralēli jaunākajai Java versijai un nodrošina visbiežāk izmantotās Java Web Start un JNLP standarta funkcijas.

## Atsauces Nr.

* [Kas ir Java Web Start un kā tas tiek palaists?](https://www.java.com/en/download/help/java_webstart.html)

* [Palaidiet JNLP ar jaunāko Java versiju](https://openwebstart.com/)

* [Java Web Start — Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)


