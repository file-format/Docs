{
  "date": "2019-10-11",
  "keywords": [
"3DS",
"fayl",
"format",
"fayl növü",
"uzadılması",
"3DS faylı nədir?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "3DS fayl formatı və 3DS fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "title": "3DS fayl formatı",
  "linktitle": "3DS",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3ds"
}
},
  "lastmod": "2019-09-10"
}

## 3DS faylı nədir?

.3ds genişləndirilməsi olan fayl Autodesk 3D Studio tərəfindən istifadə edilən 3D Sudio (DOS) şəbəkə fayl formatını təmsil edir. Autodesk 3D Studio 1990-cı illərdən 3D fayl formatı bazarındadır və indi 3D modelləşdirmə, animasiya və renderləmə ilə işləmək üçün 3D Studio MAX-a çevrilmişdir. 3DS faylı səhnələrin və şəkillərin 3D təsviri üçün məlumatları ehtiva edir və 3D məlumatların idxalı və ixracı üçün məşhur fayl formatlarından biridir. O, səhnəni göstərmək üçün təpələr və çoxbucaqlılar yaratmaq üçün kamera yerləri, Mesh məlumatları, işıqlandırma məlumatı, görünüş sahəsinin konfiqurasiyaları, hamarlama qrup məlumatları, bitmap istinadları və atributları kimi məlumatları nəzərdən keçirir.

## 3DS Fayl Format - Ətraflı Məlumat
Əsasında 3DS ikili fayl formatıdır və məlumatların saxlanması və əldə edilməsi üçün əvvəlcədən müəyyən edilmiş strukturu izləyir. İkili fayl formatı 3DS fayl formatını mətn əsaslı fayl formatları ilə müqayisədə daha sürətli kiçikləşdirməyə imkan verir. 3DS faylının içindəki məlumatlar parçalar şəklində saxlanılır.

### 3DS yığını

3DS faylındakı hər bir parça ID, növbəti blokun yeri üçün blokun uzunluğu və məlumatların özünü ehtiva edən məlumat blokudur. Parça ID 3DS fayl formatı oxucularına tanımadıqları blokları atlamağa imkan verir. O, həmçinin formatın genişlənməsinə kömək edir. Hər bir parça, birlikdə səhnəni göstərən formalar, işıqlandırma və baxış məlumatları ilə bağlı məlumatları saxlayır. Parçalar 3DS faylında iyerarxik strukturda yerləşdirilir və təqdimatda XML Sənəd Obyekt ağacına bənzəyir.

**Chunk ID:** The first two bytes of a chunk represent a chunk identifier that lets the file reader decide whether to consider it during reading or skip i-azt.

** Parçanın uzunluğu:** Parça ID-sindən sonra parçanın uzunluğunu ifadə edən 4 baytlıq tam ədəd (az-endian ilə) gəlir. Bu uzunluğa verilənlərin uzunluğu, onun alt bloklarının uzunluğu və 6 baytlıq başlıq daxildir.

**Yükləmə:** Parçanın uzunluğundan sonra yığın üçün faktiki məlumat baytları, ardınca isə bir neçə səviyyəyə qədər genişləndirilə bilən eyni iyerarxik strukturda onun alt hissələri gəlir.

### Parçanın strukturu

Sadə bir yığının iyerarxik quruluşu aşağıda göstərildiyi kimidir:

**Bir parça**

|başlanğıc|son|ölçü|ad
--- | --- | --- | ---
|0|1|2|Böyük ID
|2|5|4|Növbəti Parça

Parçaların identifikatoru ilə müəyyən edilmiş bir iyerarxiyası var. 3ds faylının Əsas yığın ID 4D4Dh var. Bu həmişə faylın ilk hissəsidir. Əsas hissələrdə əsas hissələr var.

**Əsas hissələr**

|id|Təsvir
--- | ---
|3D3D|Obyekt mesh məlumatının başlanğıcı.
|B000|Açıq kadr məlumatlarının başlanğıcı.

ID blokundan sonrakı Next Chunk göstəricisi növbəti Əsas hissəyə işarə edir.
Əsas yığından dərhal sonra başqa bir yığın gəlir. Bu, əsas hissələr çərçivəsində icazə verilən hər hansı digər növ yığın ola bilər.
For the Mesh description (3D3D) they could be any multiples of.

**3D3D-nin alt hissələri - Mesh Block**


|id|Təsvir
--- | ---
|1100|naməlum
|1200|Fon Rəngi.
|1201|naməlum
|1300|naməlum
|1400|naməlum
|1420|naməlum
|1450|naməlum
|1500|naməlum
|2100|Ətraf mühitin rəng bloku
|2200|duman?
|2201|duman?
|2210|duman?
|2300|naməlum
|3000|naməlum
|4000|Obyekt Bloku
|7001|naməlum
|AFFF|naməlum

**4000-in alt hissələri - Obyekt təsviri bloku**
Subchunk 4000-in ilk elementi obyekt adının ASCIIZ sətridir.
Yadda saxlayın ki, obyekt mesh, işıq və ya kamera ola bilər.

|id|Təsvir
--- | ---
|4010|naməlum
|4012|kölgə?
|4100|Üçbucaqlı Çoxbucaqlı Obyekt
|4600|İşıq
|4700|Kamera

## İstinadlar

* [Həndəsə Fayl Formatları - Autodesk](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)

* [3DS - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/.3ds)


