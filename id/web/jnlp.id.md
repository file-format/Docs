---
date: 2022-07-30
pengarang:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format File JNLP - Apa itu file JNP?
linktitle: JNLP
description: "Pelajari tentang format file JNLP dan API yang dapat membuat dan membuka file JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Apa itu file JNLP?

File JNLP adalah file Java Web Start (JWS) yang berisi informasi XML untuk meluncurkan program Java melalui jaringan. Itu disimpan dalam format Java Network Launching Protocol (JNLP). Ini digunakan oleh teknologi Java Web Start (JWS) yang merupakan teknologi penerapan aplikasi untuk mengunduh dan menjalankan aplikasi. File JNLP berisi alamat jarak jauh server tempat program diunduh dan diluncurkan di mesin lokal.

## Format File JNLP - Informasi Lebih Lanjut

File JNLP disimpan sebagai file **[XML](/id/web/xml/)** yang disimpan dalam format teks yang dapat dibaca manusia. File XML memiliki informasi yang digunakan untuk meluncurkan dan menjalankan aplikasi Java melalui jaringan. JWS memungkinkan Anda meluncurkan aplikasi dengan mengklik tautan halaman web. Aplikasi diunduh jika belum diunduh di komputer pengguna.

Oracle menghentikan JWS dengan merilis Java Platform Standard Edition (JSE) 9. Dengan ini, file JNLP tidak lagi didukung.

### Bagaimana cara membuka file JNLP?

Aplikasi yang bisa **membuka file JNLP** antara lain **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart**, dan * *GitHub Atom**.

### Contoh File JNLP

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
**Penggunaan**

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
## Bagaimana cara menjalankan file JNLP?

Dengan dihentikannya JWS, aplikasi yang dikembangkan berdasarkan teknologi JWS tidak dapat dijalankan dengan Java versi terbaru. Namun, program berbasis JNLP ini dapat dijalankan menggunakan OpenWebStart yang merupakan implementasi ulang sumber terbuka dari teknologi Java Web Start. Itu diinstal secara paralel dengan versi terbaru Java dan menyediakan fitur Java Web Start yang paling umum digunakan dan standar JNLP.

## Referensi ##

* [Apa itu Java Web Start dan Bagaimana peluncurannya?](https://www.java.com/en/download/help/java_webstart.html)
* [Jalankan JNLP dengan Java Versi Terbaru](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

