---
date: 2022-07-30
مؤلف:
  display_name: Kashif Iqbal
draft: false
toc: true
title: تنسيق ملف JNLP - ما هو ملف JNP؟
linktitle: JNLP
description: "تعرف على تنسيق ملف JNLP وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات JNLP وفتحها."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## ما هو ملف JNLP؟

ملف JNLP هو ملف Java Web Start (JWS) يحتوي على معلومات XML لتشغيل برنامج Java عبر الشبكة. يتم حفظه بتنسيق Java Network Launching Protocol (JNLP). يتم استخدامه بواسطة تقنية Java Web Start (JWS) وهي تقنية نشر تطبيق لتنزيل تطبيق وتشغيله. يحتوي ملف JNLP على العنوان البعيد للخادم الذي يتم من خلاله تنزيل البرنامج وتشغيله على الجهاز المحلي.

## تنسيق ملف JNLP - مزيد من المعلومات

يتم حفظ ملفات JNLP كملفات ** [XML](/ar/ web / xml /) ** مخزنة بتنسيق نصي يمكن للبشر قراءته. يحتوي ملف XML على المعلومات المستخدمة لبدء تشغيل تطبيق Java وتنفيذه عبر الشبكة. يتيح لك JWS تشغيل التطبيقات بالنقر فوق ارتباط صفحة الويب. يتم تنزيل التطبيق في حالة عدم تنزيله بالفعل على كمبيوتر المستخدم.

تم إهمال Oracle JWS مع إصدار Java Platform Standard Edition (JSE) 9. مع هذا ، لم تعد ملفات JNLP مدعومة.

### كيفية فتح ملفات JNLP؟

تتضمن التطبيقات التي يمكنها ** فتح ملفات JNLP ** ** Microsoft Visual Studio Code ** و ** Notepad ** و ** Notepad ++ ** و ** Oracle Java Web Start ** و ** Karakun OpenWebStart ** و * * جيثب أتوم **.

مثال على ملف JNLP

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
** الاستخدام **

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
## كيفية تشغيل ملفات JNLP؟

مع إهمال JWS ، لا يمكن تشغيل التطبيقات التي تم تطويرها بناءً على تقنية JWS بأحدث إصدار من Java. ومع ذلك ، يمكن تشغيل هذه البرامج المستندة إلى JNLP باستخدام OpenWebStart وهو إعادة تطبيق مفتوحة المصدر لتقنية Java Web Start. يتم تثبيته بالتوازي مع أحدث إصدار من Java ويوفر الميزات الأكثر استخدامًا لـ Java Web Start ومعيار JNLP.

## مراجع ##

* [ما هو Java Web Start وكيف يتم إطلاقه؟](https://www.java.com/en/download/help/java_webstart.html)
* [تشغيل JNLP بأحدث إصدار من Java](https://openwebstart.com/)
* [جافا ويب ستارت - ويكيبيديا](https://en.wikipedia.org/wiki/Java_Web_Start)

