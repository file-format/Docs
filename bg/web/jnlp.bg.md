---
date: 2022-07-30
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP файлов формат - Какво е JNP файл?
linktitle: JNLP
description: "Научете за файловия формат JNLP и API, които могат да създават и отварят JNLP файлове."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Какво е JNLP файл?

JNLP файл е Java Web Start (JWS) файл, който съдържа XML информация за стартиране на Java програма по мрежата. Записва се във формат Java Network Launching Protocol (JNLP). Използва се от технологията Java Web Start (JWS), която е технология за внедряване на приложение за изтегляне и стартиране на приложение. JNLP файлът съдържа отдалечения адрес на сървъра, от който програмата се изтегля и стартира на локална машина.

## JNLP файлов формат - повече информация

JNLP файловете се записват като **[XML](/bg/web/xml/)** файлове, които се съхраняват в четим от хора текстов формат. XML файлът съдържа информацията, която се използва за стартиране и изпълнение на Java приложение по мрежата. JWS ви позволява да стартирате приложения, като щракнете върху връзката към уеб страницата. Приложението се изтегля, в случай че вече не е изтеглено на компютъра на потребителя.

Oracle отхвърли JWS с пускането на Java Platform Standard Edition (JSE) 9. С това JNLP файловете вече не се поддържат.

### Как да отворите JNLP файлове?

Приложенията, които могат да **отварят JNLP файлове**, включват **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** и * *GitHub Atom**.

### Пример за JNLP файл

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
**Употреба**

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
## Как да стартирате JNLP файлове?

С оттеглянето на JWS приложенията, разработени на базата на технологията JWS, не могат да се изпълняват с най-новата версия на Java. Тези програми, базирани на JNLP, обаче могат да се изпълняват с помощта на OpenWebStart, който е реимплементация с отворен код на технологията Java Web Start. Инсталира се успоредно с най-новата версия на Java и предоставя най-често използваните функции на Java Web Start и стандарта JNLP.

## Препратки ##

* [Какво е Java Web Start и как се стартира?](https://www.java.com/en/download/help/java_webstart.html)
* [Стартирайте JNLP с най-новата версия на Java](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

