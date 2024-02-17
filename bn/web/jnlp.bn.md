---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP ফাইল ফরম্যাট - একটি JNP ফাইল কিe?
linktitle: JNLP
description: LJNLP ফাইল ফরম্যাট এবং API সম্পর্কে আয় করুন যা JNLP ফাইল তৈরি এবং খুলতে পারেs.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## একটি JNLP ফাইল কি?

একটি JNLP ফাইল হল একটি জাভা ওয়েব স্টার্ট (JWS) ফাইল যাতে নেটওয়ার্কে একটি জাভা প্রোগ্রাম চালু করার জন্য XML তথ্য থাকে। এটি জাভা নেটওয়ার্ক লঞ্চিং প্রোটোকল (JNLP) ফরম্যাটে সংরক্ষিত হয়। এটি জাভা ওয়েব স্টার্ট (JWS) প্রযুক্তি দ্বারা ব্যবহৃত হয় যা একটি অ্যাপ্লিকেশন ডাউনলোড এবং চালানোর জন্য একটি অ্যাপ্লিকেশন স্থাপনার প্রযুক্তি। একটি JNLP ফাইলে সার্ভারের দূরবর্তী ঠিকানা থাকে যেখান থেকে প্রোগ্রামটি ডাউনলোড করা হয় এবং স্থানীয় মেশিনে চালু করা হয়।

## JNLP ফাইল ফরম্যাট - আরও তথ্য

JNLP ফাইলগুলি **[XML](/web/xml/)** ফাইল হিসাবে সংরক্ষিত হয় যা মানুষের পাঠযোগ্য পাঠ্য বিন্যাসে সংরক্ষণ করা হয়। XML ফাইলটিতে এমন তথ্য রয়েছে যা নেটওয়ার্কের মাধ্যমে একটি জাভা অ্যাপ্লিকেশন চালু এবং কার্যকর করতে ব্যবহৃত হয়। JWS আপনাকে ওয়েব পেজ লিঙ্কে ক্লিক করে অ্যাপ্লিকেশন চালু করতে দেয়। অ্যাপ্লিকেশনটি ডাউনলোড করা হয় যদি এটি ইতিমধ্যে ব্যবহারকারীর কম্পিউটারে ডাউনলোড না হয়।

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. এর সাথে, JNLP ফাইলগুলি আর সমর্থিত নয়।

### কিভাবে JNLP ফাইল খুলবেন?

যেসব অ্যাপ্লিকেশন **JNLP ফাইল খুলতে পারে** তার মধ্যে রয়েছে **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart**, এবং * *গিটহাব এটম**।

### JNLP ফাইলের উদাহরণ

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
**ব্যবহার**

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
## কিভাবে JNLP ফাইল চালাবেন?

JWS এর অবচয়নের সাথে, JWS প্রযুক্তির উপর ভিত্তি করে বিকশিত অ্যাপ্লিকেশনগুলি জাভার সর্বশেষ সংস্করণের সাথে চালানো যাবে না। এই JNLP ভিত্তিক প্রোগ্রামগুলি অবশ্য OpenWebStart ব্যবহার করে চালানো যেতে পারে যা জাভা ওয়েব স্টার্ট প্রযুক্তির একটি ওপেন সোর্স পুনঃপ্রয়োগ। এটি জাভার সর্বশেষ সংস্করণের সমান্তরালে ইনস্টল করে এবং জাভা ওয়েব স্টার্ট এবং JNLP স্ট্যান্ডার্ডের সর্বাধিক ব্যবহৃত বৈশিষ্ট্যগুলি প্রদান করে।

## তথ্যসূত্র ##

* [জাভা ওয়েব স্টার্ট কী এবং কীভাবে এটি চালু হয়?](https://www.java.com/en/download/help/java_webstart.html)

* [জাভার সর্বশেষ সংস্করণ সহ JNLP চালান](https://openwebstart.com/)

* [জাভা ওয়েব স্টার্ট - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Java_Web_Start)


