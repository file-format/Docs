---
date: 2022-07-30
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Формат файлу JNLP - Що таке файл JNP?
linktitle: JNLP
description: "Дізнайтеся про формат файлів JNLP та API, які можуть створювати та відкривати файли JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Що таке файл JNLP?

Файл JNLP — це файл Java Web Start (JWS), який містить інформацію XML для запуску програми Java через мережу. Він зберігається у форматі Java Network Launching Protocol (JNLP). Він використовується технологією Java Web Start (JWS), яка є технологією розгортання програми для завантаження та запуску програми. Файл JNLP містить віддалену адресу сервера, з якого програма завантажується та запускається на локальній машині.

## Формат файлу JNLP - Додаткова інформація

Файли JNLP зберігаються як файли **[XML](/uk/web/xml/)**, які зберігаються в зручному для читання текстовому форматі. Файл XML містить інформацію, яка використовується для запуску та виконання програми Java через мережу. JWS дозволяє запускати програми, натиснувши посилання на веб-сторінку. Програма завантажується, якщо вона ще не завантажена на комп’ютер користувача.

Oracle припинив підтримку JWS із випуском Java Platform Standard Edition (JSE) 9. Після цього файли JNLP більше не підтримуються.

### Як відкрити файли JNLP?

Програми, які можуть **відкривати файли JNLP**, включають **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** і * *GitHub Atom**.

### Приклад файлу JNLP

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
**Використання**

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
## Як запустити файли JNLP?

Після припинення підтримки JWS програми, розроблені на основі технології JWS, не можна запускати з останньою версією Java. Однак ці програми на основі JNLP можна запускати за допомогою OpenWebStart, який є повторним впровадженням технології Java Web Start з відкритим кодом. Він встановлюється паралельно з останньою версією Java та надає найбільш часто використовувані функції Java Web Start і стандарту JNLP.

## Посилання ##

* [Що таке Java Web Start і як його запускати?](https://www.java.com/en/download/help/java_webstart.html)
* [Запустіть JNLP з останньою версією Java](https://openwebstart.com/)
* [Java Web Start – Вікіпедія](https://en.wikipedia.org/wiki/Java_Web_Start)

