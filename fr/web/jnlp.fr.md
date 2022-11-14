---
date: 2022-07-30
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fichier JNLP - Qu'est-ce qu'un fichier JNP ?
linktitle: JNLP
description: "Découvrez le format de fichier JNLP et les API qui peuvent créer et ouvrir des fichiers JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Qu'est-ce qu'un fichier JNLP ?

Un fichier JNLP est un fichier Java Web Start (JWS) qui contient des informations XML pour lancer un programme Java sur le réseau. Il est enregistré au format Java Network Launching Protocol (JNLP). Il est utilisé par la technologie Java Web Start (JWS) qui est une technologie de déploiement d'application pour télécharger et exécuter une application. Un fichier JNLP contient l'adresse distante du serveur à partir duquel le programme est téléchargé et lancé sur la machine locale.

## Format de fichier JNLP - Plus d'informations

Les fichiers JNLP sont enregistrés en tant que fichiers **[XML](/fr/web/xml/)** stockés dans un format texte lisible par l'homme. Le fichier XML contient les informations utilisées pour lancer et exécuter une application Java sur le réseau. Le JWS vous permet de lancer des applications en cliquant sur le lien de la page Web. L'application est téléchargée si elle n'est pas déjà téléchargée sur l'ordinateur de l'utilisateur.

Oracle a déprécié JWS avec la sortie de Java Platform Standard Edition (JSE) 9. Avec cela, les fichiers JNLP ne sont plus pris en charge.

### Comment ouvrir les fichiers JNLP ?

Les applications pouvant **ouvrir les fichiers JNLP** incluent **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** et * *GitHub Atom**.

### Exemple de fichier JNLP

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
**Usage**

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
## Comment exécuter les fichiers JNLP ?

Avec l'obsolescence de JWS, les applications développées sur la base de la technologie JWS ne peuvent pas être exécutées avec la dernière version de Java. Cependant, ces programmes basés sur JNLP peuvent être exécutés à l'aide d'OpenWebStart qui est une réimplémentation open source de la technologie Java Web Start. Il s'installe en parallèle de la dernière version de Java et fournit les fonctionnalités les plus couramment utilisées de Java Web Start et du standard JNLP.

## Références ##

* [Qu'est-ce que Java Web Start et comment est-il lancé ?](https://www.java.com/en/download/help/java_webstart.html)
* [Exécutez JNLP avec la dernière version de Java] (https://openwebstart.com/)
* [Java Web Start - Wikipédia](https://en.wikipedia.org/wiki/Java_Web_Start)

