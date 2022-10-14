---
date: 2022-07-30
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "JNLP-Dateiformat - Was ist eine JNP-Datei?"
linktitle: "JNLP"
description: "Erfahren Sie mehr über das JNLP-Dateiformat und APIs, die JNLP-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Was ist eine JNLP-Datei?

Eine JNLP-Datei ist eine Java Web Start (JWS)-Datei, die XML-Informationen zum Starten eines Java-Programms über das Netzwerk enthält. Es wird im JNLP-Format (Java Network Launching Protocol) gespeichert. Es wird von der Java Web Start (JWS)-Technologie verwendet, die eine Anwendungsbereitstellungstechnologie zum Herunterladen und Ausführen einer Anwendung ist. Eine JNLP-Datei enthält die entfernte Adresse des Servers, von dem das Programm heruntergeladen und auf dem lokalen Computer gestartet wird.

## JNLP-Dateiformat – Weitere Informationen

JNLP-Dateien werden als **[XML](/de/web/xml/)**-Dateien gespeichert, die in einem für Menschen lesbaren Textformat gespeichert sind. Die XML-Datei enthält die Informationen, die zum Starten und Ausführen einer Java-Anwendung über das Netzwerk verwendet werden. Mit dem JWS können Sie Anwendungen starten, indem Sie auf den Webseitenlink klicken. Die Anwendung wird heruntergeladen, falls sie nicht bereits auf den Computer des Benutzers heruntergeladen wurde.

Oracle hat JWS mit der Veröffentlichung von Java Platform Standard Edition (JSE) 9 als veraltet markiert. Damit werden JNLP-Dateien nicht mehr unterstützt.

### Wie öffnet man JNLP-Dateien?

Zu den Anwendungen, die **JNLP-Dateien öffnen** können, gehören **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** und * *GitHub-Atom**.

### JNLP-Dateibeispiel

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
**Verwendungszweck**

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
## Wie führt man JNLP-Dateien aus?

Mit der Einstellung von JWS können Anwendungen, die auf der Grundlage der JWS-Technologie entwickelt wurden, nicht mit der neuesten Version von Java ausgeführt werden. Diese JNLP-basierten Programme können jedoch mit OpenWebStart ausgeführt werden, das eine Open-Source-Neuimplementierung der Java Web Start-Technologie ist. Es wird parallel zur neuesten Version von Java installiert und bietet die am häufigsten verwendeten Funktionen von Java Web Start und dem JNLP-Standard.

## Verweise ##

* [Was ist Java Web Start und wie wird es gestartet?](https://www.java.com/en/download/help/java_webstart.html)
* [JNLP mit der neuesten Java-Version ausführen](https://openwebstart.com/)
* [Java Web Start – Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

