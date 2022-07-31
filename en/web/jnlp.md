---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP File Format - What is a JNP file?
linktitle: JNLP
description: Learn about JNLP file format and APIs that can create and open JNLP files.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## What is a JNLP file?

A JNLP file is a Java Web Start (JWS) file that contains XML information for launching a Java program over the network. It is saved in Java Network Launching Protocol (JNLP) format. It is used by the Java Web Start (JWS) technology that is an application deployment technology to download and run an application. A JNLP file contains the remote address of the server from which the program is downloaded and launched on local machine.

## JNLP File Format - More Information

JNLP files are saved as **[XML](/web/xml/)** files that are stored in human-readable text format. The XML file has the information that is used to launch and execute a Java application over the network. The JWS lets you launch applications by clicking the web page link. The application is downloaded in case it is not already downloaded on the user computer.

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. With this, JNLP files are no more supported.

### How to Open JNLP files?

Applications that can **open JNLP files** include **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**,  **Oracle Java Web Start**, **Karakun OpenWebStart**, and **GitHub Atom**.

### JNLP File Example

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
## How to Run JNLP files?

With the deprecation of JWS, applications developed based on JWS technology can't be run with the latest version of Java. These JNLP based programs, however, can be run using OpenWebStart that is an open source reimplementation of the Java Web Start technology. It installs in parallel to the latest version of Java and provides the most commonly used features of Java Web Start and the JNLP standard.  

## References ##

* [What is Java Web Start and How it is launched?](https://www.java.com/en/download/help/java_webstart.html)
* [Run JNLP with Latest Version of Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)
