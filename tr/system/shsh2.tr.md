{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2 Dosyası - iOS SHSH Blob Dosya Formatı",
  "description":"SHSH2 dosyasının ne olduğunu öğrenin.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## SHSH2 dosyası nedir?

SHSH blobu veya ECID SHSH olarak da bilinen SHSH2 dosyası, Apple tarafından iPhone'lar, iPad'ler ve iPod'lar gibi iOS aygıtları için ürün yazılımı güncellemelerinin kimliğini doğrulamak ve doğrulamak için kullanılan dijital bir imzadır. ECID (Exclusive Chip ID) olarak bilinen cihaz için benzersiz bir tanımlayıcı içerir. Ayrıca cihazda yüklü olan donanım yazılımı sürümü hakkında da bilgi içerir.

## SHSH2 Dosya Formatı - Daha Fazla Bilgi

SHSH2 dosyaları diske ikili dosya formatında kaydedilir ve bu dosya formatının dahili dosya yapısı ayrıntıları kamuya açık değildir.

iPhone, iPad veya Mac gibi bir Apple cihazına iOS'un yeni bir sürümü yüklendiğinde bir SHSH2 dosyası oluşturulur. Bu SHSH2 dosyası, bu dijital imza dosyasını okuyan ve doğrulayan Apple sunucularına gönderilir. Sunucu, bu bilgilere dayanarak kuruluma izin verir veya kuruluma izin vermez.

Bir güncelleme istendiğinde de aynı şey olur. Bir kullanıcı, iTunes veya başka bir yazılım aracılığıyla aygıtının güncellenmesini veya geri yüklenmesini istediğinde, Apple'ın sunucuları, güncellemenin devam etmesine izin vermeden önce SHSH2 dosyasının aygıtın ECID ve aygıt yazılımı sürümüyle eşleştiğini kontrol edecektir.

## Referanslar

* [SHSH Blobu - Wikipedia'dan](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Tasarrufu](https://tsssaver.1conan.com/v2/)

