---
date: 2022-07-30
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP Dosya Biçimi - JNP dosyası nedir?
linktitle: JNLP
description: "JNLP dosya formatı ve JNLP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## JNLP dosyası nedir?

JNLP dosyası, ağ üzerinden bir Java programı başlatmak için XML bilgilerini içeren bir Java Web Start (JWS) dosyasıdır. Java Ağ Başlatma Protokolü (JNLP) biçiminde kaydedilir. Bir uygulamayı indirmek ve çalıştırmak için bir uygulama dağıtım teknolojisi olan Java Web Start (JWS) teknolojisi tarafından kullanılır. Bir JNLP dosyası, programın indirildiği ve yerel makinede başlatıldığı sunucunun uzak adresini içerir.

## JNLP Dosya Biçimi - Daha Fazla Bilgi

JNLP dosyaları, insanlar tarafından okunabilir metin biçiminde saklanan **[XML](/tr/web/xml/)** dosyaları olarak kaydedilir. XML dosyası, ağ üzerinden bir Java uygulamasını başlatmak ve yürütmek için kullanılan bilgilere sahiptir. JWS, web sayfası bağlantısına tıklayarak uygulamaları başlatmanıza izin verir. Uygulama, kullanıcı bilgisayarına henüz indirilmemişse indirilir.

Oracle, Java Platform Standard Edition (JSE) 9'un piyasaya sürülmesiyle JWS'yi kullanımdan kaldırdı. Bununla, JNLP dosyaları artık desteklenmiyor.

### JNLP dosyaları nasıl açılır?

**JNLP dosyalarını açabilen** uygulamalar arasında **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** ve * bulunur. *GitHub Atom**.

### JNLP Dosya Örneği

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
**Kullanım**

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
## JNLP dosyaları nasıl çalıştırılır?

JWS'nin kullanımdan kaldırılmasıyla, JWS teknolojisine dayalı olarak geliştirilen uygulamalar, Java'nın en son sürümüyle çalıştırılamaz. Ancak bu JNLP tabanlı programlar, Java Web Start teknolojisinin açık kaynaklı yeniden uygulaması olan OpenWebStart kullanılarak çalıştırılabilir. Java'nın en son sürümüne paralel olarak yüklenir ve Java Web Start'ın en sık kullanılan özelliklerini ve JNLP standardını sağlar.

## Referanslar ##

* [Java Web Start nedir ve nasıl başlatılır?](https://www.java.com/en/download/help/java_webstart.html)
* [JNLP'yi En Son Java Sürümüyle Çalıştırın](https://openwebstart.com/)
* [Java Web Başlangıç - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

