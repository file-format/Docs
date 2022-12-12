---
date: 2022-07-30
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format pliku JNLP - Co to jest plik JNP?
linktitle: JNLP
description: "Dowiedz się więcej o formacie pliku JNLP i interfejsach API, które umożliwiają tworzenie i otwieranie plików JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Czym jest plik JNLP?

Plik JNLP to plik Java Web Start (JWS), który zawiera informacje XML do uruchamiania programu Java przez sieć. Jest zapisany w formacie Java Network Launching Protocol (JNLP). Jest używany przez technologię Java Web Start (JWS), która jest technologią wdrażania aplikacji do pobierania i uruchamiania aplikacji. Plik JNLP zawiera zdalny adres serwera, z którego program jest pobierany i uruchamiany na komputerze lokalnym.

## Format pliku JNLP — więcej informacji

Pliki JNLP są zapisywane jako pliki **[XML](/pl/web/xml/)** w formacie tekstowym czytelnym dla człowieka. Plik XML zawiera informacje używane do uruchamiania i wykonywania aplikacji Java w sieci. JWS umożliwia uruchamianie aplikacji poprzez kliknięcie łącza do strony internetowej. Aplikacja jest pobierana, jeśli nie została jeszcze pobrana na komputerze użytkownika.

Firma Oracle wycofała JWS wraz z wydaniem Java Platform Standard Edition (JSE) 9. Dzięki temu pliki JNLP nie są już obsługiwane.

### Jak otworzyć pliki JNLP?

Aplikacje, które mogą **otwierać pliki JNLP**, to **Microsoft Visual Studio Code**, **Notatnik**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** i * *GitHub Atom**.

### Przykład pliku JNLP

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
**Stosowanie**

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
## Jak uruchomić pliki JNLP?

Wraz z wycofaniem JWS aplikacje opracowane w oparciu o technologię JWS nie mogą działać z najnowszą wersją Javy. Te programy oparte na JNLP można jednak uruchamiać przy użyciu OpenWebStart, który jest otwartą reimplementacją technologii Java Web Start. Instaluje się równolegle z najnowszą wersją Java i zapewnia najczęściej używane funkcje Java Web Start i standard JNLP.

## Bibliografia ##

* [Co to jest Java Web Start i jak jest uruchamiana?](https://www.java.com/en/download/help/java_webstart.html)
* [Uruchom JNLP z najnowszą wersją Java](https://openwebstart.com/)
* [Java Web Start – Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

