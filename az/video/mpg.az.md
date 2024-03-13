{
  "date": "2021-04-15",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MPG fayl formatı",
  "keywords": [
"MPG",
"fayl",
"uzadılması",
"format",
"video formatı",
"mpg fayl formatı nədir",
"mpg fayl formatı",
"mpg fayl pleyeri",
"mpeg sıxılma",
"video",
"MPEG",
"MPEG-1",
"MPEG-2"
],
  "description": "MPG fayl formatı və MPG fayllarının necə açılacağını yarada və göstərə bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MPG",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mp-azg"
}
},
  "lastmod": "2021-07-26"
}

## MPG fayl formatı nədir? ##

The file with a .mpg extension belongs to the group of file extensions for MPEG-1 or MPEG-2 audio and video compression. MPEG-1 Part 2 video is not easily available, and this extension (MPG file format) typically points to a MPEG program stream which is defined in MPEG-1 and MPEG-2, or an MPEG transport stream which is defined in MPEG-2. .m2ts kimi digər genişləndirmələr də dəqiq konteyneri, bu halda, MPEG-2 TS-ni göstərən mövcuddur, lakin bunun MPEG-1 mediasına az aidiyyatı var. [.mp3](/audio/mp3/) MP3 audio olan fayllar üçün ən çox yayılmış genişlənmədir. MP3 faylı adi səs axınıdır; MP3 fayllarını etiketləməyin ənənəvi yolu media məlumatını saxlayan, lakin **mpg fayl pleyeri** tərəfindən atılan hər bir çərçivənin zibil seqmentlərinə axın məlumatlarının yazılmasıdır. Bu, AAC fayllarını etiketləmək üçün istifadə edilən oxşar texnikadır, lakin bu gün daha az dəstəklənir.

## MPEG sıxılma ##

MPEG adı Hərəkətli Şəkillər Ekspertlər Qrupu deməkdir. MPEG, şəkillərin və səslərin sıxılmasını, həmçinin hər ikisinin sinxronizasiyasını nəzərdə tutan video sıxılma vasitəsidir.
Hal-hazırda bir neçə MPEG standartı mövcuddur.

- MPEG-1 1,5 Mbit/san aralıq məlumat sürəti üçün təklif olunur.
- MPEG-2 ən azı 10 Mbit/san yüksək məlumat sürəti üçün təklif olunur.
- MPEG-3 HDTV-nin sıxılması üçün təklif edildi, lakin lazımsız olduğu aşkar edildi və MPEG-2 ilə birləşdirildi.
- MPEG-4 64 Kbit/s-dən az olan çox aşağı məlumat sürətləri üçün təklif olunur.


## MPG fayl formatının proqram axını ##

Proqram axını rəqəmsal audio, video və s. multipleks üçün konteynerdir. Proqram axını formatı MPEG-1-in 1-ci hissəsində (ISO/IEC 11172-1) və MPEG-2, Sistemlərin 1-ci hissəsində (ISO/IEC standart 13818-1/ITU-T H.222.0) müəyyən edilmişdir. MPEG-2 Proqram Axını analoq əsaslıdır və ISO/IEC 11172 Sistemləri səviyyəsinə bənzəyir və irəli uyğun gəlir.

### Kodlaşdırma təfərrüatları ###

Qismən MPEG-2 Proqram Axını paketi başlıq formatının kodlaşdırma təfərrüatları buradadır:

| Adı | Bitlərin sayı | Təsvir |
---|---|---|
| sinxronizasiya baytları | 32 | 0x000001BA |
| marker bitləri | 2 | MPEG-2 versiyası üçün 01b. MPEG-1 versiyası üçün marker bitləri 0010b dəyəri olan 4 bitdir. |
| Sistem saatı [32..30] | 3 | Sistem Saatı Referansı (SCR) bitləri 32 - 30 |
| marker bit | 1 | 1 Bit həmişə təyin olunur. |
| Sistem saatı [29..15] | 15 | Sistem saatının bitləri 29 - 15 |
| marker bit | 1 | 1 Bit həmişə təyin olunur. |
| Sistem saatı [14..0] | 15 | Sistem saatı bitləri 14 - 0 |
| marker bit | 1 | 1 Bit həmişə təyin olunur. |
| SCR uzadılması | 9 | |
| marker bit | 1 | 1 Bit həmişə təyin olunur. |
| bit dərəcəsi | 22 | Saniyədə 50 bayt vahidlərdə. |
| marker bitləri | 2 | 11 bit həmişə təyin olunur. |
| qorunur | 5 | gələcək istifadə üçün qorunur |
| içlik uzunluğu | 3 | |
| baytların doldurulması | 8*doldurma uzunluğu | |
| sistem başlığı (isteğe bağlı) | 0 və ya daha çox | sistem başlığının başlanğıc kodu belədirsə: 0x000001BB |

Aşağıdakı cədvəl qismən sistem başlığı formatını göstərir:

| Adı | Baytların sayı | Təsvir |
---|---|---|
| sinxronizasiya baytları | 4 | 0x000001BB |
| başlıq uzunluğu | 2 | |
| dərəcəsi bağlı və marker bit | 3 | |
| audio bağlı və bayraqlar | 1 | |
| bayraqlar, marker biti və video bağlı | 1 | |
| Paket sürətinin məhdudlaşdırılması və ehtiyat bayt | 1 | |


## İstinadlar ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



