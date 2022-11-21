{
  "date" : "2020-08-20",
  "keywords" :[ "fon dosyası", "fon dosya biçimi", "fon dosyası nedir", "dosya", "fon örneği", "fon dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Yazı Tipi Kitaplığı Dosyası",
  "description":"FON dosya formatı ve FON dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## .fon dosyası nedir?

.fon uzantılı bir dosya, aslında yürütülebilir bir dosya olan ancak .fon olarak yeniden adlandırılan bir Microsoft Windows 3.x yazı tipi kitaplığıdır. Kendi içinde [.fnt](/tr/font/fnt/) dosyalarından oluşan bir koleksiyondur ve uygulamalar, sistem yazı tipine erişirken ona başvurur. Bu nedenle bir kaynak dosyası görevi görür. Microsoft Windows Yazı Tipi Görünümü uygulaması kullanılarak Windows işletim sisteminde açılabilir.

## FON Dosya Biçimi

Bir FON dosyası yazı tipi kaynakları içerir ve Kaynak (.res) dosya biçimine sahiptir. .res dosya formatı, dosya başlığını ve veri bölümü özelliklerini belirtir. .fnt ayrıca bir kaynak dosyasına dahil olan bir kaynak veri dosyasıdır. FON dosyaları ikili dosya formatına ve application/octet-stream MIME tipine sahiptir.

Yazı tipi kaynakları, diğer kaynak türlerinin aksine, bir uygulamanın kaynaklarına eklenmez. Bunun yerine EXE dosyalarına eklenirler ve .fon dosyaları olarak yeniden adlandırılırlar, bu da uygulamalar yerine kitaplık dosyalarıyla sonuçlanır. Birden Çok Bireysel yazı tipi, her grubun bir kaynak grubu yapısını takip ettiği bir yazı tipi grubunun bileşenlerini oluşturur. Yazı tipi kaynakları, bu kaynak grubu yapılarını kullanır. Grup başlığı, gruptan belirli bir yazı tipine erişmek için gereken tüm bilgileri içerir. Bir yazı tipi bileşen kaynağı aşağıdaki biçime sahiptir.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/tr/font/fnt/) file)
```
Tek bir .rc kaynak dosyası, karışık kaynak bildirimlerine sahip olabilir. Yazı tipi grupları, kaynak dosyasında herhangi bir yerde olabilir ve bitişik olmaları gerekmez. FONTDIR'in manuel girişini eklemek, .RES dosyaları oluşturan programların olmazsa olmazıdır. Grup başlığının yapısı aşağıdadır.

```
[Normal kaynak başlığı (tür = 7)]

WORD Yazı Tipi Sayısı; // .RES dosyasındaki toplam sayı
```     
The remaining data is repeated for every font in the .RES file.

```
WORD yazıtipi Sıralı;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfTelif hakkı[60];
KELİME dfType;
KELİME dfPuanları;
KELİME dfVertRes;
KELİME dfHorizRes;
KELİME dfAscent;
WORD dfDahiliYönlendirme;
WORD dfExternalLeading;
BYTE dfItalik;
BAYT dfAlt Çizgi;
BAYT dfStrikeOut;
KELİME dfAğırlık;
BAYT dfCharSet;
KELİME dfPixWidth;
KELİME dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfOrtGenişlik;
KELİME dfMaxWidth;
BAYT dfFirstChar;
BAYT dfLastChar;
BAYT dfDefaultChar;
BAYT dfBreakChar;
KELİME dfWidthBytes;
DWORD dfCihaz;
DWORD dfFace;
DWORD dfReserved;
char szCihazAdı[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

