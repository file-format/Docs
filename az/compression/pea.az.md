{
  "date": "2021-04-21",
  "keywords": [
"noxud faylı",
"noxud fayl formatı",
"noxud faylı nədir",
"fayl",
"noxud nümunəsi",
"noxud fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEA - PeaZip Arxiv Fayl Formatı",
  "description": "PEA fayl formatı və PEA fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PEA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pe-aza"
}
},
  "lastmod": "2021-04-21"
}

## PEA faylı nədir?

Pack, Encrypt və Authenticate sözlərinin abreviaturası olan .pea uzantısı olan fayl [PeaZip](https://peazip.github.io/) arxivləşdirmə proqramı ilə yaradılmış [zip](/compression/zip/) arxivdir. O, sıxılma və çoxlu həcm çıxışına malikdir və Doğrulanmış Şifrələmə və kriptoqrafiya vasitəsilə çevik təhlükəsizlik modeli təklif edir. Bu, məlumatların həm məxfiliyini, həm də autentifikasiyasını təmin edir. PeaZip yardım proqramı tələblərə uyğun olaraq müxtəlif OS üçün tərtib edilə bilən açıq mənbəli mühərrik kimi mövcuddur.

## PEA fayl formatı

[PEA file format specifications](https://peazip.github.io/pea_help.pdf) tərtibatçının arayışı üçün açıqdır. PEA arxivləri çevik təhlükəsizlik modeli və yoxlama məbləğlərindən kriptoqrafik cəhətdən güclü hashlara qədər lazımsız bütövlük yoxlamaları olan ikili fayllardır. Bu, nəzarət etmək üçün üç fərqli ünsiyyət səviyyəsini müəyyənləşdirir:

 * Axınlar - çoxlu giriş faylları tərəfindən formalaşan və birdən çox çıxış həcminə yazıla bilən faktiki çıxış məlumat axını
 * Obyektlər - .pea arxivinə göndərilən daxiletmə faylları və qovluqları
 * Həcmlər - istifadəçi tərəfindən müəyyən edilmiş ölçüyə yayıla bilən çıxış arxiv faylı

Bunların hər biri isteğe bağlıdır və istifadəçi tələblərinə uyğun olaraq daxil edilə bilər. PEA fayl formatı limitsiz obyektləri ehtiva edən tək axını saxlaya bilər. Hər axın ölçüsü 2^64 bayta qədərdir.

PEA faylları EAX və ya HMAC rejimində AES-dən, alternativ olaraq EAX rejimində Twofish və Serpent-dən istifadə edərək isteğe bağlı bütövlük yoxlanışı və təsdiqlənmiş şifrələmə təklif edir.

### PEA Arxiv Başlığı

Arxiv başlığı 10 baytdır və aşağıdakı kimi qurulmuşdur.

|Bayt|Təsvir|
---|---|
|1 | Fayl formatının aydınlaşdırılması üçün sehrli bayt sahəsi: $EA|
|1 | Versiya nömrəsi|
|1 | Reviziya nömrəsi|
|1 | Həcmə nəzarət sxemi|
|1 | Axının qurulduğu ƏS-nin elan edilməsi|
|1 | OS tarix və vaxt kodlaşdırmasının elan edilməsi|
|1 | Obyektlərin elan edilməsi simvol kodlaşdırması
|1 | CPU növünün elan edilməsi (7 bitdə kodlanmış) və endianness (msb-də)|
|1 | Gələcək istifadə üçün qorunur|

## İstinadlar

* [PEA Fayl Formatının Xüsusiyyətləri](https://peazip.github.io/pea_help.pdf)

* [PEA Fayl Formatı](https://peazip.github.io/pea-file-format.html#.pea_specifications)


