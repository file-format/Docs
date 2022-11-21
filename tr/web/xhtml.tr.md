{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Dosya", "Uzantı", "Dosya Biçimi", "Dosya Uzantısı", "genişletilebilir html"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Genişletilebilir Köprü Metni Biçimlendirme Dili Dosya Biçimi",
  "description":"XHTML dosya biçiminin ne olduğunu ve XHTML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Bir XHTML dosyası nedir?

XHTML, HTML 4.0'ın yeniden formülasyonunu kullanan, XML'de biçimlendirme içeren metin tabanlı bir dosya biçimidir. Bu dosyalar, bir web tarayıcısında açılmaya veya görüntülenmeye çok uygundur. XHTML daha yapılandırılmış, daha az komut dosyası içeren, genel olacak şekilde tasarlanmıştır; XML'in mevcut tüm olanaklarını kullanarak ve daha fazla cihazdan bağımsız olarak. XHTML, stil sayfalarıyla birlikte uzantı seçenekleriyle genel olarak değerli bir dizi öğe ve nitelik sağlar. Öznitelikler, meta veri öznitelikleri koleksiyonundan kullanılır. XHTML, tüm **[HTML](/tr/web/html/)** sunum öğelerini stil sayfalarına tabi kılarak esneklik ve erişilebilirlik sağlar. Stil sayfaları, bu sunum öğelerinden daha çok yönlüdür. HTML 4.01, HTML5 ve XHTML spesifikasyonları, World Wide Web Consortium (W3C) tarafından dinamik olarak geliştirilmektedir.

## XHTML Dosya Biçiminin Kısa Tarihi

XHTML'nin tarihi, World Wide Web Konsorsiyumu tarafından Aralık 1998'de yayınlanan bir taslak belgeyle başlar. Bu belge, XHTML 1.0 adlı bir belirtim olan "XML'de HTML'nin Yeniden Biçimlendirilmesi"ne atıfta bulunur. Bu yeni belirtim, varolan öğeleri veya öznitelikleri kullanarak HTML'yi XML'de yeniden formüle etmiştir. Mayıs 1999'da W3 Konsorsiyumu, HTML 4.0'ın bir XML uygulaması olarak yeniden biçimlendirildiğini açıkladı. yani XHTML. 26 Ocak 2000'de, XHTML 1.0'ı tanımlayan ilk belirtim W3C tarafından yayınlandı. Ayrıca 31 Mayıs 2001'de W3C, XHTML'yi bağımsız bir dil olarak duyurdu ve HTML 5.0'ın geliştirilmesi için çalışmaya başladı. Ancak 2005 yılında sıradan HTML'yi XHTML'den bağımsız olarak geliştirmeyi amaçlayan bir çalışma grubu (WHATWG) kuruldu. WHATWG sonunda XHTML 2'ye paralel olarak HTML5 üzerinde çalışmaya başladı.

## XHTML Dosya Biçimi

XHTML, HTML 4'ü taklit eden, kategorize eden ve genişleten farklı belge türlerinin ve modüllerin bir koleksiyonu olan bir biçimdir. XHTML'deki dosyalar XML tabanlıdır ve XML tabanlı kullanıcı aracılarıyla çalışmayı amaçlar. XHTML dosyaları XML uyumludur. XHTML dosyalarını görüntülemek, düzenlemek ve doğrulamak için standart XML araçları kullanılır. HTML Belge Nesne Modeli veya XML Belge Nesne Modeli [DOM] bağımlı uygulamalar, XHTML belgeleri aracılığıyla çalışabilir. Bugün XHTML'yi seçen içerik geliştiriciler, içeriklerinin ileri veya geri uyumluluğu konusunda endişe duymadan XML'in ilgili tüm avantajlarından yararlanabilirler.

Bir dizi ilgili öğe, XHTML'de bir modül oluşturur. Bir form veya tablo modülü, bir web sayfasında görüntülenebilen çeşitli form veya tablo öğeleri içerebilir. Modülerleştirme, HTML öğelerini çok sayıda bağlantılı öğe kümesine ayırmayı amaçladı. Böylece içerik geliştiriciler, farklı cihaz türleri için modül seçiminden faydalanabilir. Ayrıca modüller, kullanıcı aracılarının XHTML standardıyla tutarlılığı kaybetmeden öğeleri seçmesine olanak tanır. XHTML'nin ayrıştırma gereksinimleri XML ile aynıdır, HTML ise kendi uygulamalarını yapar.

### Belge Uygunluğu

XHTML2, XML ve XHTML 1.0'daki ad alanları öğelerini ve niteliklerini kullanan XHTML 1.0 belgelerine uygun özellikler sunar. Belge Uygunluğu iki türdendir.

Kesinlikle Uygun Belge, yalnızca bu belirtimde tanımlanan zorunlu hizmetlere ihtiyaç duyan XML tabanlıdır. XHTML dosyaları için aşağıdaki kriterlerin karşılanması gerekir:

* Bir dosya, DTD'lerde ve Ek B'de tanımlanan kısıtlamalara uygun olmalıdır.
* Dosyanın temel öğesi html olmalıdır.
* Dosyanın temel öğesi, XHTML ad alanı için bildirim içermeli ve şu şekilde tanımlanmalıdır:

```
http://www.w3.org/1999/xhtml.
```

* Temel eleman şu şekilde yazılabilir:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Temel öğeden önce, genel tanıtıcısı üç belge türü tanımından (DTD) birine başvurması gereken bir DOCTYPE bildirilmelidir. Sistem tanımlayıcısı, mevcut sistem kurallarına uymak için değiştirilebilir.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

XML belgelerinde, tüm belgelerde XML bildirimlerini belirtmek gereksizdir; ancak içerik geliştiriciler, tüm XHTML belgelerinde XML bildirimlerini kullanmaya ikna edilir. Belgenin karakter kodlaması UTF-8 /16'dan farklı olduğunda veya geçerli bir protokol tarafından hiçbir kodlama belirtilmediğinde bu bildirim zorunludur. Aşağıdaki bir XHTML belgesi örneği, XML bildirimlerini tanımlar

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Uyumlu bir kullanıcı aracısının aşağıdaki kuralları karşılaması gerekir:

* XHTML belgesinin ayrıştırılması ve değerlendirilmesi, XML 1.0 Önerisi ile tutarlılığını sağlayan bir kullanıcı aracısı tarafından yapılır.
* Kullanıcı aracısının doğrulanması durumunda, XML'e göre başvurulan DTD'leri için belgelerin geçerliliğini kontrol etmelidir. XHTML dosyası, kullanıcı aracısı tarafından jenerik XML olarak işlendiğinde, tip kimliğinin özellikleri parça tanımlayıcıları olarak kabul edilecektir.

Bir kullanıcı aracısı tanınmayan bir öğeye çarparsa, yerine getirmesi gereken zorunlu kriterler şunlardır:

* o bilinmeyen öğenin içeriğini işle
* özniteliği ve değerini göz ardı edin
* Varsayılan olarak sağlanan özniteliğin değerini kullanın.

Kullanıcı aracısı, daha önce işlenmemiş bir varlık referans bildirimi ile karşılaştığında, karakterler olarak ("&" işaretiyle başlayıp noktalı virgülle biten) işlenmelidir. İçerik işleme sırasında, kullanıcı aracısı tarafından tahmin edilebilen ancak işlenemeyen karakterler veya karakter varlığı referansları, benzer anlamı veren herhangi bir alternatif işlemeyi kullanabilir. Böyle bir durumda belge, kullanıcıya render işleminin normal olmadığını açıkça gösterecek şekilde gösterilmelidir. Boşlukları işlemek için, kullanıcı aracısının CSS karakterlerinden [CSS2] tanıma bakması gerekir.

## XHTML Geriye dönük uyumluluk

XHTML 1. belgelerinin geriye dönük uyumluluğu, uygun kurallara uyulması halinde HTML 4 kullanıcı aracıları ile iyi bir şekilde bilgilendirilir. XHTML 1.1, genellikle HTML 4 tarayıcıları tarafından göz ardı edilmelerine rağmen, yakut ek açıklamaları dışında tamamen uyumludur. XHTML 2.0 nispeten daha az uyumludur, yine de sorun bir dereceye kadar komut dosyası kullanımıyla ele alınmıştır.

## Referanslar

* [XHTML Tarihi: 1990'lardan Günümüze](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

