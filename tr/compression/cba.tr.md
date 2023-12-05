{
"tarih": "2023-05-24",
  "keywords": [
"cba dosyası",
"cba dosyası nedir",
"CBA dosyası nasıl oluşturulur",
"CBA dosyası neler içeriyor",
"cba dosyasının formatı nedir",
"dosya",
"cba dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CBA Dosya Formatı - Çizgi Roman Arşivi",
  "description":"CBA formatı ve CBA dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "CBA",
  "menu": {
    "docs": {
      "identifier": "compression-cba",
      "parent": "compression"
}
},
"sonmod": "2023-05-24"
}

## .CBA dosyası nedir?

Çizgi Roman Arşivi veya Çizgi Roman Okuyucu dosyası olarak da bilinen Çizgi Roman Arşivi (CBA) dosyası, dijital çizgi romanları depolamak ve dağıtmak için kullanılan popüler bir formattır. Genellikle kolay düzenleme ve okuma için tek tek çizgi roman sayfalarının veya tek bir dosyada bir araya getirilmiş görsellerin koleksiyonunu içerir.

Çizgi Roman Arşivi dosyaları oluşturmak için yaygın olarak kullanılan formatlardan biri TAR (Kaset Arşivi) formatıdır. TAR, Unix ve Linux ortamlarında kullanılan bir dosya arşivleme formatıdır. Birden fazla dosyayı, genellikle yedekleme amacıyla kullanılan tek bir dosyada birleştirir.

## CBA dosyası nasıl oluşturulur?

TAR arşivleme aracını kullanarak Çizgi Roman Arşivi dosyası oluşturmak için genellikle şu adımları izlersiniz:

1. Arşive eklemek istediğiniz tüm çizgi roman sayfalarını veya görsellerini toplayın.
2. Bir komut istemi veya terminal penceresi açın.
3. Çizgi roman sayfalarının/görsellerinin bulunduğu dizine gidin.
4. Arşivi oluşturmak için TAR komutunu uygun seçeneklerle kullanın. Örneğin komut şu şekilde görünebilir:

```
tar -cf comicbook.cbt page1.jpg page2.jpg page3.jpg
```

Bu örnekte, -c seçeneği TAR'a yeni arşiv oluşturmasını söyler ve -f seçeneği çıktı dosyasının adını belirtir (bu durumda comicbook.cbt). Seçenekleri belirledikten sonra arşive dahil etmek istediğiniz dosyaların isimlerini (sayfa1.jpg, sayfa2.jpg, sayfa3.jpg) veriyorsunuz.

5. Komutu yürüttükten sonra TAR aracı, geçerli dizinde Çizgi Roman Arşivi dosyasını (bu örnekte comicbook.cbt) oluşturacaktır.

Çizgi Roman Arşivi dosyanıza sahip olduğunuzda, bilgisayarınızda veya cihazınızda çizgi roman açmak ve okumak için çeşitli çizgi roman okuyucu yazılımlarını veya uygulamalarını kullanabilirsiniz. Bu uygulamalar genellikle okuma deneyimini geliştirmek için sayfada gezinme, yakınlaştırma ve yer imi ekleme gibi özellikler sağlar.

## CBA dosyası neler içeriyor?

TAR arşivleme aracı kullanılarak oluşturulan bir Çizgi Roman Arşivi (CBA) dosyası, tek bir dosyada bir araya getirilmiş ayrı çizgi roman sayfaları veya resimlerden oluşan bir koleksiyon içerir. Arşivin belirli içeriği, paketlenen çizgi romana bağlıdır.

Tipik olarak bir Çizgi Roman Arşivi dosyası aşağıdakileri içerir:

- **Çizgi roman sayfaları:** Arşivin ana içeriği çizgi roman sayfalarının kendisidir. Bu sayfalar genellikle çizgi romanın her sayfasını temsil eden JPEG veya PNG gibi ayrı görüntü dosyaları olarak kaydedilir. Çizgi romanın anlatım akışını sürdürmek için sayfalar belirli bir sıraya göre düzenlenmiştir.
- **Meta veriler:** Bazı Çizgi Roman Arşivi formatları, çizgi roman hakkında başlık, yazar, yayıncı, yayın tarihi ve açıklama gibi meta veriler içerebilir. Bu bilgi çizgi romanın tanımlanmasına ve sınıflandırılmasına yardımcı olur.
- **Ek dosyalar:** Çizgi roman sayfaları ve meta verilere ek olarak arşiv, çizgi romanla ilgili başka ek dosyalar da içerebilir. Bu dosyalar kapak resmi, tanıtım görselleri, bonus içerik veya ek bilgi veya yorum sağlayan metin dosyalarını içerebilir.

## CBA dosyasının formatı nedir?

TAR arşivleme aracı kullanılarak oluşturulan Çizgi Roman Arşivi (CBA) dosya formatı genellikle TAR formatındadır. Tape Archive'ın kısaltması olan TAR, Unix ve Linux sistemlerinde yaygın olarak kullanılan bir dosya arşivleme formatıdır. Çizgi romanlara özel olmayıp genel amaçlı bir arşivleme formatıdır.

TAR formatı, birden fazla dosyayı tek bir arşiv dosyasında birleştirmenin basit bir yoludur. Kendi başına sıkıştırma sağlamaz, bu nedenle ortaya çıkan TAR dosyasının boyutu, ZIP veya RAR gibi diğer sıkıştırılmış formatlarla karşılaştırıldığında büyük olabilir. Ancak TAR dosyaları ek araçlar kullanılarak sıkıştırılabilir veya dosya boyutunu küçültmek için gzip veya bzip2 gibi sıkıştırma algoritmalarıyla birleştirilebilir.

TAR formatı, dahil edilen dosyaların dosya yapısını, dosya izinlerini ve zaman damgalarını korur. Dosyaları arşiv içinde sırayla saklayarak tek tek dosyaların veya arşivin tamamının kolayca çıkarılmasına olanak tanır.

## Referanslar
* [Çizgi roman arşivi](https://en.wikipedia.org/wiki/Comic_book_archive)

