{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "dosya", "dosya formatı", "Sayfa Açıklama Dili", "Ölçek" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"SVG dosya formatı ve SVG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"SVG dosyası nedir?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## SVG dosyası nedir? ##

Bir SVG dosyası, bir görüntünün görünümünü açıklamak için XML tabanlı metin formatı kullanan bir Skaler Vektör Grafik dosyasıdır. Ölçeklenebilir kelimesi, SVG'nin herhangi bir kalite kaybı olmadan farklı boyutlara ölçeklenebilmesini ifade eder. Bu tür dosyaların metin tabanlı açıklaması, onları çözünürlükten bağımsız kılar. Ölçeklenebilirlik elde etmek için bir web sitesi oluşturmak ve grafikleri yazdırmak için en çok kullanılan biçimlerden biridir. Format ancak iki boyutlu grafikler için kullanılabilir. SVG dosyaları, Chrome, Internet Explorer, Firefox ve Safari dahil neredeyse tüm modern tarayıcılarda görüntülenebilir/açılabilir.

## Kısa Tarih ##

SVG spesifikasyonları, 1999'dan beri World Wide Web Consortium (W3C) tarafından açık standart olarak mevcuttur. Bundan önce, altı farklı formattaki benzer dosya formatı spesifikasyonları, 1998 yılına kadar W3C'ye sunuldu. Spesifikasyonlara 2011 yılında bir güncelleme uygulandı ve 1.1 sürümüne getirildi. . 2016 yılında, SVG 2, SVG 1.1'dekilere ek özellikler içeren daha yeni bir sürüm olarak yayınlandı.

## Dosya Biçimi Özellikleri ##

SVG Belge Nesne Modeli (DOM), belirtimlerin belirli bölümlerine karşılık gelen tüm belirtimlerin ve arabirimlerin temellerini atar. SVG görüntüleyiciler, SVG DOM arabirimlerini W3C belirtimlerinde tanımlandığı şekilde uygulamalıdır. DOM'si, farklı veri türleri ve öğeleri için çeşitli arabirimler sunar.

### SVG şekilleri ###

SVG, geliştiriciler tarafından kullanılabilecek önceden tanımlanmış bazı şekil öğelerine sahiptir:

* Dikdörtgen<rect>
* Daire<circle>
* Elips<ellipse>
* Astar<line>
* Çoklu çizgi<polyline>
* çokgen<polygon>
* Yol<path>

Bu şekil ve özelliklere göre SVG'nin işlevsel alanları aşağıdaki gibidir.

**Yollar** - Yollar, basit ve bileşik şekil ana hatlarını temsil etmek için kullanılır. İşlemin doğasını tanımlamak için kodlamalar kullanılır. Örneğin, M Taşı için kullanılır, L Satır Hedefi için kullanılır, Z yolu kapatmak için kullanılır vb.

**Temel Şekiller** - Düz çizgi yolları ve bir dizi bağlı düz çizgi parçalarından (sürekli çizgiler) oluşan yollar, ayrıca kapalı çokgenler, daireler ve elipsler çizilebilir. Dikdörtgenler ve yuvarlak köşeli dikdörtgenler de standart öğelerdir.

**Metin** - Metin temsili, metne birçok görsel efektin uygulanabileceği XML karakter verileri olarak ifade edilir. Spesifikasyonlar, çift yönlü metin, dikey metin ve karakterlerin kavisli bir yol boyunca işlenmesine izin verir.

**Boyama** - Şekiller, bir renk, bir degrade veya desenle doldurulabilir ve/veya ana hatları çizilebilir; Bir çokgenin köşelerinde görünen ok uçları veya semboller gibi çizgi sonu özellikleri, İşaretleyiciler tarafından temsil edilir.

**Renk** - SVG spesifikasyonları, tüm görünür SVG öğelerine doğrudan veya dolgu, kontur ve diğer özellikler aracılığıyla renklerin uygulanmasına izin verir. Siyah veya mavi, onaltılı temsil, ondalık veya RGB formunun yüzdeleri gibi belirtmek için farklı renk kodlamaları kullanılabilir.

**Degradeler ve Desenler** - Bir SVG dosyasındaki şekiller düz renkler, degradeler veya yinelenen desenlerle doldurulabilir veya ana hatları çizilebilir.

**Filtre Efektleri** - Aslında, değiştirilmiş sonuç üretmek için verilen kaynak vektör grafiğine uygulanan bir dizi grafik işlemidir.

**Etkileşim** - Kullanıcılar, odağı değiştirerek, fareyi tıklatarak, görüntüyü kaydırarak veya yakınlaştırarak SVG dosyalarıyla etkileşim kurabilir. Etkileşim, SVG görüntülerinin, daha önce belirtildiği gibi, kullanıcılarla birçok farklı şekilde etkileşim kurmasını sağlar.

**Bağlantı** - SVG görüntülerinin diğer belgelere köprüleri olması mümkündür. Bu, XML Bağlama Dili veya XLink aracılığıyla gerçekleştirilir. Bu, belirli bir alanı yakınlaştırmak/uzaklaştırmak veya görünümü belirli bir öğeyle sınırlamak için kullanılan belirli görünüm durumları oluşturmaya izin verir.

**Komut Dosyası Oluşturma** - HTML'ye benzer şekilde, bir SVG belgesinin tüm yönlerine komut dosyaları kullanılarak müdahale için erişilebilir. SVG DOM nesneleri, SVG öğesini ve niteliğini kullanarak bunu başarmak için rehberlik sağlar. Komut dosyaları, "komut dosyası" etiketi öğeleri içine alınır ve gerektiğinde işaretçi, klavye veya belge olaylarına yanıt olarak çalışabilir.

**Animasyon** - DOM öğeleri<animate> ,<animateMotion> ve<animateColor> SVG içerikleri için animasyon eklemenizi sağlar. Elbette bu, betikler ve yerleşik zamanlayıcılar kullanılmadan gerçekleştirilemez. Bu animasyonlar sürekli olabilir ve kullanıcı olaylarına yanıt verirken aynı zamanda tekrarların yanı sıra döngüye alınabilir.

**Yazı Tipleri** - SVG'deki metin, sistem yazı tipleri gibi harici yazı tipi dosyalarına başvurabilir. Bu tür yazı tiplerinin yokluğunda, SVG'deki metin çıktıya işlenmez. Bu, gerekli glifleri daha sonra kullanılarak işlenen bir yazı tipi gibi bir dosyaya dahil ederek aşılabilir.<text> öğe.

## Örnekler ##
Aşağıdaki satırlar, bir Çemberin SVG betiği kullanılarak nasıl temsil edildiğini gösterir.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Aşağıdaki kod satırları, nasıl kullanılacağını gösterir.<text> metni SVG'ye dönüştürmek için blok.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Referanslar ##

* [W3C SVG Spesifikasyonları](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

