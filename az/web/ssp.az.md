---
date: 2021-07-05
keywords: ssp, .ssp, ssp file format, how to open ssp files, Scala Server Page
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Server Səhifələri Fayl Formasıat
linktitle: SSP
description: LSSP fayl formatının nə olduğu və SSP faylını yarada və aça bilən API-lər haqqında məlumat əldə edins.
menu:
  docs:
    identifier: "web-ss-azp"
    parent: "web"
lastmod: 2021-09-30
---

## SSP faylı nədir?

.ssp uzantısı olan fayl yalnız adi HTML əvəzinə ifadələr üçün Scala kodu ilə yaradılmış veb səhifədir. HTML və Scala birləşməsindən istifadə edərək server tərəfi skripti kimi çıxış edir. Bu fayllar serverdə yerləşir və istifadəçilərə təqdim olunacaq statik veb səhifələr yaratmaq üçün istifadə olunur. Scala özü sintaksisi Velocity, JSP və ya Erb ilə işləyən istifadəçilərə tanış olan ümumi təyinatlı proqramlaşdırma dilidir. SSP faylları mətn və işarələmə yaratmaq üçün Scala əsaslı şablon mühərriki olan [Scalate](https://scalate.github.io/scalate/) istifadə edərək təhlil və qiymətləndirilə bilər.

## SSP Fayl Format - Ətraflı Məlumat

SSP faylları düz mətn faylında saxlanılır və Scalate istifadə edərək qiymətləndirilə bilər. Ssp şablonu daha çox HTML sənədi olan düz mətndən ibarətdir. O, daxil edilmiş Ssp teqlərinə malikdir və bu, göstərmə mühərriklərinin sənədin müxtəlif hissələrini dinamik şəkildə göstərməsinə səbəb olur. Teqlər <% ... %> və ${ ... } ardıcıllığı ilə başlayır və bitir və bunlardan kənar hər şey hərfi mətn kimi qəbul edilir.

### SSP Nümunəsi

Aşağıdakı nümunə SSP kodunu və göstərmə mühərriki tərəfindən göstərildikdə onun çıxışını göstərir.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Çıxış aşağıdakı kimidir.
```
<p>
  hi there reader!
  yo 7
</p>
```

## İstinadlar

- [SSP Reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)

