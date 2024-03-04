---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP failo formatas – kas yra JNP failase?
linktitle: JNLP
description: Luždirbti apie JNLP failo formatą ir API, kurios gali sukurti ir atidaryti JNLP failąs.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Kas yra JNLP failas?

JNLP failas yra Java Web Start (JWS) failas, kuriame yra XML informacija, skirta Java programai paleisti tinkle. Jis išsaugomas Java Network Launching Protocol (JNLP) formatu. Ją naudoja Java Web Start (JWS) technologija, kuri yra programos diegimo technologija, skirta programai atsisiųsti ir paleisti. JNLP faile yra nuotolinis serverio, iš kurio programa atsisiunčiama ir paleidžiama vietiniame kompiuteryje, adresas.

## JNLP failo formatas – daugiau informacijos

JNLP failai išsaugomi kaip **[XML](/web/xml/)** failai, kurie saugomi žmonėms suprantamu teksto formatu. XML faile yra informacija, kuri naudojama Java programai paleisti ir vykdyti tinkle. JWS leidžia paleisti programas spustelėjus tinklalapio nuorodą. Programa atsisiunčiama, jei ji dar neatsisiųsta vartotojo kompiuteryje.

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. Dėl to JNLP failai nebepalaikomi.

### Kaip atidaryti JNLP failus?

Programos, kurios gali **atidaryti JNLP failus**, apima **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** ir * *GitHub Atom**.

### JNLP failo pavyzdys

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
**Naudojimas**

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
## Kaip paleisti JNLP failus?

Nustojus naudoti JWS, programos, sukurtos remiantis JWS technologija, negali būti paleidžiamos naudojant naujausią Java versiją. Tačiau šias JNLP pagrįstas programas galima paleisti naudojant OpenWebStart, kuri yra atvirojo kodo Java Web Start technologijos pakartotinis įgyvendinimas. Jis įdiegiamas lygiagrečiai su naujausia Java versija ir pateikia dažniausiai naudojamas Java Web Start ir JNLP standarto funkcijas.

## Nuorodos Nr.

* [Kas yra „Java Web Start“ ir kaip ji paleidžiama?](https://www.java.com/en/download/help/java_webstart.html)

* [Paleiskite JNLP su naujausia Java versija](https://openwebstart.com/)

* [Java Web Start – Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)


