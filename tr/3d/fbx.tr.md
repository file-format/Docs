{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "dosya", "uzantı", "biçim", "3D Dosya Biçimi" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"FBX dosyasının ne olduğunu ve bunları oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "title" :"FBX - FilmBox 3D Dosya Biçimi",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## FBX dosyası nedir?

FBX, FilmBox, orijinal olarak Kaydara tarafından MotionBuilder için geliştirilmiş popüler bir 3D dosya formatıdır. 2006 yılında Autodesk Inc tarafından satın alındı ve şu anda birçok 3B araç tarafından kullanılan ana 3B değişim formatlarından biri. FBX, hem ikili hem de ASCII dosya biçiminde mevcuttur. Biçim, dijital içerik oluşturma uygulamaları arasında birlikte çalışabilirliği sağlamak için oluşturulmuştur. FBX dosya formatından/formatına dönüştürmek için birçok araç mevcuttur.

## FBX Dosya Biçimi - Daha Fazla Bilgi

FBX tescilli bir formattır ve ikili dosya formatıyla ilgili spesifikasyonlar resmi olarak mevcut değildir. Autodesk tarafından FBX dosyasına/dosyasından okuma, yazma ve dönüştürme için bir C++ FBX SDK sağlanır. FBX SDK kullanmayan Blender yazılımında FBX için bir Python içe ve dışa aktarma betiği de mevcuttur.

### Metin Tabanlı Dosya Yapısı

Metin tabanlı dosya yapısı, açıkça adlandırılmış tanımlayıcılarla belgelenmiş bir ağaç yapısıdır. Her düğümün sahip olduğu hiyerarşide düzenlenmiş iç içe geçmiş bir düğüm listesinden oluşur:

* Bir NodeType tanımlayıcısı (sınıf adı)
* Onunla ilişkili bir dizi özellik, demet öğeleri olağan ilkel veri türleridir: ##float, integer, string## vb.
* Aynı formatta (yinelemeli) düğümleri içeren bir liste.

Bunlar mantıksal olarak aşağıdaki gibi temsil edilebilir:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Bazı standart düğümler, her öğenin iç içe geçmiş bir listeden oluştuğu örtülü liste olarak tanımlanır. FBX geometrisine erişmeyi amaçlayan herhangi bir uygulama, bu içerikleri ayrıştırmalı ve faydalı anlamlar çıkarmalıdır. Metin tabanlı bir FBX dosyası örneği aşağıda verilmiştir:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## FBX Dosyalarının İkili Dosya Yapısı

Daha önce belirtildiği gibi, FBX dosya biçimi belirtimleri FBX için herkese açık değildir. Blender Foundation, şirketin sağladığı SDK'yı kullanmadan FBX dosya biçimini uyguladığından, ikili dosya biçimiyle ilgili bazı ayrıntılar [mevcuttur](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) uygulamanın bir parçası olarak.

İkili dosya yapısı aşağıdaki sırayı takip eder:

* Başlık
* Nesne Kaydı
* Altbilgi

### FBX Başlığı

Dosya başlığı bilgisi 27 bayttan oluşur.

* Bayt 0 - 20: Kaydara FBX Binary \x00 (sonunda 2 boşluk bulunan, ardından NULL sonlandırıcı olan dosya büyüsü).
* Bayt 21 - 22: [0x1A, 0x00]## (bilinmiyor ancak gözlemlenen tüm dosyalar bu baytları gösteriyor).
* Bayt 23 - 26: unsigned int, sürüm numarası. Örneğin sürüm 7.3 için 7300.

### Nesne Kaydı ###

Başlığı, boş ad ve boş özellik listesiyle tam bir düğüm kaydı olan bir nesne kaydı izler. Tüm dosya oluşumunu yinelemeli olarak içerir.

### Altbilgi ###

FBX Altbilgi bölümü, içeriği bilinmeyen dosyanın sonunda yer alır.

## Kayıt Biçimleri ##

Bir FBX dosyasındaki kayıtlar şu şekilde kategorize edilir:

* Düğüm Kayıtları
* Emlak Kayıtları

### Düğüm Kayıt Formatı ###

Her Düğüm Kaydı Formatı adlandırılır ve aşağıdaki hafıza düzenine sahiptir.


|Boyut (Bayt)|Tarih Türü|Ad
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|ÖzellikListLen
|1|UInt8|AdLen
|AdUzunluğu|karakter|Ad
|?|?|Özellik[n], burada n = 0:ÖzellikListLen
|İsteğe bağlı| |
|?|?|İç İçe Liste
|13|uint8[]|Sıfır Kayıt

nerede:

* `EndOffset`, dosyanın başlangıcından düğüm kaydının sonuna kadar olan mesafedir (yani, sonraki adımın ilk baytı). Bu, bilinmeyen veya gerekli olmayan kayıtları kolayca atlamak için kullanılabilir.
* 'NumProperties', düğümle ilişkili değer tanımlama grubundaki özelliklerin sayısıdır. Son öğe olarak iç içe geçmiş bir liste, özellik olarak sayılmaz.
* `PropertyListLen` özellik listesinin uzunluğudur. Bu, özelliklerin veri türüne bağlı olarak ##NumProperties## özelliklerini depolamak için gereken boyuttur.
* `NameLen`, nesne adının karakter cinsinden uzunluğudur. Bunun 0 olduğu tek durum, en üst düzey listeler gibi görünüyor.
* `Ad`, nesnenin adıdır. Sıfır sonlandırma yoktur.
* "Property[n]", n'inci özelliktir. Biçim için, Kayıt Biçimi bölüm özelliğine bakın. Özellikler sırayla ve dolgu yapılmadan yazılır.
* `NestedList`, varlığı en sonunda bir NULL kaydıyla gösterilen iç içe geçmiş listedir.

İç içe geçmiş bir liste girişinin varlığı, EndOffset'e ulaşılana kadar kalan bayt olup olmadığı kontrol edilerek belirlenebilir. Eğer öyleyse, bir sonraki nesne kaydı, son özelliğin hemen ardından okunmalıdır. Nesne kaydı daha sonra 13 sıfır baytı takip eder ve bunlar daha sonra EndOffset ile birleşir. NULL girişinin amacı veya gereksinimi bilinmemektedir ve bazı biçim özelliklerine işaret edebilir.

### Özellik Kayıt Formatı ###

Bir özellik Kaydı, Node.js'nin parçası olan özelliklerle ilgili ayrıntıları içerir. Bir özellik kaydı aşağıdaki bellek düzenine sahiptir:


|Boyut (Bayt)|Veri Türü|Ad
--- | --- | ---
|1|karakter|TürKodu
|?|?|Veriler

TypeCode, benzer işlem gerektiren gruplar halinde sıralanan karakter kodlarını temsil eder. TypeCode'lar aşağıdaki tiplerde sınıflandırılabilir ve TypeCode bu tipler arasında yer alan karakter kodlarından biri olabilir.

#### İlkel Türler ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

İlkel skaler tür kaydındaki veriler, tam olarak küçük endian bayt düzeninde değerin ikili temsilidir.

#### Dizi Türleri ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Dizi Türü için Veriler daha karmaşıktır ve aşağıdaki yapıdadır.


|Boyut (Bayt)|Veri Türü|Ad
--- | --- | ---
|4|Uint32|Dizi Uzunluğu
|4|Uint32|Kodlama
|4|Uint32|Sıkıştırılmış Uzunluk
|?|?|İçindekiler

### Özel Tipler ###

Aşağıda Özel Tip Tip Kodları bulunmaktadır.

```
S: String
R: raw binary data
```

Bu TypeCode'ların her ikisi de aşağıdaki gibi temsil edilir:


|Boyut (Bayt)|Veri Türü|Ad
--- | --- | ---
|4|Uin32|Uzunluk
|Uzunluk| |

Dize sıfır sonlu değildir ve \0 karakterleri içerebilir (bu aslında bazı FBX özelliklerinde kullanılır).

## Referanslar ##

* [FBX - Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)
* [FBX İkili Dosya Biçimi Özellikleri](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

