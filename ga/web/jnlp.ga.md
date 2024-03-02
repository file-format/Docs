---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JFormáid Chomhaid NLP - Cad is comhad JNP anne?
linktitle: JNLP
description: Ltuilleamh faoi fhormáid comhaid JNLP agus APIs ar féidir leo comhad JNLP a chruthú agus a oscailts.
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Cad is comhad JNLP ann?

Is éard atá i gcomhad JNLP ná comhad Java Web Start (JWS) ina bhfuil faisnéis XML chun clár Java a sheoladh thar an líonra. Déantar é a shábháil i bhformáid Prótacal Seoladh Líonra Java (JNLP). Úsáideann an teicneolaíocht Java Web Start (JWS) é, teicneolaíocht imlonnaithe feidhmchlár chun feidhmchlár a íoslódáil agus a rith. I gcomhad JNLP tá ciansheoladh an fhreastalaí óna ndéantar an clár a íoslódáil agus a sheoladh ar an meaisín áitiúil.

## Formáid Chomhaid JNLP - Tuilleadh Eolais

Déantar comhaid JNLP a shábháil mar **[XML](/web/xml/)** comhaid a stóráiltear i bhformáid téacs inléite ag an duine. Tá an fhaisnéis sa chomhad XML a úsáidtear chun feidhmchlár Java a sheoladh agus a rith thar an líonra. Ligeann an JWS duit feidhmchláir a sheoladh trí chliceáil ar an nasc leathanach gréasáin. Déantar an feidhmchlár a íoslódáil i gcás nach bhfuil sé íoslódála cheana féin ar an ríomhaire úsáideora.

Oracle deprecated JWS with the release of Java Platform Standard Edition (JSE) 9. Leis seo, ní thacaítear níos mó le comhaid JNLP.

### Conas comhaid JNLP a oscailt?

I measc na n-iarratas ar féidir **comhaid JNLP a oscailt** tá **Cód Microsoft Visual Studio**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart**, agus * * Adamh GitHub**.

### Sampla Comhad JNLP

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
**Úsáid**

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
## Conas Comhaid JNLP a Rith?

Le dímheas JWS, ní féidir feidhmchláir a forbraíodh bunaithe ar theicneolaíocht JWS a rith leis an leagan is déanaí de Java. Is féidir na cláir seo atá bunaithe ar JNLP, áfach, a rith ag baint úsáide as OpenWebStart atá mar athchur foinse oscailte ar theicneolaíocht Java Web Start. Suiteálann sé go comhthreomhar leis an leagan is déanaí de Java agus soláthraíonn sé na gnéithe is coitianta a úsáidtear de Java Web Start agus an caighdeán JNLP.

## Tagairtí ##

* [Cad é Java Web Start agus Conas a sheoltar é?](https://www.java.com/en/download/help/java_webstart.html)

* [Rith JNLP leis an Leagan is déanaí de Java](https://openwebstart.com/)

* [Tosú Gréasáin Java - Vicipéid](https://ga.wikipedia.org/wiki/Java_Web_Start)


