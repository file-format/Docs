{
  "date" : "2019-10-11",
  "keywords" :[ "html","html dosyası", "html dosya biçimi", "html dosya türü", "dosya", "tür", "html dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTML Dosya Biçimi",
  "description":"HTML dosya formatı ve HTML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## HTML dosyası nedir?

HTML (Hyper Text Markup Language), tarayıcılarda görüntülenmek üzere oluşturulan web sayfalarının uzantısıdır. Web dili olarak bilinen HTML, web sayfalarının bir parçası olarak görüntülenecek yeni bilgi gereksinimlerinin gereksinimleriyle gelişmiştir. En son değişken, dille çalışmak için çok fazla esneklik sağlayan HTML 5 olarak bilinir. HTML sayfaları, barındırıldıkları sunucudan alınır veya yerel sistemden de yüklenebilir. Her HTML sayfası, formlar, metin, resimler, animasyonlar, bağlantılar vb. Ayrıca, genel mizanpaj gösterimi için JavaScript ve Stil Sayfaları (CSS) gibi betik dillerinde yazılmış uygulamaları da gömebilir.

## Kısa Tarih ##

Başlangıcından ve ilk ortaya çıkışından bu yana, HTML spesifikasyonları 1996'dan beri World Wide Web Konsorsiyumu (W3C) tarafından sürdürülmektedir. 2000 yılında ayrıca uluslararası bir standart haline gelmiştir (ISO/IEC 15445:2000). 1999'da HTML 4.01 yayınlandı. 2004 yılında Web Köprü Metni Uygulama Teknolojisi Çalışma Grubu (WHATWG), 2008 yılında W3C ile ortak çıktı haline gelen HTML5 sürümü üzerinde çalışmaya başladı. 28 Ekim 2014 tarihinde tamamlanarak standart hale getirildi.

## HTML Dosya Biçimi Yapısı ##

Bir HTML 4 belgesi üç bölümden oluşur:

1. HTML sürüm bilgilerini içeren bir satır
1. bildirim niteliğinde bir başlık bölümü
1. belgenin gerçek içeriğini içeren bir gövde. Gövde, gövdeyi çerçeveler içinde tutmak için BODY öğesi veya FRAMESET öğesi tarafından uygulanabilir.

Her bölümün başında veya sonunda beyaz boşluklar, yeni satırlar, sekmeler ve yorumlar olabilir. Basit bir HTML belgesi örneği aşağıda gösterildiği gibidir:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Versiyon bilgisi ###

İlk kod satırı, \<!DOCTYPE html> , belge türü bildirimi olarak adlandırılır ve tarayıcıya sayfanın hangi HTML sürümünün yazıldığını söyler. HTML sürümüne bağlı olarak, belge için kullanılan belge türü tanımını (DTD) adlandıran bir dizi farklı belge türü bildirimi vardır. Her DTD, desteklediği öğeler açısından diğerinden farklıdır ve aşağıdaki gibi farklılık gösterir:

* HTML 4.01 Strict - [kullanımdan kaldırılmamış](https://www.w3.org/TR/html401/conform.html#deprecated) veya çerçeve kümesi belgelerinde görünmeyen tüm öğeleri ve nitelikleri içerir
* HTML 4.01 Transitional - katı DTD'deki her şeyi artı kullanımdan kaldırılmış öğeleri ve nitelikleri içerir (çoğu görsel sunumla ilgilidir)
* HTML 4.01 Çerçeve Kümesi - geçiş DTD artı çerçevelerdeki her şeyi içerir

**HTML5** için sürüm bilgisi basitçe aşağıda belirtildiği gibidir.

```
<!DOCTYPE html>
```

### HTML Başlık Bilgisi ###

Bir HTML belgesinin başlığı, tarayıcı tarafından oluşturulmayan bir dizi HTML öğesi içerebilir. Bu tür öğeler, sayfa hakkındaki bilgileri açıklayan meta verilerdir veya CSS stil sayfaları veya JavaScript dosyaları gibi harici kaynaklardan bilgi almak için kullanılan bölümleri içerir. Bir sayfanın başlığı, başlık etiketi ile temsil edilir.

Sayfa başlığını ayarlamak için, **başlık** öğesi, sayfa içinde gerekli olan tek öğedir.<head> etiketler. Aynı arama motorları tarafından bir sayfanın başlığını belirlemek için kullanılır.

### HTML Gövde Bilgisi ###

Bu, dosyanın tarayıcılar tarafından oluşturulan tüm içeriğini içeren ana bölümdür. Html gövdesi, etiketler şeklinde çeşitli yapı taşlarına atıfta bulunabilen işaretlemeler içerebilir. Metin, resimler, renkler, grafikler vb. gibi birkaç farklı türde bilgi içerebilir. Ayrıca, ses ve video öğeleri de tarayıcılar tarafından işlenmek üzere html gövdesine gömülebilir. Görsel sunum için modern stil sayfaları uygulamasının varlığında, BODY'nin arka plan rengi, bağlantı rengi, metin rengi vb. sunum nitelikleri kullanımdan kaldırılmıştır. Böylece, aşağıda gösterilen stil sayfaları kullanılarak aynı efektler elde edilebilir:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Satır içi stil sayfalarının yerleştirilmesi kolaydır ve görsel efektlere hızlı uygulamalar için, harici stil sayfalarını bir kez dağıtmayı ve birçok yerden erişmeyi daha kolay hale getirir.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML Öğeleri ###

Daha önce bahsedildiği gibi, HTML Gövdesi içindeki içerikler, Html Öğeleri olarak da bilinen etiketlerle temsil edilir. Her etiket, şu şekilde yazılan nitelikler biçiminde ek bilgilere sahip olabilir:<tag attribute1#"value1" attribute2#"value2"> , ancak her etikette niteliklere sahip olmak gerekli değildir. Özniteliklerden bahsedilmiyorsa, her durumda varsayılan değerler kullanılır. Element örneklerinden bazıları aşağıda verilmiştir:

#### Başlık ####

```
<head>
  <title>The Title</title>
</head>
```

#### Başlıklar ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Paragraflar ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Referanslar ##

* [HTML belgesinin Global Yapısı](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

