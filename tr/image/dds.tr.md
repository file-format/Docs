{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DDS Dosya Biçimi- DirectDraw Yüzey Görüntü Dosyası",
  "description":"DDS dosya formatı ve DDS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## DDS dosyası nedir?

Bir DDS dosyası, DirectDraw Surface (DDS) kap biçimini kullanan bir raster görüntü dosyasıdır. Sıkıştırılmamış ve sıkıştırılmış (DXTn) dokuları depolar ve farklı veri türlerini depolamak için farklı türler uygular. Ayrıca, tek katmanlı dokular, mipmap'li dokular, küp haritalar, hacim haritaları ve doku dizileri gibi birçok farklı veri türünü destekler. Bu, DDS dosyalarının dijital fotoğraflara ve Windows masaüstü arka planlarına ek olarak video oyunu doku birimi modellerini depolamasını sağlar. DDS dosya formatı Microsoft tarafından DirectX SDK ile kullanılmak üzere geliştirilmiştir.

## DDS Dosya Biçimi

DDS dosyaları ikili dosyalar olarak kaydedilir ve DirectX SDK ile kullanılabilir. 3D oyunlar gibi gerçek zamanlı işleme uygulamaları geliştirmek için DirectX'in gücünden yararlanır.

### DDS Dosya Düzeni

[DDS dosya düzeni](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) Microsoft tarafından ayrıntılı olarak belgelenmiştir. Bir ikili DDS dosyası aşağıdaki bilgileri içerir.

* Dört karakterli kod değeri 'DDS' (0x20534444) içeren bir DWORD (sihirli sayı).
* Dosyadaki verilerin açıklaması.

DDS_HEADER, verileri, DDS_PIXELFORMAT ise piksel formatını tanımlar. Bunların her ikisi de kullanımdan kaldırılan DDSURFACEDESC2, DDSCAPS2 ve DDPIXELFORMAT DirectDraw 7 yapılarının yerine geçer.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[DDS dosya biçiminin programlama kılavuzu](https://docs.Microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) bu dosya biçiminin teknik ayrıntılarını daha ayrıntılı olarak açıklar.

## Referanslar

* [DDS - Wikipedia Tarafından](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [ZSoft PCX Dosya Biçimi Teknik Referans Kılavuzu](http://qzx.com/pc-gpe/pcx.txt)

