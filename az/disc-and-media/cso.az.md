{
  "date": "2021-08-09",
  "keywords": [
"cso faylı",
"cso fayl formatı",
"cso faylı nədir",
"fayl",
"cso misal",
"cso fayl uzantısı",
"uzadılması",
"format",
"iso",
"DAX sıxılması"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "CSO fayl formatı və CSO fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "CSO - Sıxılmış ISO Disk Şəkli",
  "linktitle": "CSO",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cs-azo"
}
},
  "lastmod": "2021-08-09"
}

## CSO faylı nədir?

.cso uzantısı olan fayl sıxılmış ISO təsvir faylıdır. CSO DAX sıxılma metoduna alternativdir; CISO kimi də tanınır; [ISO](/compression/iso/) fayllarını sıxışdırmaq üçün ilk üsul idi və adətən PlayStation Portable materiallarının arxivləşdirilməsi üçün üstünlük verilən üsuldur. Bu format doqquz sıxılma qatını əhatə edə bilən Deflate sıxılmadan istifadə edir. Şəkilləri yaratmaq üçün Prometheus və YACC kimi proqramlardan istifadə olunur.

## CSO fayl formatı

CSO fayl formatı daha çox yaddaş sahəsinə qənaət etmək üçün ISO üçün ilk sıxılma üsulu idi. Daha yaxşı sıxılma üçün təkmilləşdirmələr vaxtaşırı edildi. CSO doqquz səviyyəli əvvəlcədən təyin edilmiş Deflate sıxılmadan istifadə edir, adətən, hər səviyyə 2 KiB bloku ayrı-ayrılıqda idarə edə bilər. Ən yüksək sıxılma səviyyələri disk axınından çox asılı olan proqram təminatının yükləmə müddətlərini yavaşlatsa da, aşağı səviyyələr də əhəmiyyətli sıxılma həyata keçirə bilər.

### CSO fayl strukturu

CSO fayl formatında 24 baytlıq başlıq, məlumat blokları və indeks cədvəli var. Little-endian baytdan böyük sahələr üçün qəbul edilir. PlayStation Portable-ın arxitekturası aşağıda verilmişdir.

#### Başlıq

| Ofset (bayt) | Adı | Ölçü (bayt) | Məqsəd |
----------|----------|--------------|---------|
| 0x0 | Sehrli | 4 | Həmişə CISO və ya 32 bitlik tam ədəd kimi oxunduqda 0x4F534943. Bu sahə CSO faylını müəyyən etmək üçün istifadə olunur. Qeyd edək ki, bu sahə CSO-nun digər törəmələri üçün fərqli ola bilər, məsələn, ZSO ZISO sehrli kodundan istifadə etmişdir. |
| 0x4 | Başlıq ölçüsü | 4 | Orijinal CSO v1 fayl formatı üçün bu sahə nəzərə alınmır və buna görə də dəqiq olması tələb olunmur. Bununla belə, v2 və ZSO formatı bu sahənin həmişə 0x18 (24 bayt) olmasını tələb edir. |
| 0x8 | Sıxılmamış ölçü | 8 | Baytlarda orijinal sıxılmamış ISO ölçüsü. |
| 0x10 | Blok ölçüsü | 4 | Sıxılmadan əvvəl hər bir məlumat blokunun baytla ölçüsü. Adətən 2048 bayt, hər bir ISO 9660 sektorunun ölçüsü ilə eynidir. |
| 0x14 | Version | 1 | The version of the file format in use. For the "v1" format, the value can be either 0 or 1. v2 formatı üçün bu, 2 olmalıdır. Əlavə olaraq, ZSO formatı bunun 1 olmasını tələb edir. |
| 0x15 | İndeksin uyğunlaşdırılması | 1 | Bitlərlə göstərilən hər bir indeks girişinin uyğunlaşdırılması. |
| 0x16 | Qorunur | 2 | Bu sahə istifadə olunmur. v1 formatında bu sahə nəzərə alınmır və ixtiyari dəyərlərdən ibarət ola bilər. v2 formatında bu sahə sıfır olmalıdır. |

#### İndeks cədvəli

İndeks cədvəlində hər bir məlumat blokunun mövqeyini göstərən bir neçə 4 baytlıq giriş və faylın sonuna işarə edən əlavə, sonuncu qeyd var.
Hər bir girişin məzmunu aşağıdakı kimidir:
| Bit | Uzunluq | Maska | Adı | Məqsəd |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Vəzifə | Bu sahə, başlıqda verilmiş indeks düzülüşü ilə sola sürüşdürüldükdə, məlumat blokunun başladığı mövqeyi verir. |
| 31 | 1 | 0x80000000 | Sıxılma növü | ZSO formatı oxşar semantikaya malikdir, yalnız 0 Deflate əvəzinə LZ4-ü təmsil edir. v2 formatında. Blok ölçüsü faylın başlığında göstərilən blok ölçüsünə bərabər və ya ondan böyükdürsə, blok dolayısı ilə sıxılmamış hesab olunur. |

#### Məlumat blokları

Məlumat blokları sıxılmamış və ya sıxılmış verilənlərdən ibarətdir. Blokun ölçüsü onun mövqeyini əldə etməklə və sonra onu növbəti blokun mövqeyindən çıxarmaqla hesablanır. İndeksin uyğunlaşdırılması sıfırdan böyükdürsə, çox güman ki, blok ölçüsü onun saxladığı məlumatdan daha böyükdür.


## İstinadlar 

* N/A


