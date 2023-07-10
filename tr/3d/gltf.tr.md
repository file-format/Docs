{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "dosya", "uzantı", "biçim", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"GLTF dosyaları ve GLTF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"GLTF - GL İletim Dosya Formatı",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## GLTF dosyası nedir?

glTF (GL İletim Biçimi), 3B model bilgilerini JSON biçiminde depolayan bir 3B dosya biçimidir. JSON kullanımı, hem 3B varlıkların boyutunu hem de bu varlıkları paketten çıkarmak ve kullanmak için gereken çalışma zamanı işlemeyi en aza indirir. 3B sahnelerin ve modellerin uygulamalar tarafından verimli bir şekilde iletilmesi ve yüklenmesi için benimsenmiştir. glTF, Khronos Group 3D Formats Working Group tarafından geliştirildi ve yaratıcıları tarafından 3D'nin [JPEG](/tr/image/jpeg/) olarak tanımlandı.

GLTF dosya formatı, yazma iş akışlarını kolaylaştıran ve endüstri genelinde içeriğin birlikte çalışabilir şekilde kullanılmasını sağlayan 3D içerik araçları ve hizmetleri için genişletilebilir, ortak bir yayınlama formatı tanımlar. glTF dosya biçiminin oluşturulmasının ardındaki amaç, yazma iş akışlarını kolaylaştırması ve endüstri genelinde içeriğin birlikte çalışabilir şekilde kullanılmasını sağlaması gereken 3B içerik araçları ve hizmetleri için genişletilebilir, ortak bir yayınlama biçimi tanımlamaktı. WebGL ve diğer API'leri kullanan uygulamalar tarafından çalışma zamanı işlemeyi en aza indirir.

## GLTF Dosyasının Kısa Tarihçesi

glTF dosya formatı 1.0 için ilk spesifikasyonlar Ekim 2015'te açıklandı. Bu, Mart 2012'de Khronos tarafından başlatılan bir dizi çaba olarak geldi. Bu çabaların amacı, WebGL çekişi etrafındaki fırsatları değerlendirmekti. Sonuç olarak, glTF formatının JSON formatına dayalı ilk demosu 2012'deki WebGl buluşmasında sunuldu. Format, zaman zaman Cesium, 3D Tiles, Oculus, Microsoft, Archilogic ve diğerleri dahil olmak üzere birçok şirket tarafından benimsendi.

glTF 2.0, 5 Haziran 2017'de Web3D 2017 Konferansı'nda yayınlandı. Bundan sonra glTF dosya formatını benimseyen uzun bir şirket listesi var.

## GLTF Dosya Biçimi

glTF 2.0 için dosya formatı belirtimleri referans için [çevrimiçi](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) mevcuttur ve okuma/yazma ile ilgili herhangi bir uygulamada destek için danışılmalıdır. glTF dosya biçimi.

glTF, varlıkları harici verileri destekleyen JSON dosyaları olarak tanımlar. 3B modelleri aşağıdakilerin yardımıyla temsil eder:

* Düğüm hiyerarşisi, malzemeler, kameralar ve kafesler, animasyonlar ve diğer yapılar için tanımlayıcı bilgileri içeren JSON biçimli bir .glTF dosyasında yer alan tam sahne açıklaması
* Geometri ve animasyon verilerini ve diğer tampon tabanlı verileri içeren ikili dosyalar (.bin)
* Dokular için görüntü dosyaları ([.jpg](/tr/image/jpeg/), [.png](/tr/image/png/))

Görüntüler gibi herhangi bir harici varlık, URI aracılığıyla başvurulan harici dosyalarda saklanır. Bu URI'ler, GLB kabının yanında depolanır veya veri URI'leri kullanılarak doğrudan JSON'a gömülür. Her geçerli glTF, sürümünü belirtmelidir.

glTF, küçük dosya boyutu, hızlı yükleme, eksiksiz 3B sahne gösterimi ve genişletilebilirlik elde etmek için tasarlanmıştır. Bu benzersiz tasarım hedefleri, glTF dosya biçiminin 3B alanda popüler olmasının ana nedenleridir. Farklı dosya türleri için glTF dosya biçimi tarafından desteklenen mime türleri aşağıdadır:

* .gltf dosyalarında model/gltf+json kullanılır
* .bin dosyaları application/octet-stream kullanır
* Doku dosyaları, belirli görüntü formatına dayalı olarak resmi görüntü/* türünü kullanır. Modern web tarayıcılarıyla uyumluluk için şu görüntü formatları desteklenir: image/jpeg, image/png.

### JSON Kodlaması

glTF, JSON dosya biçiminde aşağıdaki ek kısıtlamaları uygular

İstemci tarafında uygulamayı basitleştirmek için glTF, JSON formatı ve kodlamasında ek kısıtlamalara sahiptir.

1. JSON, BOM olmadan UTF-8 kodlaması kullanmalıdır.
1. Bu spesifikasyonda tanımlanan tüm dizeler (özellik adları, numaralandırmalar) yalnızca ASCII karakter kümesini kullanır ve düz metin olarak yazılmalıdır, örneğin `"\u0062\u0075\u0066\u0066\u0065\u0072"' yerine "buffer".
1. JSON nesneleri içindeki adlar (anahtarlar) benzersiz olmalıdır, yani yinelenen anahtarlara izin verilmez.

### URI'ler

Arabelleklere ve Görüntü kaynaklarına, URI'ler aracılığıyla başvurulur. Aşağıdaki iki URI türü istemciler tarafından desteklenmelidir.

**Veri URI'leri:** Veri URI'leri, RFC 2397 tarafından tanımlandığı gibidir ve glTF tarafından kaynakları JSON'a katıştırmak için kullanılır.

**Göreceli URI Yolları:** veya RFC 3986, [Bölüm 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) tarafından tanımlandığı şekliyle yol şeması — şema, yetki veya parametreler olmadan. Ayrılmış karakterler, RFC 3986 [Bölüm 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2) uyarınca yüzde olarak kodlanmalıdır.

## Referanslar ##

* [glTF 2.0 Teknik Özellikleri - Khronos](https://github.com/KhronosGroup/glTF)
* [glTF Dosya Biçimi - Wikipedia Tarafından](https://en.wikipedia.org/wiki/GlTF)

