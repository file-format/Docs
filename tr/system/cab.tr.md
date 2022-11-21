{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "uzantı", "dosya", "biçim", "sistem", "Windows Kabin Dosyası", "Microsoft", "Yükleyici", "Kurulum", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows Kabin Dosyası",
  "description":"CAB dosya formatı ve CAB dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .cab dosyası nedir? ##

.cab uzantılı bir dosya, sistem dosyaları kategorisine ait bir windows kabin dosyasına aittir. [LZX](/tr/compression/lzx/), Quantum ve [ZIP](/tr/compression/zip/) gibi sıkıştırılmış veri algoritmalarını destekleyen Microsoft Windows sürümlerinde arşiv dosyası biçiminde kaydedilen bir dosyadır. ). Dosya, bir kullanıcı veya geliştirici yazılım yükleme verilerini ve dosyalarını içermek ve paylaşmak istediğinde hayati önem taşır. Bu dosyalarda bulunan kayıpsız veri sıkıştırma ve dijital sertifika özellikleri, bu dosyayı bu tür dosyaları depolamak ve paylaşmak için mükemmel kılar. Cihaz Yükleyici, Kurulum API'si ve AdvPak gibi farklı Microsoft yükleyicilerini destekler.

## Kısa Tarih ##

CAB dosyası, Microsoft tarafından geliştirilen bir veri sıkıştırma dosyası türüdür. Başlangıçta "Diamond" olarak adlandırıldı, ancak daha sonra popüler olarak "Cabinet" kelimesinin kısaltması olan CAB dosyası olarak bilinmeye başlandı.

## Teknik Şartname ##

Bir CAB dosyası genellikle en fazla 65535 klasör içerebilir ve bu klasörlerin her biri en fazla 65536 dosya içerebilir. CAB dosya depolama mekanizması, her dosyayı ayrı ayrı sıkıştırmak ve depolamak yerine her klasörü sıkıştırılmış bir blok olarak kaydettiği için zamandan ve yerden tasarruf sağlar. Boş klasörler, CAB arşiv klasörlerinde saklanamaz. CAB dosyası ilk olarak Microsoft tarafından geliştirilmiştir ve InstallShield gibi çeşitli yükleyicilerde biraz farklı bir biçimde kullanılır. CAB dosyaları genellikle kendi kendine açılan programlara bağlanır. Microsoft CAB dosyaları, biçimi tanımlamaya yardımcı olan benzersiz işaretleri sayesinde kolayca tanınabilir. Tüm Microsoft CAB dosyaları için benzersiz işaret, MSCF adlı dört kelimelik bir önektir. Bu kodu gören bir kullanıcı, bir Microsoft CAB dosyasını diğer dosyalardan kolayca ayırt edebilir ve buna göre sıkıştırıcılarda veya sürümlerde kullanabilir. Dosyalar, daha fazla yazılım yükleme verisi ile sıkıştırılabilir veya doğru yazılım kullanılarak mevcut verilerin sıkıştırılmış hali açılabilir.


## CAB Örneği ##

Aşağıdaki örnek, bir CAB dosya yapısındaki dosyalar ve klasörler arasındaki ilişkiyi göstermektedir:

{{< figure src="../cab.png" alt="CAB Dosya Biçimi" >}}

## Referans ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
