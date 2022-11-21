{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WHL Dosya Formatı - Python Wheel Paket Dosyası",
  "description":"WHL dosya formatı ve WHL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## .whl dosyası nedir?

Bir WHL (Tekerlek) dosyası, Python'un tekerlek biçiminde kaydedilen bir dağıtım paketi dosyasıdır. Python dağıtımlarının standart formatlı bir kurulumudur ve kurulum için gerekli tüm dosyaları ve meta verileri içerir. WHL dosyası, bu tekerlek dosyası tarafından desteklenen Python sürümleri ve platformları hakkında da bilgi içerir. [MSI](/tr/executable/msi/) kurulum dosyasına benzer şekilde, WHL dosya formatı, kaynak dağıtımı oluşturmadan kurulum paketinin çalıştırılmasına izin veren, kuruluma hazır bir formattır.

## WHL Dosya Biçimi

WHL dosya biçimi, bir paketin yüklenmesi için yükleyiciler tarafından gereken tüm yükleme dosyalarını ve meta verileri içeren bir [ZIP](/tr/compression/zip/) (.zip) arşividir. Bu WHL dosyaları, unzip seçeneği veya WinZIP ve WinRAR gibi standart açma yazılımı uygulamaları kullanılarak çıkarılabilir.

### WHL Dosya Adı Kuralı

Bir WHL dosyası, aşağıdaki kurala göre adlandırılır.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

WHL dosya adının bir örneği aşağıdaki gibidir.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `cryptography` paket adıdır.
* `2.9.2`, kriptografinin paket versiyonudur. Sürüm, 2.9.2, 3.4 veya 3.9.0.a3 gibi PEP 440 uyumlu bir dizedir.
* `cp35`, Python etiketidir ve çarkın talep ettiği Python uygulamasını ve sürümünü belirtir.
* `abi3`, ABI etiketidir. ABI, uygulama ikili arayüzü anlamına gelir.
* `macosx_10_9_x86_64`, oldukça ağız dolusu olan platform etiketidir.

## Referanslar

* [Python Wheels Nedir ve Neden Önemsemelisiniz?](https://realpython.com/python-wheels/)
* [Python Wheel](https://pypi.org/project/wheel/)

