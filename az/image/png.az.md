{
  "date": "2019-10-11",
  "keywords": [
"png faylı",
"png fayl formatı",
"png faylı nədir",
"fayl",
"png nümunəsi",
"png fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PNG Fayl Format - Raster Şəkil Faylı",
  "description": "PNG faylları yarada və aça bilən PNG fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "PNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pn-azg"
}
},
  "lastmod": "2019-09-10"
}

## PNG faylı nədir?

**PNG** (Portable Network Graphics) faylı itkisiz sıxılmadan istifadə edən rastr şəkil fayl formatıdır. Bu fayl formatı Qrafik Mübadilə Formatının ([GIF](/image/gif/)) əvəzlənməsi kimi yaradılmışdır və heç bir müəllif hüququ məhdudiyyəti yoxdur. Bununla belə, PNG fayl formatı animasiyaları dəstəkləmir. PNG fayl formatı itkisiz şəkil sıxılmasını dəstəkləyir və bu onu istifadəçiləri arasında populyar edir. Zaman keçdikcə PNG geniş istifadə olunan şəkil fayl formatlarından biri kimi inkişaf etmişdir.

## PNG Fayl Formatının Qısa Tarixi

The main reason behind the creation of PNG file format was the patented compression algorithm, Lempel-Ziv-Welch, used in the GIF file format. This along with other GIF limitations created a need for replacement of [**GIF**](/image/gif/) file format. The first proposal and name for PNG file format came in January 1995. PNG fayl formatları ilə bağlı əsas hadisələr aşağıda verilmişdir:

* Oktyabr 1996: PNG spesifikasiyalar Versiya 1.0 buraxıldı və daha sonra [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083 kimi çıxdı. Eyni şey 1996-cı ilin oktyabrında W3C Tövsiyəsi oldu.

* Dekabr 1998: Versiya 1.1, bəzi kiçik dəyişikliklər və üç yeni hissənin əlavə edilməsi ilə buraxıldı.

* Avqust 1999: Əlavə bir parça əlavə edən 1.2 versiyası buraxıldı.

* Noyabr 2003: PNG Beynəlxalq Standart oldu (ISO/IEC 15948:2003). PNG-nin bu versiyası 1.2 versiyasından bir qədər fərqlənir və heç bir yeni parça əlavə etmir.

* Mart 2004: ISO/IEC 15948:2004


## GIF və PNG-nin funksional müqayisəsi

PNG fayl formatı sadə və daşına bilən, qanuni olaraq yüksüz, dəyişdirilə bilən, çevik və möhkəm olmaq üçün nəzərdə tutulmuşdur. Aşağıdakı cədvəldə yeni xüsusiyyətlərə əlavə olaraq PNG fayl formatı tərəfindən miras qalan GIF xüsusiyyətləri sadalanır.

|Xüsusiyyət|GIF|PNG|
---|---|---|
|256 rəngə qədər indeks rəngli şəkillər|Bəli|Bəli|
|Axınma üçün dəstək|Bəli|Bəli|
|Şəffaflıq|Bəli|Bəli|
|Əlavə məlumat|Bəli|Bəli|
|Təchizat və Platformanın Müstəqilliyi|Bəli|Bəli|
|Effektiv|Bəli|Bəli|
|Hər piksel üçün 48 bitə qədər Truecolor şəkilləri|Xeyr|Bəli|
|Hər piksel üçün 16 bitə qədər boz tonlu şəkillər|Xeyr|Bəli|
|Tam alfa kanalı (ümumi şəffaflıq maskaları)|Xeyr|Bəli|
|Şəkil qamma məlumatı|Xeyr|Bəli|
|Etibarlılıq|Xeyr|Bəli|
|Daha sürətli ilkin təqdimat|Xeyr|Bəli|

## PNG fayl strukturu

Demək olar ki, bütün Əməliyyat Sistemləri PNG faylları açmaq üçün dəstək var. Məsələn, Microsoft Windows görüntüləyicisi PNG fayllarını açmaq imkanına malikdir, çünki OS standart olaraq quraşdırmanın bir hissəsi kimi dəstəklənir. PNG faylı PNG `imzasından` və ardınca bir sıra //parçalardan// ibarətdir.

### PNG fayl başlığı

PNG faylının ilk səkkiz baytı həmişə aşağıdakı (ondalıq) dəyərləri ehtiva edir:

{{{137 80 78 71 13 10 26 10 }}}

Bu imza onu göstərir ki, faylın qalan hissəsi IHDR yığını ilə başlayan və IEND yığını ilə bitən bir sıra parçalardan ibarət tək PNG şəklini ehtiva edir.

### Parçalar ###

Hər bir parça dörd hissədən ibarətdir:

**Uzunluq:** Parçanın məlumat sahəsində baytların sayını verən 4 baytlıq işarəsiz tam ədəd. Uzunluq yalnız məlumat sahəsini hesablayır, özünü, yığın növü kodunu və ya CRC-ni deyil. Sıfır etibarlı uzunluqdur. Kodlayıcılar və dekoderlər uzunluğa işarəsiz kimi baxmalı olsalar da, onun dəyəri 231 baytdan çox olmamalıdır.

**Chunk Type:** A 4-byte chunk type code. For convenience in description and in examining PNG files, type codes are restricted to consist of uppercase and lowercase ASCII letters (A-Z and a-z, or 65-90 and 97-122 decimal). However, encoders and decoders must treat the codes as fixed binary values, not character strings. For example, it would not be correct to represent the type code IDAT by the EBCDIC equivalents of those letters. Additional naming conventions for chunk types are discussed in the next section.

**Böyük Məlumat:** Əgər varsa, yığın növünə uyğun olan məlumat baytları. Bu sahə sıfır uzunluqda ola bilər.

**CRC:** 4 baytlıq CRC (Cyclic Redundancy Check). CRC həmişə, hətta heç bir məlumatı olmayan parçalar üçün də mövcuddur.

Parça məlumatının uzunluğu maksimuma qədər istənilən bayt sayı ola bilər; buna görə də, icraçılar parçaların baytdan daha böyük hər hansı sərhədlərdə düzüldüyünü güman edə bilməzlər.

Parçalar hər bir parça növünə qoyulan məhdudiyyətlərə uyğun olaraq istənilən qaydada görünə bilər. (Bir diqqətəlayiq məhdudiyyət ondan ibarətdir ki, IHDR əvvəlcə, IEND isə sonuncu görünməlidir; beləliklə, IEND yığını faylın sonu markeri kimi xidmət edir.) Eyni tipdə bir neçə parça görünə bilər, ancaq bu tip üçün xüsusi olaraq icazə verildiyi təqdirdə.

#### Parça növləri

Parça Növləri Parça Tipinə təyin edilmiş 4 baytlıq böyük hərflərə həssas ASCII dəyərinə əsasən **Kritik** və **Köməkçi** hissələrə təsnif edilir. Bütün tətbiqlər standart kritik parçaları başa düşməli və uğurla təqdim etməlidir. Etibarlı PNG təsvirində IHDR yığını, bir və ya daha çox IDAT parçası və IEND yığını olmalıdır.

### Sıxılma

PNG sıxılma metodu 0 (hazırda PNG üçün müəyyən edilmiş yeganə sıxılma üsulu) ən çox 32768 baytlıq sürüşmə pəncərəsi ilə söndürmə/şişirmə sıxılmasını təyin edir. Deflate sıxılma zip, gzip, pkzip və əlaqəli proqramlarda istifadə olunan LZ77 törəməsidir. Onun patentsiz statusunu dəstəkləyən geniş araşdırmalar aparılmışdır. Zlib məlumat axınındakı sıxılmış məlumatlar hər biri xam (sıxılmamış) məlumatları, sabit Huffman kodları ilə kodlanmış LZ77-sıxılmış məlumatları və ya xüsusi Huffman kodları ilə kodlanmış LZ77-sıxılmış məlumatları təmsil edə bilən bir sıra bloklar kimi saxlanılır. Son blokdakı marker biti onu sonuncu blok kimi müəyyən edir və dekoderə sıxılmış məlumat axınının sonunu tanımağa imkan verir.

#### Sıxılmadan əvvəl filtrləmə

Şəkil məlumatlarını optimal sıxılma üçün hazırlamaq üçün əvvəlcədən sıxılma filtrləri tətbiq olunur. PNG filtr üsulu beş əsas filtr növünü aşağıdakı kimi müəyyən edir:

|Filtr növü|Ad|Proqnozlaşdırılan dəyər|
---|---|---|
|0|Heç biri|Skan xətti dəyişdirilmədən ötürülür|
|1|Alt|Hər bayt və əvvəlki pikselin müvafiq baytının dəyəri arasındakı fərqi ötürür.|
|2|Yuxarı|Yuxarı() filtri eynilə Sub() filtrinə bənzəyir, istisna olmaqla, cari pikselin solunda deyil, dərhal yuxarıda olan piksel proqnozlaşdırıcı kimi istifadə olunur.|
|3|Orta|Average() filtri pikselin dəyərini proqnozlaşdırmaq üçün iki qonşu pikselin (solda və yuxarıda) ortalamasından istifadə edir.|
|4|Paeth|Paeth() filtri üç qonşu pikselin (sol, yuxarı, sol yuxarı) sadə xətti funksiyasını hesablayır, sonra proqnozlaşdırıcı olaraq hesablanmış dəyərə ən yaxın qonşu pikseli seçir.|

Filtrləmə alqoritmləri təsvirin bit dərinliyindən və ya rəng növündən asılı olmayaraq, piksellərə deyil, baytlara” tətbiq edilir. Filtrləmə alqoritmləri skan xəttinin yaratdığı bayt ardıcıllığı üzərində işləyir. Şəkildə bir alfa kanalı varsa, alfa məlumatları görüntü məlumatları ilə eyni şəkildə süzülür.

Şəkil interlaced olduqda, interlace modelinin hər keçidi filtrləmə məqsədləri üçün müstəqil təsvir kimi qəbul edilir. Filtrlər keçid zamanı faktiki olaraq ötürülən piksellərin yaratdığı bayt ardıcıllığı üzərində işləyir və əvvəlki skan xətti tam təsvirdə bitişik deyil, əvvəllər eyni keçiddə ötürüləndir. Qeyd edək ki, hər hansı bir keçiddə ötürülən alt təsvir həmişə düzbucaqlıdır, lakin tam təsvirdən daha kiçik eni və/yaxud hündürlüyü var. Bu alt şəkil boş olduqda filtrləmə tətbiq edilmir.

## İstinadlar ##

* [PNG - Əsas Səhifə](http://www.libpng.org/pub/png/)


