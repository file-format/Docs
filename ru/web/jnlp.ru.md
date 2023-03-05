---
date: 2022-07-30
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Формат файла JNLP. Что такое файл JNP?
linktitle: JNLP
description: "Узнайте о формате файла JNLP и API-интерфейсах, которые могут создавать и открывать файлы JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## .JNLP вариант №

Файл JNLP — это файл Java Web Start (JWS), который содержит XML-информацию для запуска программы Java по сети. Он сохраняется в формате Java Network Launching Protocol (JNLP). Он используется технологией Java Web Start (JWS), которая представляет собой технологию развертывания приложений для загрузки и запуска приложения. Файл JNLP содержит удаленный адрес сервера, с которого программа загружается и запускается на локальном компьютере.

## Формат файла JNLP — дополнительная информация

Файлы JNLP сохраняются в виде файлов **[XML](/ru/web/xml/)** в удобочитаемом текстовом формате. Файл XML содержит информацию, которая используется для запуска и выполнения приложения Java по сети. JWS позволяет запускать приложения, щелкнув ссылку на веб-страницу. Приложение загружается в том случае, если оно еще не загружено на компьютер пользователя.

Oracle объявила JWS устаревшей с выпуском Java Platform Standard Edition (JSE) 9. После этого файлы JNLP больше не поддерживаются.

### Как открыть файлы JNLP?

Приложения, которые могут **открывать файлы JNLP**, включают **Microsoft Visual Studio Code**, **Блокнот**, **Блокнот++**, **Oracle Java Web Start**, **Karakun OpenWebStart** и * *Атом GitHub**.

### Пример файла JNLP

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
**Применение**

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
## Как запустить файлы JNLP?

С прекращением поддержки JWS приложения, разработанные на основе технологии JWS, нельзя запускать с последней версией Java. Однако эти программы на основе JNLP можно запускать с помощью OpenWebStart, который является повторной реализацией технологии Java Web Start с открытым исходным кодом. Он устанавливается параллельно с последней версией Java и предоставляет наиболее часто используемые функции Java Web Start и стандарта JNLP.

## Использованная литература ##

* [Что такое Java Web Start и как он запускается?](https://www.java.com/en/download/help/java_webstart.html)
* [Запустите JNLP с последней версией Java](https://openwebstart.com/)
* [Java Web Start — Википедия](https://en.wikipedia.org/wiki/Java_Web_Start)

