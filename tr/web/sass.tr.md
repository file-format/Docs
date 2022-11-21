---
date: 2019-10-11
keywords: sass, .sass, sass dosya formatı, sass dosyalarının nasıl açılacağı, sözdizimsel olarak harika stil sayfası, css önişlemcisi, sass
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dosya Biçimi
linktitle: Sass
description: "Sass dosya formatı ve Sass dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## SASS dosyası nedir? ##

Sass (sözdizimsel olarak harika stil sayfaları), bir önişlemci betik dilidir. [CSS](/tr/web/css/) biçiminde derlenir ve .sass uzantısıyla depolanır. Sass iki sözdiziminden oluşur; orijinali .sass uzantısını kullanan girintilere dayalıdır ve .scss uzantısını kullanan CSS gibi blok biçimlendirmeli daha yeni SCSS'dir.

## Sass ## neden kullanılır?

Sass, stillerle çalışmayı eğlenceli hale getiren değişkenleri tanıtma, iç içe yerleştirme, karışımlar, içe aktarma ve seçici kalıtım gibi birçok özellik sağladığından stilleri korumada gerçekten yararlıdır.

## SASS dosyaları nasıl kullanılır ##

SASS dosyaları doğrudan [HTML](/tr/web/html/) belgesine dahil edilmez, bunun yerine HTML dosyalarına dahil edilen CSS dosyalarına dönüştürülür. [Resmi Sass Sitesi](https://sass-lang.com/install) üzerinde verilen talimatları takip ederek sisteminize Sass kurabilirsiniz.

Sass, önceden kaydedilmiş bir SASS dosyasını dönüştürerek veya değişiklikleri izleyerek ve dosya kaydedilirken dönüştürerek CSS'ye dönüştürülebilir. Her ikisi için de komutlar aşağıda verilmiştir.

### Bir Kez Dönüştürün ###

Komutun ilk parametresi kaynak SASS dosyası, ikinci parametresi ise çıktı CSS dosyasıdır.

```cmd
sass main.sass main.css
```

### Değişiklikleri İzleyin ###

Yukarıdaki komut, komutu çalışır durumda tutan ek bir *izle* bayrağıyla çalıştırılabilir ve Sass dosyası kaydedilir kaydedilmez CSS çıktısı oluşturulur.

```cmd
sass --watch main.sass main.css
```

## Sas Sözdizimi ##

Sass değişkenleri, iç içe yerleştirmeyi, karışımları, içe aktarmaları, seçici kalıtımı vb. destekler. Aşağıda bu özelliklerin örnekleri verilmiştir.

### Değişkenler ###

Değişkenler, bir düğme için birincil renk veya dolgu gibi yeniden kullanılabilir bilgileri ayarlamak için kullanılabilir. Bu, gelecekte bu bilgileri değiştirmeniz gerektiğinde yararlı olabilir, yalnızca bir yerde değiştirirsiniz ve her yerde güncellenir.

**küstah**

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

CSS seçicileri, HTML hiyerarşisine benzer şekilde yuvalanabilir. Aşağıdaki örnekte yayılma, h1 bloğunun içine yerleştirilmiştir.

**küstah**

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

Karışımlar, birden çok yerde kullanılan benzer özellikleri bir arada gruplandırmak için kullanılır. Karışımlar ayrıca parametreleri destekler.

**küstah**

**Bir karışımın bildirilmesi**

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

**Bir karışım kullanarak**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Genişletme/Kalıtım, bir seçicinin özelliklerinin başka bir seçiciyle paylaşılmasının gerektiği durumlarda faydalı olabilir. Aşağıdaki örnekte *.error-notice* seçici, *.error-text* seçicinin tüm özelliklerini alır ve kenarlık ve dolgu özellikleri ekler.

**küstah**

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

Stillerinizi, işlevselliğe veya izlediğiniz diğer herhangi bir yapıya dayalı olarak farklı dosyalarda yapılandırırsanız, içe aktarma yararlı olabilir. Tüm bu dosyaları, daha sonra CSS'ye dönüştürülecek olan birincil SASS dosyasına aktarabilirsiniz. İçe aktarırken, içe aktarma talimatında dosya uzantısını belirtmeniz gerekmez. Sass, tüm SASS dosyalarını doğrudan derler. İçe aktarma dosyalarının doğrudan derlenmesini önlemek için, adlarının başına alt çizgi(_) ekleyerek dosyaları kısmi hale getirebilirsiniz. Kısmi dosyalar, normal Sass dosyalarına benzer şekilde içe aktarılır.

**küstah**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Çıktı CSS, içe aktarılan tüm dosyalardan stillere sahip olacaktır.

## Referanslar ##

- [Sass - Vikipedi](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

