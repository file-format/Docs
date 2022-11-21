{
  "date" : "2020-08-20",
  "keywords" :[ "fnt dosyası", "fnt dosya biçimi", "fnt dosyası nedir", "dosya", "fnt örneği", "fnt dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows Yazı Tipi Dosyası",
  "description":"FNT dosya formatı ve FNT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## .fnt dosyası nedir?

.fnt uzantılı bir dosya, Windows İşletim sistemlerinde genel yazı tipi bilgilerini depolayan bir yazı tipi dosyasıdır. FNT dosyalarının yerini çoğunlukla TrueType (.TTF) ve OpenType (.OTF) dosya formatları almıştır ve şu an itibariyle kullanılmayan bir yazı tipi dosyası formatıdır. Bu dosyalar, tek bir puanlayıcı veya vektör yazı tipini saklayabilir. Tüm aygıt sürücüleri, Windows 2.x yazı tiplerini destekler. Ancak, tüm aygıt sürücüleri
Windows 3.0 sürümünü destekler.

## FNT Dosya Biçimi

FNT dosyaları, tek bir raster veya vektör yazı tipini saklayabilir. Vektör formatları, her berat glifinin küçük bir bitmap kullanılarak tanımlandığı raster ile karşılaştırıldığında GDI tarafından daha sık kullanılır. .fnt'nin .ttf ve .otf ile değiştirilmesinin açık nedeni tarama biçimidir.

### Yazı Tipi Dosya Başlığı
Hem raster hem de vektör yazı tipi dosyalarının başlangıcı ortaktır, ardından her dosya türü için farklı bilgiler gelir. Windows 3.0 için yazı tipi dosyası üst bilgisi aşağıdaki gibi altı yeni alan içerir ve bunlar, Windows'un gelecekteki sürümleriyle uyumluluğu sağlamak için sıfıra ayarlanır.

* d Bayraklar
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfAyrılmış1

Windows 3.0 ve 2.0 başlıkları hakkında ayrıntılı bilgi için [Microsoft KnowledgeBase Arşivini](https://jeffpar.github.io/kbarchive/kb/065/Q65123/) ziyaret edin.

## Referanslar
* [Yazı Tipi Dosya Biçimi](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Windows'ta bir yazı tipi nasıl yüklenir veya kaldırılır](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)

