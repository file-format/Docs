---
date: 2019-10-11
keywords: json, .json, json dosya formatı, json dosyaları nasıl açılır, javascript nesne gösterimi, json veri formatı, .json dosya formatı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON Dosya Biçimi - JSON dosyası nedir?
linktitle: JSON
description: "JSON dosya biçimi ve JSON dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## JSON dosyası nedir?

JSON (JavaScript Object Notation), verileri depolamak ve iletmek için insanlar tarafından okunabilir metin kullanan, verileri paylaşmak için açık standart bir dosya biçimidir. JSON dosyaları .json uzantısıyla depolanır. JSON daha az biçimlendirme gerektirir ve [XML](/tr/web/xml/) için iyi bir alternatiftir. JSON, JavaScript'ten türetilmiştir ancak dilden bağımsız bir veri biçimidir. JSON'un oluşturulması ve ayrıştırılması, birçok modern programlama dili tarafından desteklenir. *application/json*, JSON için kullanılan ortam türüdür.

## JSON Dosya Biçimi - Kısa Tarihçe

JSON'un yaratılmasına yol açan gerçek zamanlı sunucudan istemciye iletişime ihtiyaç vardı. JSON formatı ilk olarak Mart 2001'de Douglas Crockford tarafından belirtildi. JSON, JavaScript'in bir alt kümesi olan Standard ECMA-262 3rd Edition—Aralık 1999'a dayanıyordu.

JSON standardı ECMA-404'ün ilk baskısı Ekim 2013'te Ecma International tarafından yayınlandı. RFC 7159, 2014 yılında JSON'un İnternet kullanımları için ana referans oldu. Kasım 2017'de uluslararası bir standart olarak ISO/IEC 21778:2017 yayınlandı. RFC 8259, İnternet Standardı STD 90'ın güncel versiyonu olan İnternet Mühendisliği Görev Gücü tarafından 13 Aralık 2017'de yayınlandı.

## JSON Dosya Yapısı

JSON verileri **anahtar/değer** çiftleri halinde yazılır. Anahtar ve değer, solda anahtar ve sağda değer olmak üzere ortada iki nokta üst üste (:) ile ayrılır. Farklı anahtar/değer çiftleri virgül(,) ile ayrılır. Anahtar, örneğin "ad" gibi çift tırnak içine alınmış bir dizedir. Değerler aşağıdaki tiplerde olabilir.

- "Numara"
- `String`: Çift tırnak içine alınmış Unicode karakter dizisi.
- `Boolean`: Doğru veya Yanlış.
- "Dizi": Örneğin, köşeli parantez içine alınmış bir değerler listesi

json
[ "Elma", "Muz", "Portakal" ]
```

- "Nesne": Örneğin kaşlı ayraçlarla çevrelenmiş bir anahtar/değer çiftleri koleksiyonu

json
{"name": "Jack", "yaş": 30, "favori Spor" : "Futbol"}
```

JSON nesneleri, verilerin yapısını temsil edecek şekilde yuvalanabilir. Aşağıda verilen bir JSON nesnesi örneğidir.

### JSON Biçim Örneği

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## JSON dosyasının maksimum boyutu nedir?

Bir JSON dosyasının maksimum boyutunda neredeyse hiçbir sınır yoktur. Depolanacak içeriğin gerektirdiği alan kadar uzun olabilir.

İnternet üzerinden veri aktarımı için JSON dosya biçimini kullanmak söz konusu olduğunda, bilgisayarın mevcut kaynakları konusunda dikkatli olunması gerekir. Büyük JSON verileri aktarılırsa, istemci tarayıcısının sınırlı belleği varsa aktarım etkilenir.


Spesifikasyon tarafından tanımlanan kesin bir sınır yoktur, ancak kullanıcılarınızın bilgisayarlarındaki kaynakları tüketmemeye dikkat etmelisiniz çünkü bu, kullanıcı deneyimlerini hızlı bir şekilde bozar ve muhtemelen uygulamanızı terk ederler.

## JSON ve XML

**XML**, internet üzerinden veri alışverişi için yaygın olarak kullanılan başka bir dosya biçimidir. Uygulamalar arasında veri alışverişi söz konusu olduğunda, geliştiricilerin hem XML hem de JSON dosya biçimlerini kullanma seçeneği vardır. Ancak aşağıdaki nedenlerden dolayı internet üzerinden uygulamalar arasında veri alışverişi için en uygun yol olarak JSON benimsenmiştir.

1. JSON, XML dosya biçimlerine kıyasla net ve okunması kolay bir veri görünümü sağlar
1. JSON, XML'e kıyasla aynı veri kümesini tanımlamak için daha az sayıda karaktere sahip olduğundan, internet üzerinden veri aktarımı yükünü azaltır
1. Modern programlama dilleri, JSON yanıtını web üzerinden ayrıştırmak için yerleşik ayrıştırıcılar sağlar.

## Biliyor musun?

Bulgularınızla dosya formatı topluluğunu güncel tutmak için FileFormat.com'a katkıda bulunabilirsiniz. JSON veya Web dosya biçimleri hakkında herhangi bir şey paylaşmanız gerekiyorsa, insanların bunlardan daha fazla bilgi edinmesi için bulgularınızı [Web Dosya Biçimi Haberleri](https://news.fileformat.com/t/Web) bölümünde yayınlayabilirsiniz.

## Referanslar

- [JSON - Vikipedi](https://en.wikipedia.org/wiki/CSS)
- [JSON'a Giriş](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

