---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM Fayl Format - PYM Macro Preprocessor File
linktitle: PYM
description: LPYM faylı yarada və aça bilən PYM fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## PYM faylı nədir?

PYM faylı Python proqramlaşdırma dilinə əsaslanan makro preprosessor faylıdır. O, VRVis Research tərəfindən hazırlanmış və makro qısa yollarını saxlamışdır. PYM faylı Python tərcüməçisinin ilkin emal mərhələsi tərəfindən şərh edildikdə, bu qısayollar onların tam mətnini əvəz edən kimi genişləndirilir. Bundan əlavə, makro preprosessor tərəfindən yerinə yetirilə bilən üçüncü, isteğe bağlı əməliyyat fayl daxil edilməsidir. PYM faylları Linux-da Notepad, Notepad++, Apple TextEdit və VI mətn redaktorlarında açıla bilər.

## PYM fayl formatı

PYM faylları diskdə düz mətn faylları kimi saxlanılır. PYM faylı `#include` direktivindən istifadə edərək digər faylları da daxil edə bilər.

### PYM Sintaksisi

PYM ifadələri aşağıda göstərildiyi kimi #begin python və #end python markerləri arasında yer alır.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM Makro Genişlənməsi

PYM makro genişlənməsi iki ardıcıllıqla, yəni <[ və ]> ilə təmsil olunur. Bunlar xüsusi html teqləridir və xəttin istənilən yerində görünə bilər. Kiçik bir PYM nümunəsi aşağıdakı kimidir.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

Bunu PYM vasitəsilə həyata keçirməyin nəticəsi aşağıdakı kimidir:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## İstinadlar ##

 * [PYM - Python-a əsaslanan makro preprosessor](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [PYM Tərcüməçiləri](https://github.com/interpreters/pym)

