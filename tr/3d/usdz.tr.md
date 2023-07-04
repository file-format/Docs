{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "usdz dosyası", "usdz dosya biçimi", "dosya biçimi", "3d","usdz dosyası indirme"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Evrensel Sahne Açıklama ZIP Formatı",
  "description":"USDZ dosya formatı ve USDZ dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## USDZ dosyası nedir?

.usdz içeren bir dosya, [USD](/tr/3d/usd/) (Evrensel Sahne Tanımı) dosya biçimi için sıkıştırılmamış ve şifrelenmemiş bir ZIP arşividir ve içine gömülü diğer biçimlerdeki (dokular ve animasyonlar gibi) dosyaları ve bunlar için proxy'leri içerir. arşivi açar ve paketi açmaya gerek kalmadan doğrudan USD çalışma zamanı ile çalıştırır. USDZ dosyaları, tasarımı bir paketin yeni Ar-seviyesi soyutlamasına dayanan paketlerdir. Usdz, IANA'ya kayıtlıdır ve medya türü adı modele ve alt tür adı vnd.usd+zip'e sahiptir ve ayrıntıları [IANA kayıt sayfasında](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ Dosya Biçimi

USDZ dosyaları, tek tek dosyaları kapsayıcısında arşivleyen ZIP dosya biçimini temel alır. Bu, alıcının yalnızca içeriği açmasını ve çalışmak ve incelemek için normal USD sahne açıklama dosyalarını kullanmasını sağlar. Neredeyse tüm işletim sistemleri, ZIP dosya biçimleri için yerleşik destek sağlar ve herhangi bir özel yöntem yerine bu arşivleme biçimini seçmek, USDZ dosyalarının basit bir aktarım protokolü olarak kullanışlı olmasını kolaylaştırır.

### ZIP Kısıtlamaları

USDZ dosya biçimi, herhangi bir "sıkıştırma" ve "şifreleme" olmaksızın ZIP dosya biçimini kullanır. Bu, tasarım gereği iki gereksinimi karşılamayı amaçlıyordu:

* Halihazırda belleğe yüklenmiş bir paket veya diskte tek bir dosya olarak, görüntünün içerdiği verilere erişmek için API'ler USD cinsinden mevcuttur.
* Dosyaları diske çıkarmaya veya daha fazla yığın depolama alanı ayırmaya gerek olmamalıdır

USDZ ile, görüntü formatlarının çoğu dahili sıkıştırma şemalarına izin verdiğinden, bu gereksinimlerin her ikisi de karşılanır ve bu da kompakt dosya boyutu sağlar.

### Düzen Gereksinimleri

USDZ paketleri, paket içindeki dosyaların düzenini gerektirir; her dosya için veri, paketin başından itibaren 64 baytın katlarında başlamalıdır. Ancak, paketin basit bir referansla hedeflenmesi durumunda paket yerel bir [USD](/tr/3d/usd/) dosyasıyla başlamalıdır. Böyle bir durumda, bu ilk USD dosyası Varsayılan Katman olarak adlandırılır. "Akış yapılabilir içerik" sunmak isteyen müşteriler, diğer düzen kısıtlamalarını da dikkate almak isteyebilir.

## USDZ dosyası indirme
Usdz dosyaları diğer yüksek kaliteli görüntüler ve usd dosyalarıyla dolu olduğundan, daha fazla disk alanı kaplayabilirler. Burada indirmek için basit ve daha küçük bir USDZ örnek dosyası bulabilirsiniz:

- [Örnek.usdz](../sample.usdz)

## Referanslar

* [USDZ Dosya Biçimi Özellikleri](https://openusd.org/release/spec_usdz.html)
