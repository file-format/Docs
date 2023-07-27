{
  "date" : "2021-01-21",
  "keywords" :[ "ai dosyası", "ai dosya biçimi", "ai dosyası nedir", "dosya", "ai örneği", "ai dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Adobe Illustrator Çizim Dosyası",
  "description":"AI dosya formatı ve AI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## .ai dosyası nedir?

.ai uzantılı bir dosya, tek bir sayfada vektör grafikleri içeren bir Adobe Illustrator Artwork dosyasıdır. görüntü verilerini görüntülemek için yollar oluşturmak üzere noktaları kullanır, böylece büyütülürse görüntü kalitesinin kaybolmasını önler. AI dosya formatı, AI dosyalarına benzer olan PGF dosya formatının temelidir. AI formatı, logolar ve basılı medya için başlıca kullanımını bulur ve ilk sürümlerinin [EPS](/tr/page-description-language/eps/) dosyalarına benzer olduğu kabul edilir. AI dosyaları Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro ve CorelDraw Graphics araçlarıyla açılabilir.

## AI Dosya Biçimi

AI, Adobe Illustrator'ın tescilli dosya formatıdır ve EPS uyumlu dosyaları kaydetmek için PGF'ye benzer ikili yol yaklaşımını kullanır. [Adobe Illustrator Dosya Biçimi belirtimleri](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) ayrıntılı bilgi sağlar. Bu dosya biçiminin dahili ayrıntıları için geliştiricinin referansı. Tümü Adobe Illustrator tarafından oluşturulan belgeler (dosyalar) PostScript dil belgeleridir ve Belge Yapılandırma Kurallarına uyan iki ana bölümden oluşur: bir "prolog" ve bir "komut dosyası".

### Önsöz

Prolog bölümü, dosyanın yorumlanması için gerekli bilgileri kapsar. Bir örnek, sayfadaki tüm işaretleri içeren sınırlayıcı kutu olabilir. Ayrıca yazı tipleri ve prosedür tanımları gibi kaynak bilgilerini de içerir. Bu kaynaklar mantıksal olarak procset adı verilen kümeler halinde gruplanır ve prosedürlerini başlatmak ve sonlandırmak için açık yöntemler içerir.

### Senaryo

Sayfadaki grafik öğeler komut dosyası tarafından tanımlanır. Bir betik, işlenenler ve verilerle birlikte prologtaki işleçlere ve prosedürlere referanslar içerir. Bir betiğin üç mantıksal bölümü şunları içerir:

* Kurulum Sırası - prolog'da tanımlanan kaynakları başlatan ve etkinleştiren
* Tanımlayıcı operatörlerin sırası
* Kaynakları devre dışı bırakan fragman

Komut dosyasındaki işleçler, prolog'da procsets tarafından tanımlanan dilde yazılmış grafik öğeleri dizileridir. Bu diziler, veri öğeleri koleksiyonlarından, grafik öznitelik tanımlarından ve süreç setlerinde tanımlanan prosedür çağrılarından oluşur.

### Nesne Etiketleri

Nesne etiketleri, bir Adobe Illustrator sanat nesnesine özel bilgiler eklemek için kullanılır. Etiketler şunlardan oluşur:

* Etiket tanımlayıcı
* Etiket türü
* Veri

## Referanslar
* [Adobe Illustrator Dosya Biçimi Özellikleri](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [PaintShopPro tarafından AI Dosya Biçimi](https://www.paintshoppro.com/en/pages/ai-file/)

