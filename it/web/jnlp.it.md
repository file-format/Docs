---
date: 2022-07-30
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato file JNLP - Che cos'è un file JNP?
linktitle: JNLP
description: "Scopri il formato di file JNLP e le API che possono creare e aprire file JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Che cos'è un file JNLP?

Un file JNLP è un file Java Web Start (JWS) che contiene informazioni XML per l'avvio di un programma Java sulla rete. Viene salvato nel formato JNLP (Java Network Launching Protocol). Viene utilizzato dalla tecnologia Java Web Start (JWS), che è una tecnologia di distribuzione delle applicazioni per scaricare ed eseguire un'applicazione. Un file JNLP contiene l'indirizzo remoto del server da cui il programma viene scaricato e lanciato sulla macchina locale.

## Formato file JNLP - Ulteriori informazioni

I file JNLP vengono salvati come file **[XML](/it/web/xml/)** archiviati in un formato di testo leggibile. Il file XML contiene le informazioni utilizzate per avviare ed eseguire un'applicazione Java sulla rete. Il JWS consente di avviare le applicazioni facendo clic sul collegamento alla pagina Web. L'applicazione viene scaricata nel caso in cui non sia già stata scaricata sul computer dell'utente.

Oracle ha deprecato JWS con il rilascio di Java Platform Standard Edition (JSE) 9. Con questo, i file JNLP non sono più supportati.

### Come aprire i file JNLP?

Le applicazioni che possono **aprire file JNLP** includono **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** e * *GitHub Atom**.

### Esempio di file JNLP

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
**Utilizzo**

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
## Come eseguire file JNLP?

Con il ritiro di JWS, le applicazioni sviluppate sulla base della tecnologia JWS non possono essere eseguite con l'ultima versione di Java. Questi programmi basati su JNLP, tuttavia, possono essere eseguiti utilizzando OpenWebStart, che è una reimplementazione open source della tecnologia Java Web Start. Si installa in parallelo all'ultima versione di Java e fornisce le funzioni più comunemente utilizzate di Java Web Start e lo standard JNLP.

## Riferimenti ##

* [Cos'è Java Web Start e come viene avviato?](https://www.java.com/en/download/help/java_webstart.html)
* [Esegui JNLP con l'ultima versione di Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

