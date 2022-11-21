---
date: 2019-10-11
keywords: scss, .scss, scss dosya formatı, scss dosyalarının nasıl açılacağı, sözdizimsel olarak harika stil sayfası, css önişlemcisi, sass
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS Dosya Formatı - Sass Basamaklı Stil Sayfası
linktitle: SCSS
description: "SCSS dosya formatı ve SCSS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## SCSS dosyası nedir? ##

SCSS, girintiler yerine parantez kullanan Sass'ın (Sözdizimsel Olarak Harika Stil Sayfası) ikinci sözdizimidir. SCSS, geçerli bir CSS3 dosyası aynı zamanda geçerli bir SCSS dosyası olacak şekilde tasarlanmıştır. SCSS dosyaları .scss uzantısıyla saklanır.

## Neden SCSS ## kullanmalısınız?

Web sitelerinin tasarımları karmaşık hale geldikçe, büyük [CSS](/tr/web/css/) dosyaları ortaya çıkıyor. Bu tür dosyaların bakımı daha zordur. SCSS'nin devreye girdiği yer burasıdır. SCSS, CSS geliştirmede değişkenler, iç içe yerleştirme, karışımlar, içe aktarmalar ve seçici kalıtımı sunar. Bu eklemeler, tasarımla çalışmayı çok daha eğlenceli hale getiriyor.

## SCSS dosyaları nasıl kullanılır ##

SCSS dosyaları, CSS gibi doğrudan [HTML](/tr/web/html/) belgesine dahil edilmez. Bunun yerine, SCSS dosyaları HTML dosyalarında bulunan CSS dosyalarına dönüştürülür. SCSS'yi sisteminize kurmak için [Resmi Sass Sitesi](https://sass-lang.com/install) üzerinde verilen talimatları izleyin.
SCSS'yi CSS'ye dönüştürmek için önceden kaydedilmiş bir SCSS dosyasını dönüştürebilir veya değişiklikleri izleyerek dosya kaydedilirken dönüştürebilirsiniz. Her ikisi için de komutlar aşağıda verilmiştir.

### Bir Kez Dönüştürün ###

İlk parametre kaynak SCSS dosyasıdır ve ikinci parametre çıktı CSS dosyasıdır.

```cmd
sass main.scss main.css
```

### Değişiklikleri İzleyin ###

Komutun, komutu çalışır durumda tutan ek bir *izle** bayrağı vardır ve SCSS dosyası kaydedilir kaydedilmez CSS çıktısı oluşturulur.

```cmd
sass --watch main.scss main.css
```

## SCSS Sözdizimi ##

SCSS değişkenleri, iç içe yerleştirmeyi, karışımları, içe aktarmaları, seçici kalıtımı vb. destekler. Aşağıda bu özelliklerin örnekleri verilmiştir.

### Değişkenler ###

Değişkenleri kullanarak, kaydet düğmesi için birincil renk veya arka plan rengi gibi yeniden kullanılabilir bilgileri ayarlayabilirsiniz. Bu bilgiyi değiştirmeniz gerektiğinde kullanışlıdır, sadece bir yerde değiştirirsiniz ve kullanıldığı yerde güncellenir.

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

**Oluşturulan CSS**

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

### Yerleştirme ###

CSS seçicilerini HTML hiyerarşisine benzer şekilde iç içe yerleştirebilirsiniz. Aşağıda verilen örnekte, açıklık h1 bloğunun içine yerleştirilmiştir.

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

**Oluşturulan CSS**

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

### Karışımlar ###

Karışımlar, birden çok yerde birlikte kullanılan benzer özellikleri gruplandırmak için kullanılabilir. Parametreleri karışımlara da iletebilirsiniz.

**SCSS**

**Bir karışımın bildirilmesi**

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

**Bir karışım kullanarak**

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

**Oluşturulan CSS**

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

### Uzatmak ###

Extend/Inheritance, bir seçicinin özelliklerinin başka bir seçiciyle paylaşılmasının gerektiği durumlarda kullanışlıdır. Aşağıdaki örnekte *.error-notice* seçici, *.error-text* seçicinin tüm özelliklerini alır ve kenarlık ve dolgu özellikleri ekler.

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

**Oluşturulan CSS**

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

### İçe aktarmak ###

İthalat endişelerin ayrılmasında faydalı olabilir. Stilleri, başlık stilleri ayrı bir dosyada, altbilgi stilleri ayrı bir dosyada, stillerde kullanılan tüm renk değişkenleri ayrı bir dosyada vb. olacak şekilde bölebilirsiniz. Bu tekniği kullanarak, stiller düzenli kalır. Aşağıdaki örnekte gösterildiği gibi dosyaları ana SCSS dosyanıza aktarmanız yeterlidir. İçe aktarma talimatında dosya uzantısını belirtmeniz gerekmez. Sass, tüm SCSS dosyalarını doğrudan derler. İçe aktarma dosyalarının doğrudan derlenmesini önlemek için, adlarının önüne alt çizgi(_) ekleyerek dosyaları kısmi yapabilirsiniz. Alt çizgi olmadan normal SCSS dosyalarına benzer kısmi dosyaları içe aktarabilirsiniz.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Çıktı CSS'si, içe aktarılan tüm dosyalardan stillere sahip olacaktır.

## Referanslar ##

- [SCSS - Vikipedi](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

