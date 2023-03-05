---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "Formato de archivo JNLP: ¿qué es un archivo JNP?"
linktitle: JNLP
description: "Obtenga información sobre el formato de archivo JNLP y las API que pueden crear y abrir archivos JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## ¿Qué es un archivo JNLP?

Un archivo JNLP es un archivo Java Web Start (JWS) que contiene información XML para iniciar un programa Java a través de la red. Se guarda en formato Java Network Launching Protocol (JNLP). Lo utiliza la tecnología Java Web Start (JWS), que es una tecnología de implementación de aplicaciones para descargar y ejecutar una aplicación. Un archivo JNLP contiene la dirección remota del servidor desde el cual se descarga y ejecuta el programa en la máquina local.

## Formato de archivo JNLP - Más información

Los archivos JNLP se guardan como archivos **[XML](/es/web/xml/)** que se almacenan en formato de texto legible por humanos. El archivo XML tiene la información que se utiliza para iniciar y ejecutar una aplicación Java en la red. El JWS le permite iniciar aplicaciones haciendo clic en el enlace de la página web. La aplicación se descarga en caso de que no esté ya descargada en la computadora del usuario.

Oracle dejó de usar JWS con el lanzamiento de Java Platform Standard Edition (JSE) 9. Con esto, los archivos JNLP ya no son compatibles.

### ¿Cómo abrir archivos JNLP?

Las aplicaciones que pueden **abrir archivos JNLP** incluyen **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** y * *Átomo de GitHub**.

### Ejemplo de archivo JNLP

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
**Uso**

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
## ¿Cómo ejecutar archivos JNLP?

Con la desaprobación de JWS, las aplicaciones desarrolladas en base a la tecnología JWS no se pueden ejecutar con la última versión de Java. Sin embargo, estos programas basados en JNLP se pueden ejecutar con OpenWebStart, que es una reimplementación de código abierto de la tecnología Java Web Start. Se instala en paralelo con la última versión de Java y proporciona las funciones más utilizadas de Java Web Start y el estándar JNLP.

## Referencias ##

* [¿Qué es Java Web Start y cómo se inicia?](https://www.java.com/en/download/help/java_webstart.html)
* [Ejecute JNLP con la última versión de Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

