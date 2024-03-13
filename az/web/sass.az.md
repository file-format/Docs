---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass fayl formasıat
linktitle: Sass
description: LSass faylı yarada və aça bilən Sass fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## SASS faylı nədir? ##

Sass (sintaktik cəhətdən zəhmli üslub vərəqləri) preprosessor skript dilidir. O, [CSS](/web/css/) daxilində tərtib edilib və .sass uzantısı ilə saxlanılır. Sass iki sintaksisdən ibarətdir, orijinal .sass genişlənməsini istifadə edən girintilərə əsaslanır və .scss genişləndirilməsini istifadə edən CSS kimi blok formatlı daha yeni SCSS.

## Niyə Sass ## istifadə edin

Sass üslubları saxlamaqda həqiqətən faydalıdır, çünki o, dəyişənlər, yuvalar, mikslər, idxallar və üslublarla işləməyi əyləncəli edən seçici miras kimi bir çox xüsusiyyətləri təqdim edir.

## SASS fayllarından necə istifadə etmək olar ##

SASS faylları birbaşa [HTML](/web/html/) sənədinə daxil edilmir, əksinə HTML fayllarına daxil edilmiş CSS fayllarına çevrilir. Siz [Official Sass Site](https://sass-lang.com/install)-də verilmiş təlimatlara əməl etməklə sisteminizin Sass-ı dayandıra bilərsiniz.

Sass ya artıq saxlanmış SASS faylını çevirməklə, ya da dəyişiklikləri izləməklə və fayl saxlandıqca çevirməklə CSS-ə çevrilə bilər. Hər ikisi üçün əmrlər aşağıda verilmişdir.

### Bir dəfə çevirin ###

Komandanın birinci parametri mənbə SASS faylıdır, ikinci parametr isə çıxış CSS faylıdır.

```cmd
sass main.sass main.css
```

### Dəyişikliklərə baxın ###

Yuxarıdakı əmr əmri işlək vəziyyətdə saxlayan əlavə *watch* bayrağı ilə işlədilə bilər və Sass faylı saxlanılan kimi çıxış CSS yaradılır.

```cmd
sass --watch main.sass main.css
```

## Sass Sintaksis ##

Sass dəyişənləri, yuva qurmağı, miksinləri, idxalı, seçici irsiyyətini və s. dəstəkləyir. Aşağıda bu xüsusiyyətlərin nümunələri verilmişdir.

### Dəyişənlər ###

Dəyişənlər bir düymə üçün əsas rəng və ya doldurma kimi təkrar istifadə edilə bilən məlumatları təyin etmək üçün istifadə edilə bilər. Bu, gələcəkdə həmin məlumatı dəyişmək lazım gələrsə, onu sadəcə bir yerdə dəyişdirsəniz və o, hər yerdə yenilənirsə faydalı ola bilər.

**Sass**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

CSS seçiciləri HTML iyerarxiyasına bənzər şəkildə yuvalana bilər. Aşağıdakı nümunədə span h1 blokunun içərisinə yerləşdirilib.

**Sass**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

Qarışıqlar bir çox yerdə istifadə olunan oxşar xüsusiyyətləri bir araya toplamaq üçün istifadə olunur. Mixinlər də parametrləri dəstəkləyir.

**Sass**

**Mixin elan edilməsi**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Mixin istifadəsi**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Genişləndirmə/Vərəslik bir seçicinin xassələrinin digər seçici ilə paylaşılması lazım olduğu hallarda faydalı ola bilər. Aşağıdakı misalda *.error-notice* seçicisi *.error-text* seçicisinin bütün xassələrini götürür və haşiyə və doldurma xüsusiyyətlərini əlavə edir.

**Sass**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

Stillərinizi funksionallıq və ya izlədiyiniz hər hansı digər struktur əsasında müxtəlif fayllara strukturlaşdırsanız, idxal faydalı ola bilər. Siz bütün bu faylları sonradan CSS-ə çevrilən əsas SASS faylına idxal edə bilərsiniz. İdxal edərkən, idxal təlimatında fayl uzantısını göstərməyə ehtiyac yoxdur. Sass bütün SASS fayllarını birbaşa tərtib edir. İdxal fayllarının birbaşa tərtib edilməməsi üçün adının əvvəlinə alt xətt (_) əlavə etməklə onları qismən edə bilərsiniz. Qismən adi Sass fayllarına bənzər idxal olunur.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Çıxış CSS-də bütün idxal edilmiş faylların üslubları olacaq.

## İstinadlar ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

