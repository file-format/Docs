---
date: 2022-07-30
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formát souboru JNLP - Co je soubor JNP?
linktitle: JNLP
description: "Přečtěte si o formátu souborů JNLP a rozhraních API, která mohou vytvářet a otevírat soubory JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Co je soubor JNLP?

Soubor JNLP je soubor Java Web Start (JWS), který obsahuje informace XML pro spouštění programu Java přes síť. Je uložen ve formátu JNLP (Java Network Launching Protocol). Používá ji technologie Java Web Start (JWS), což je technologie nasazení aplikací ke stažení a spuštění aplikace. Soubor JNLP obsahuje vzdálenou adresu serveru, ze kterého je program stažen a spuštěn na místním počítači.

## Formát souboru JNLP – Další informace

Soubory JNLP se ukládají jako soubory **[XML](/cs/web/xml/)**, které jsou uloženy v textovém formátu čitelném pro člověka. Soubor XML obsahuje informace, které se používají ke spuštění a spuštění aplikace Java přes síť. JWS umožňuje spouštět aplikace kliknutím na odkaz na webovou stránku. Aplikace se stáhne v případě, že již není stažena na počítači uživatele.

Oracle ukončil podporu JWS vydáním Java Platform Standard Edition (JSE) 9. Díky tomu již nejsou soubory JNLP podporovány.

### Jak otevřít soubory JNLP?

Mezi aplikace, které mohou **otevřít soubory JNLP**, patří **Microsoft Visual Studio Code**, **Poznámkový blok**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** a * *GitHub Atom**.

### Příklad souboru JNLP

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
**Používání**

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
## Jak spustit soubory JNLP?

S ukončením podpory JWS nelze aplikace vyvinuté na základě technologie JWS spouštět s nejnovější verzí Javy. Tyto programy založené na JNLP však lze spouštět pomocí OpenWebStart, což je open source reimplementace technologie Java Web Start. Instaluje se paralelně s nejnovější verzí Javy a poskytuje nejčastěji používané funkce Java Web Start a standardu JNLP.

## Reference ##

* [Co je Java Web Start a jak se spouští?](https://www.java.com/en/download/help/java_webstart.html)
* [Spusťte JNLP s nejnovější verzí Javy] (https://openwebstart.com/)
* [Java Web Start – Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

