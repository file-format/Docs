---
date: 2019-10-11
keywords: css, .css, css dosya formatı, css dosyalarının nasıl açılacağı, basamaklı stil sayfaları
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS Dosya Biçimi
linktitle: CSS
description: "CSS dosya biçimi ve CSS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## CSS dosyası nedir? ##

CSS (Basamaklı Stil Sayfaları), HTML öğelerinin ekranda, kağıtta vb. nasıl görüntülendiğini açıklayan dosyalardır. HTML ile, gömülü stiller olabilir veya stiller harici bir stil sayfasında tanımlanabilir. Stilleri gömmek için \ <style>\</style> etiketler kullanılır. Harici stil sayfaları, .css uzantılı dosyalarda saklanır. Harici CSS ile, bu sayfaların stilini güncellemek için onu birden çok HTML sayfasına ekleyebilirsiniz. Eksiksiz bir web sitesine stil vermek için tek bir CSS dosyası bile kullanılabilir.

## Kısa Tarih ##

CSS1, ortak yazar olarak Bert Bos ile 1996 yılında piyasaya sürüldü. CSS Çalışma Grubu, CSS1'de ele alınmayan konular üzerinde çalışmaya başladı. Bunun sonucunda, Kasım 1997'de, 12 Mayıs 1998'de bir W3C tavsiyesi olarak yayınlanan CSS2 oluşturuldu. Bu sürüm, yazıcılar, indirilebilir yazı tipleri, tablolar ve öğe konumlandırma gibi ortama özgü cihazlar için destek ekledi. Haziran 1999'da CSS3, W3C'nin tavsiyesi oldu. Bu, belgeleri, her modülün CSS2'de tanımlanan uzantı özelliklerine sahip olduğu modüllere ayırdı.

## CSS dosyaları nasıl kullanılır ##

Bir CSS dosyasını kullanmak için, onu HTML belgesinin baş bölümüne eklersiniz. Dosyayı aşağıda gösterildiği gibi dahil etmek için bağlantı etiketini kullanırsınız.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

link etiketinin *href* niteliği, CSS dosyasının yolunu içerir. Bunu yaparak, dahil edilen CSS dosyasında bulunan uygulanabilir stiller HTML belgesine uygulanır.

## CSS Sözdizimi ##

Bir CSS kuralı, seçici ve bildirim olmak üzere iki bileşenden oluşur. Bir seçici, HTML belgesindeki bir öğeye işaret eder. Bir öğe etiketi, sınıf adı, kimlik adı, hiyerarşiyi gösteren çoklu etiketler vb. olabilir. Bir bildirim, özellik ve değerden oluşan stil tanımını içerir. Özellik, değiştirmek istediğiniz öğenin özelliğini tanımlar ve değer, onun yeni değerini tanımlar. Her CSS kuralının birden çok bildirimi olabilir. Aşağıda bir CSS kuralı örneği verilmiştir.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Yukarıdaki örnekte, HTML belgesindeki tüm h1 etiketlerini seçen bir seçici olarak **h1**'e sahibiz. Kuralın biri yazı tipi ağırlığı ve diğeri renk için olmak üzere iki bildirimi vardır. *font-weight* ve *color* özelliklerdir ve sırasıyla *700* ve *forestgreen* değerleridir.

## CSS Kullanım Örneği ##

Aşağıda, örnek HTML belgesi ve onu biçimlendirmek için kullanılan stil sayfası gösterilmektedir. Stil sahibi ve düz HTML belgelerini karşılaştırmak için karşılaştırma görüntüsü de eklenir.

### HTML Belgesi ###

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

### CSS Stil Sayfası ###

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

### Çıktı Karşılaştırması ###

Resmin sol tarafı, HTML belgesini stiller uygulanmadan, sağ tarafı ise HTML belgesini stiller uygulanmış olarak görüntüler.

{{< figure src="../CssExample.jpg" alt="Örnek resim" >}}

## Referanslar ##

- [CSS - Vikipedi](https://en.wikipedia.org/wiki/CSS)

