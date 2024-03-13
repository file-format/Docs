---
date: 2019-10-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS fayl formasıat
linktitle: CSS
description: LCSS faylı yarada və aça bilən CSS fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## CSS faylı nədir? ##

CSS (Cascading Style Sheets) HTML elementlərinin ekranda, kağızda və s. necə göstərildiyini təsvir edən fayllardır. HTML ilə siz ya daxili üslublara malik ola bilərsiniz, ya da üslubları xarici üslub cədvəlində müəyyən etmək olar. Üslubları daxil etmək üçün \ <style>\</style> etiketlərdən istifadə olunur. Xarici üslub cədvəlləri .css uzantılı fayllarda saxlanılır. Xarici CSS ilə siz həmin səhifələrin üslubunu yeniləmək üçün onu bir neçə HTML səhifəsinə daxil edə bilərsiniz. Hətta tək bir CSS faylı tam veb saytı tərtib etmək üçün istifadə edilə bilər.

## Qısa tarix ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. Bu, 1997-ci ilin noyabrında CSS2-nin yaradılması ilə nəticələndi və 12 may 1998-ci ildə W3C tövsiyəsi kimi nəşr olundu. Bu versiya printerlər, endirilə bilən şriftlər, cədvəllər və elementlərin yerləşdirilməsi kimi media-xüsusi cihazlara dəstək əlavə etdi. 1999-cu ilin iyun ayında CSS3 W3C-nin tövsiyəsi oldu. Bu, sənədləri hər modulun CSS2-də müəyyən edilmiş genişləndirmə xüsusiyyətlərinə malik olduğu modullara böldü.

## CSS fayllarından necə istifadə etmək olar ##

CSS faylından istifadə etmək üçün onu HTML sənədinin baş hissəsinə daxil etməlisiniz. Aşağıda göstərildiyi kimi faylı daxil etmək üçün keçid etiketindən istifadə edirsiniz.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

link teqinin *href* atributunda CSS faylına gedən yol var. Bunu etməklə, daxil edilmiş CSS faylında olan müvafiq üslublar HTML sənədinə tətbiq edilir.

## CSS Sintaksis ##

CSS qaydası iki komponentdən, seçici və bəyannamədən ibarətdir. Selektor HTML sənədindəki elementə işarə edir. Bu, ya element teqi, sinif adı, id adı, iyerarxiyanı göstərən çoxsaylı teqlər və s. ola bilər. Bəyannamə mülkiyyət və dəyərdən ibarət üslub tərifini ehtiva edir. Xüsusiyyət dəyişdirmək istədiyiniz elementin xüsusiyyətini müəyyənləşdirir və dəyər onun yeni dəyərini təyin edir. Hər bir CSS qaydasının bir neçə bəyannaməsi ola bilər. Aşağıdakı bir CSS qaydasının nümunəsidir.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Yuxarıdakı misalda HTML sənədindəki bütün h1 teqlərini seçən seçici olaraq **h1** var. Qaydada biri şrift çəkisi, digəri isə rəng üçün iki bəyannamə var. *font-weight* və *color* xassələri, *700* və *forestgreen* isə müvafiq olaraq onların dəyərləridir.

## CSS İstifadə Nümunəsi ##

Aşağıda nümunə HTML sənədi və onun üslubu üçün istifadə olunan üslub cədvəli göstərilir. Müqayisə şəkli də üslublu və sadə HTML sənədlərini müqayisə etmək üçün əlavə edilir

### HTML Sənədi ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS üslub cədvəli ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Çıxış Müqayisəsi ###

Şəklin sol tərəfində tətbiq edilmiş üslublar olmadan HTML sənədi, sağ tərəfində isə tətbiq olunan üslublarla HTML sənədi göstərilir.

{{< figure src="../CssExample.jpg" alt="Nümunə şəkil" >}}

## İstinadlar ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

