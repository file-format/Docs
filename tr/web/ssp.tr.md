---
date: 2021-07-05
keywords: ssp, .ssp, ssp dosya formatı, ssp dosyaları nasıl açılır, Scala Sunucu Sayfası
yazar:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Sunucu Sayfaları Dosya Biçimi
linktitle: SSP
description: "SSP dosya biçiminin ne olduğu ve SSP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## SSP dosyası nedir?

.ssp uzantılı bir dosya, sadece düz HTML yerine ifadeler için Scala kodu ile oluşturulan web sayfasıdır. HTML ve Scala kombinasyonunu kullanan bir sunucu tarafı komut dosyası görevi görür. Bu dosyalar sunucuda bulunur ve kullanıcılara sunulmak üzere statik web sayfaları oluşturmak için kullanılır. Scala'nın kendisi, sözdizimi Velocity, JSP veya Erb ile çalışan kullanıcıların aşina olduğu genel amaçlı bir programlama dilidir. SSP dosyaları, metin ve işaretleme oluşturmak için Scala tabanlı bir şablon motoru olan [Scalate](https://scalate.github.io/scalate/) kullanılarak analiz edilebilir ve değerlendirilebilir.

## SSP Dosya Formatı - Daha Fazla Bilgi

SSP dosyaları düz metin dosyasına kaydedilir ve Scalate kullanılarak değerlendirilebilir. Bir Ssp şablonu, genellikle HTML belgesi olan düz metinden oluşur. Oluşturma motorlarının belgenin farklı bölümlerini dinamik olarak işlemesine neden olan gömülü Ssp etiketlerine sahiptir. Etiketler <% ... %> ve ${ ... } dizisi ile başlar ve biter ve bunların dışındaki her şey sabit metin olarak kabul edilir.

### SSP Örneği

Aşağıdaki örnek, işleme motoru tarafından işlendiğinde SSP kodunu ve çıktısını gösterir.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Çıktı aşağıdaki gibidir.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Referanslar

- [SSP Referansı](https://scalate.github.io/scalate/documentation/ssp-reference.html)

