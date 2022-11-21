---
date: 2022-07-30
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato de arquivo JNLP - O que é um arquivo JNP?
linktitle: JNLP
description: "Saiba mais sobre o formato de arquivo JNLP e APIs que podem criar e abrir arquivos JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## O que é um arquivo JNLP?

Um arquivo JNLP é um arquivo Java Web Start (JWS) que contém informações XML para iniciar um programa Java na rede. Ele é salvo no formato Java Network Launching Protocol (JNLP). Ele é usado pela tecnologia Java Web Start (JWS), que é uma tecnologia de implantação de aplicativo para fazer download e executar um aplicativo. Um arquivo JNLP contém o endereço remoto do servidor do qual o programa é baixado e iniciado na máquina local.

## Formato de arquivo JNLP - Mais informações

Os arquivos JNLP são salvos como arquivos **[XML](/pt/web/xml/)** que são armazenados em formato de texto legível por humanos. O arquivo XML contém as informações usadas para iniciar e executar um aplicativo Java na rede. O JWS permite iniciar aplicativos clicando no link da página da web. O aplicativo é baixado caso ainda não tenha sido baixado no computador do usuário.

A Oracle desativou o JWS com o lançamento do Java Platform Standard Edition (JSE) 9. Com isso, os arquivos JNLP não são mais suportados.

### Como abrir arquivos JNLP?

Os aplicativos que podem **abrir arquivos JNLP** incluem **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** e * *GitHub Atom**.

### Exemplo de arquivo JNLP

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
## Como executar arquivos JNLP?

Com a descontinuação do JWS, os aplicativos desenvolvidos com base na tecnologia JWS não podem ser executados com a versão mais recente do Java. Esses programas baseados em JNLP, no entanto, podem ser executados usando OpenWebStart, que é uma reimplementação de código aberto da tecnologia Java Web Start. Ele é instalado em paralelo com a versão mais recente do Java e fornece os recursos mais usados do Java Web Start e do padrão JNLP.

## Referências ##

* [O que é o Java Web Start e como ele é iniciado?](https://www.java.com/en/download/help/java_webstart.html)
* [Execute o JNLP com a versão mais recente do Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

