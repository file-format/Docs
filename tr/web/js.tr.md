---
date: 2019-10-11
keywords: js, .js, js dosya formatı, js dosyaları nasıl açılır, javascript dosyaları
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS Dosya Biçimi
linktitle: JS
description: "JS dosya formatı ve JS dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## JS dosyası nedir? ##

JS (JavaScript), web sayfalarında yürütme için JavaScript kodu içeren dosyalardır. JavaScript dosyaları .js uzantısıyla depolanır. [HTML](/tr/web/html/) belgesinin içine, JavaScript kodunu \ <script>\</script> etiketler veya bir JS dosyası içerir. [CSS](/tr/web/css/) dosyalarına benzer şekilde, kodun yeniden kullanılabilirliği için JS dosyaları birden fazla HTML belgesine dahil edilebilir. JavaScript, HTML DOM'u değiştirmek için kullanılabilir.

## Kısa Tarih ##

JavaScript, Navigator Browser'ın bir parçası olarak Eylül 1995'te Netscape tarafından LiveScript adıyla piyasaya sürüldü. Üç ay sonra JavaScript olarak yeniden adlandırıldı. 1996'da Microsoft, JScript oluşturmak için Navigator'ın yorumlayıcısının tersine mühendislik yaptı. JScript, Internet Explorer ile yayınlandı ve JavaScript'ten çok farklıydı.

Netscape, ECMA International'a JavaScript'i göndererek 1997'de ilk ECMAScript spesifikasyonunun resmi olarak yayınlanmasına yol açtı. ECMAScript 2 1998'de, ECMAScript 3 1999'da piyasaya sürüldü ve ECMAScript 4 üzerindeki çalışmalar 2000'de başladı, ancak hiçbir zaman meyvesini vermedi.

Jesse James Garrett, 2005 yılında *Ajax* terimini icat ettiği bir tanıtım yazısı yayınladı. Bu, JavaScript'i arka planda veri yükleyen ve tam sayfa yeniden yüklemelerinden kaçınan web uygulamaları oluşturmak için omurga olarak kullandı. Bu, JQuery, Prototype, Dojo, vb. gibi kitaplıkların oluşturulmasıyla sonuçlandı.

Google, 2008'de V8 JavaScript motoruna sahip Chrome tarayıcıyı piyasaya sürdü. 2009'un başlarında, ilgili tüm çalışmaları birleştirmek ve JavaScript'i ileriye taşımak için bir anlaşma yapıldı. Bu, Aralık 2009'da ECMAScript 5 Standardının yayınlanmasıyla sonuçlandı.

## JS dosyaları nasıl kullanılır ##

Bir JS dosyası kullanmak için onu HTML belgesine eklersiniz. Dosyayı aşağıda gösterildiği gibi dahil etmek için bağlantı etiketini kullanırsınız.

```html
<script src="site.js"></script>
```

*script* etiketinin *src* niteliği, JS dosyasının yolunu içerir. Bunu yaparak, JS işlevselliği HTML belgesine eklenir.

## JS Sözdizimi ##

JavaScript dosyaları değişkenler, işleçler, işlevler, koşullar, döngüler, diziler, nesneler vb. içerebilir. Aşağıda JavaScript'in söz dizimine kısa bir genel bakış verilmiştir.

- Her komut bir noktalı virgülle (;) biter.
- Değişkenleri bildirmek için *var* anahtar sözcüğünü kullanın.
- Değerleri hesaplamak için aritmetik operatörleri ( + - * / ) destekler.
- Tek satırlık yorumlar // ile eklenir ve çok satırlı yorumlar /* ve */ ile çevrelenir.
- Tüm tanımlayıcılar büyük/küçük harfe duyarlıdır, yani *modelNo* ve *modelno* iki farklı değişkendir.
- Fonksiyonlar *function* anahtar sözcüğü kullanılarak tanımlanır.
- Diziler köşeli parantez [] kullanılarak tanımlanabilir.
- JS, ==, != , >=, !==, vb. gibi karşılaştırma işleçlerini destekler.
- Sınıflar *class* anahtar sözcüğü kullanılarak tanımlanabilir.

## JS Kullanım Örneği ##

Aşağıda basit bir kullanım örneği JavaScript dosyası gösterilmektedir.

### HTML Belgesi ###

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

## Referanslar ##

- [JS - Vikipedi](https://en.wikipedia.org/wiki/JavaScript)

