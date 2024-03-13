---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS Fayl Format - Sass Cascading Style Sheet
linktitle: SCSS
description: LSCSS fayl formatı və SCSS faylını yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## SCSS faylı nədir? ##

SCSS, girintilər əvəzinə mötərizələrdən istifadə edən Sass-ın (Sintaktik Awesome Stylesheet) ikinci sintaksisidir. SCSS elə tərtib edilib ki, etibarlı CSS3 faylı da etibarlı SCSS faylı olsun. SCSS faylları .scss uzantısı ilə saxlanılır.

## Niyə SCSS ## istifadə edin

Veb saytların dizaynları mürəkkəbləşdikcə böyük [CSS](/web/css/) faylları yaranır. Belə faylları saxlamaq daha çətindir. Bu, SCSS-nin daxil olduğu yerdir. SCSS CSS inkişafında dəyişənləri, yuvaları, miksinləri, idxalı və seçici irsiyyətini təqdim edir. Bu əlavələr dizaynla işləməyi daha əyləncəli edir.

## SCSS fayllarını necə istifadə etmək olar ##

SCSS faylları birbaşa CSS kimi [HTML](/web/html/) sənədinə daxil edilmir. Bunun əvəzinə, SCSS faylları HTML fayllarına daxil olan CSS fayllarına çevrilir. Sisteminizdə SCSS quraşdırmaq üçün [Official Sass Site](https://sass-lang.com/install)-də verilmiş təlimatlara əməl edin.
SCSS-ni CSS-ə çevirmək üçün ya artıq saxlanmış SCSS faylını çevirə və ya dəyişiklikləri izləyə və fayl saxlandıqca çevirə bilərsiniz. Hər ikisi üçün əmrlər aşağıda verilmişdir.

### Bir dəfə çevirin ###

Birinci parametr mənbə SCSS faylıdır, ikinci parametr isə çıxış CSS faylıdır.

```cmd
sass main.scss main.css
```

### Dəyişikliklərə baxın ###

Komandanın əmri işlək vəziyyətdə saxlayan əlavə *watch** bayrağı var və SCSS faylı saxlanılan kimi çıxış CSS-i yaradılır.

```cmd
sass --watch main.scss main.css
```

## SCSS Sintaksis ##

SCSS dəyişənləri, yuva qurmağı, miksinləri, idxalı, seçici varisliyi və s. dəstəkləyir. Aşağıda bu xüsusiyyətlərin nümunələri verilmişdir.

### Dəyişənlər ###

Dəyişənlərin istifadəsi ilə siz saxlama düyməsi üçün əsas rəng və ya fon rəngi kimi təkrar istifadə edilə bilən məlumatları təyin edə bilərsiniz. Bu, həmin məlumatı dəyişmək lazım olduqda faydalıdır, siz onu sadəcə bir yerdə dəyişdirirsiniz və o, istifadə olunduğu yerdə yenilənir.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**Yaradılmış CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Yuvalama ###

Siz HTML iyerarxiyasına bənzər CSS seçicilərini yerləşdirə bilərsiniz. Aşağıdakı misalda span h1 blokunun içərisinə yerləşdirilib.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**Yaradılmış CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Qarışıqlar ###

Qarışıqlar bir çox yerdə birlikdə istifadə olunan oxşar xüsusiyyətləri bir araya qruplaşdırmaq üçün istifadə edilə bilər. Siz həmçinin miksinlərə parametrləri ötürə bilərsiniz.

**SCSS**

**Mixin elan edilməsi**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Mixin istifadəsi**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**Yaradılmış CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Uzatmaq ###

Genişləndirmə/Vərəslik bir selektorun xassələrinin digər seçici ilə paylaşılması lazım olduğu hallarda faydalıdır. Aşağıdakı misalda *.error-notice* seçicisi *.error-text* seçicisinin bütün xassələrini götürür və haşiyə və doldurma xüsusiyyətlərini əlavə edir.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**Yaradılmış CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### İdxal ###

İdxal narahatlıqların ayrılması üçün faydalı ola bilər. Üslubları elə bölmək olar ki, başlıq üslubları ayrıca faylda, altbilgi üslubları ayrı bir faylda olsun, üslublarda istifadə olunan bütün rəng dəyişənləri ayrı bir faylda olsun və s. Bu texnikadan istifadə edərək, üslublar mütəşəkkil qalır. Siz sadəcə olaraq aşağıdakı nümunədə göstərildiyi kimi əsas SCSS faylınızdakı faylları idxal edirsiniz. İdxal təlimatında fayl uzantısını göstərməyə ehtiyac yoxdur. Sass bütün SCSS fayllarını birbaşa tərtib edir. İdxal fayllarının birbaşa tərtib edilməməsi üçün adlarından əvvəl alt xətt (_) əlavə edərək onları qismən edə bilərsiniz. Siz adi SCSS fayllarına bənzər hissələri alt xətt olmadan idxal edə bilərsiniz.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Çıxış CSS-də bütün idxal edilmiş faylların üslubları olacaq.

## İstinadlar ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

