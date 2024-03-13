---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS Fayl Formasıat
linktitle: JS
description: LJS faylı yarada və aça bilən JS fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## JS faylı nədir? ##

JS (JavaScript) veb səhifələrdə icra üçün JavaScript kodu olan fayllardır. JavaScript faylları .js uzantısı ilə saxlanılır. [HTML](/web/html/) sənədinin içərisinə, siz \ istifadə edərək JavaScript kodunu yerləşdirə bilərsiniz. <script>\</script> etiketlər və ya JS faylı daxil edin. [CSS](/web/css/) fayllarına bənzər olaraq, JS faylları kodun təkrar istifadəsi üçün çoxlu HTML sənədlərinə daxil edilə bilər. JavaScript HTML DOM ilə manipulyasiya etmək üçün istifadə edilə bilər.

## Qısa tarix ##

JavaScript ilk dəfə 1995-ci ilin sentyabrında Netscape tərəfindən LiveScript adı ilə Navigator Brauzerinin bir hissəsi kimi göndərilib. Üç ay sonra JavaScript adını dəyişdirdi. 1996-cı ildə Microsoft, JScript yaratmaq üçün Navigatorun tərcüməçisini tərs dizayn etdi. JScript Internet Explorer ilə buraxıldı və JavaScript-dən çox fərqli idi.

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. ECMAScript 2 1998-ci ildə, ECMAScript 3 1999-cu ildə buraxıldı və ECMAScript 4 üzərində iş 2000-ci ildə başladı, lakin heç vaxt nəticə vermədi.

2005-ci ildə Jesse James Garrett *Ajax* terminini işlətdiyi ağ kağız nəşr etdi. Bu, arxa planda məlumatları yükləyən və səhifənin tam yenidən yüklənməsinin qarşısını alan veb proqramlar yaratmaq üçün JavaScript-dən əsas kimi istifadə etdi. Bu, JQuery, Prototype, Dojo və s. kimi kitabxanaların yaradılması ilə nəticələndi.

Google released the Chrome browser with the V8 JavaScript engine in 2008. 2009-cu ilin əvvəlində bütün müvafiq işləri birləşdirmək və JavaScript-i irəli aparmaq üçün razılaşma əldə edildi. Bu, 2009-cu ilin dekabrında ECMAScript 5 Standardının buraxılması ilə nəticələndi.

## JS fayllarından necə istifadə etmək olar ##

JS faylından istifadə etmək üçün onu HTML sənədinə daxil etməlisiniz. Aşağıda göstərildiyi kimi faylı daxil etmək üçün keçid etiketindən istifadə edirsiniz.

```html
<script src="site.js"></script>
```

*script* teqinin *src* atributu JS faylına gedən yolu ehtiva edir. Bunu etməklə, JS funksionallığı HTML sənədinə əlavə olunur.

## JS Sintaksis ##

JavaScript fayllarında dəyişənlər, operatorlar, funksiyalar, şərtlər, dövrələr, massivlər, obyektlər və s. ola bilər. Aşağıda JavaScript sintaksisinin qısa icmalı verilmişdir.

- Hər bir əmr nöqtəli vergül(;) ilə bitir.
- Dəyişənləri elan etmək üçün *var* açar sözündən istifadə edin.
- Supports arithmetic operators ( + - * / ) dəyərləri hesablamaq üçün.
- Tək sətir şərhlər // ilə əlavə edilir və çoxsətirli şərhlər /* və */ ilə əhatə olunur.
- Bütün identifikatorlar hərflərə həssasdır, yəni *modelNo* və *modelno* iki fərqli dəyişəndir.
- Funksiyalar *function* açar sözündən istifadə etməklə müəyyən edilir.
- Massivlər kvadrat mötərizədə [] istifadə edilməklə müəyyən edilə bilər.
- JS ==, !=, >=, !== və s. kimi müqayisə operatorlarını dəstəkləyir.
- Sinifləri *class* açar sözündən istifadə etməklə müəyyən etmək olar.

## JS İstifadə Nümunəsi ##

Aşağıda sadə istifadə nümunəsi JavaScript faylı göstərilir.

### HTML Sənədi ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### JS Kodu ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## İstinadlar ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

