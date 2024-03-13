---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP fayl formatı - JNP faylı nədire?
linktitle: JNLP
description: LJNLP fayl formatı və JNLP faylını yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## JNLP faylı nədir?

JNLP faylı şəbəkə üzərindən Java proqramını işə salmaq üçün XML məlumatını ehtiva edən Java Web Start (JWS) faylıdır. Java Network Launching Protocol (JNLP) formatında saxlanılır. Proqramı yükləmək və işə salmaq üçün proqram yerləşdirmə texnologiyası olan Java Web Start (JWS) texnologiyası tərəfindən istifadə olunur. JNLP faylı proqramın yükləndiyi və yerli maşında işə salındığı serverin uzaq ünvanını ehtiva edir.

## JNLP Fayl Format - Ətraflı Məlumat

JNLP faylları insan tərəfindən oxuna bilən mətn formatında saxlanılan **[XML](/web/xml/)** faylları kimi saxlanılır. XML faylı şəbəkə üzərindən Java proqramını işə salmaq və icra etmək üçün istifadə olunan məlumatlara malikdir. JWS veb-səhifə linkinə klikləməklə proqramları işə salmağa imkan verir. Tətbiq istifadəçi kompüterinə yüklənmədiyi halda yüklənir.

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. Bununla JNLP faylları daha dəstəklənmir.

### JNLP fayllarını necə açmaq olar?

**JNLP fayllarını** aça bilən proqramlara **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** və * daxildir. *GitHub Atom**.

### JNLP fayl nümunəsi

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
**İstifadə**

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
## JNLP fayllarını necə işə salmaq olar?

JWS-in köhnəlməsi ilə JWS texnologiyası əsasında hazırlanmış proqramlar Java-nın ən son versiyası ilə işlənə bilməz. Bununla belə, bu JNLP əsaslı proqramlar Java Web Start texnologiyasının açıq mənbə reinmplementasiyası olan OpenWebStart istifadə edərək işlədilə bilər. O, Java-nın ən son versiyasına paralel olaraq quraşdırılır və Java Web Start və JNLP standartının ən çox istifadə olunan xüsusiyyətlərini təmin edir.

## İstinadlar ##

* [Java Web Start nədir və necə işə salınır?](https://www.java.com/en/download/help/java_webstart.html)

* [JNLP-ni Java-nın ən son versiyası ilə işə salın](https://openwebstart.com/)

* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)


