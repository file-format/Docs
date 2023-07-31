{
  "date" : "2020-01-11",
  "keywords" :[ "x dosyası", "x dosya biçimi", "x dosyası nedir", "dosya", "x örneği", "x dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - DirectX 2.0 Dosya Biçimi",
  "description":"DirectX X dosya formatı ve DirectX X dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## X dosyası nedir?

.x uzantılı bir dosya, Microsoft DirectX 2.0 ile sunulan [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics eski dosya biçimini ifade eder. Oyunlarda 3B grafik oluşturma için kullanıldı ve kafesler, dokular, animasyonlar ve kullanıcı tanımlı nesneler için yapıları belirtir. Autodesk FBX dosya formatı daha modern bir format olarak daha iyi hizmet verdiği için 2014'ten beri kullanımdan kaldırılmıştır. X, şablon odaklıdır ve herhangi bir kullanım bilgisinden muaftır.

DirectX X dosyalarını Microsoft DirectX ve genel metin editörlerini kullanarak açabilirsiniz.

## X Dosya Biçimi

[X dosyası referansı](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file), API öğeleri için kullanılan referans bilgilerini içerir. DirectX .x dosyalarıyla çalışın. Format, diğer uygulamalar tarafından veri şablonları aracılığıyla daha yüksek seviyeli ilkelleri tanımlamak için kullanılan düşük seviyeli veri ilkellerini sağlar. DirectX 6.0, .x dosyalarından okumaya ve dosyalara yazmaya olanak tanıyan arabirimler ve yöntemler sunmuştur. DirectX 3.0, bu dosya biçiminin ikili bir sürümünü tanıttı.

DirectX 9 tarafından tanımlanan [X dosya formatı referansı](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format), .x için referans bilgileri içerir Metin Kodlamalarının yanı sıra Binary'deki dosyalar.

### İkili Kodlama

[İkili format](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding), DirectX X formatını metin formatının belirteçleştirilmiş bir temsili olarak tanımlar. Bu belirteçler, gramer yapısı vermek için bağımsız olabilir veya gerekli verileri sağlayan kayıt taşıyan belirteçler olabilir.

#### Başlık

İkili başlık, aşağıdaki tanımlar kullanılarak okunabilir ve yazılabilir.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Metin kodlaması

DirectX .x dosyaları, dosyanın nasıl kullanıldığına bağlı değildir ve herhangi bir uygulamaya özgü değildir. Bu şablon odaklı yaklaşım, .x dosya biçiminin herhangi bir istemci uygulaması tarafından kullanılmasına izin verir.


#### Başlık

Değişken uzunluklu başlık zorunludur ve veri akışının başında olmalıdır. Başlık aşağıdaki verileri içerir.

|Tür |Alt Tür |Boyut |İçerik |İçerik Anlamı|
---|---|---|---|---|
|Sihirli Sayı (gerekli)| | 4 bayt |xof |
|Sürüm Numarası (gerekli) |Ana Sayı |2 bayt |03 |Ana sürüm 3|
| |Küçük Sayı |2 bayt |02 |Küçük sürüm 2|
|Biçim Türü (gerekli)| |4 bayt |"txt " |Metin Dosyası|
| | | |"kutu"| İkili Dosya|
| | | |"çip"| MSZip Sıkıştırılmış Metin Dosyası|
| | | |"bzip"| MSZip Sıkıştırılmış İkili Dosya|
|Kabartma boyutu (gerekli)| |4 bayt| 0064| 64-bit değişkenler|
| | | |0032 |32-bit yüzer|


## Referanslar

* [X Dosyaları Eski](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [DirectX 9 Dosya Biçimi Referansı](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

