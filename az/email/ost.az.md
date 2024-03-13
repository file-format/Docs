{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OST - Outlook saxlama fayl formatı",
  "description": "OST faylları yarada və aça bilən OST fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "OST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-os-azt"
}
},
  "lastmod": "2019-09-10"
}

## OST faylı nədir?

OST və ya Offline Storage Files Microsoft Outlook istifadə edərək Exchange Server ilə qeydiyyatdan keçdikdən sonra yerli maşında oflayn rejimdə istifadəçinin poçt qutusu məlumatlarını təmsil edir. O, serverə qoşulduqda Microsoft Outlook-un ilk istifadəsində avtomatik olaraq yaradılır. Fayl yaradıldıqdan sonra məlumatlar e-poçt serveri ilə sinxronlaşdırılır ki, o, həm də e-poçt serverindən əlaqə kəsildikdə oflayn rejimdə əlçatan olsun. OST faylları e-poçtlar, kontaktlar, təqvim məlumatları, qeydlər, tapşırıqlar və digər oxşar məlumatlar kimi poçt qutusu elementlərini istifadə edə bilər. İstifadəçilər hətta serverə qoşulma olmadıqda belə OST faylında e-poçt və digər məlumat elementləri yarada bilərlər, lakin bunlar serverlə sinxronlaşdırılmayacaq. Bağlantı qurulduqdan sonra yerli fayl yenidən serverlə sinxronlaşdırılır ki, həm server, həm də yerli surət eyni informasiya səviyyəsində olsun.

## OST fayl formatı

The OST (Offline Storage Table) and [PST](/email/pst/) (Personal Storage Table) file format consist of the Personal Folder File (PFF) format that corresponds to storing user's emails, contacts and appointments. Data in a PFF file is stored in little-endian with all dates and times represented as FILETIME in UTC. [MS-PST] defines two types of PFF:

* 32-bit ANSI Format

* 64-bit Unicode Format


Microsoft-dan əldə olunduğu kimi PST Fayl formatı [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), Açıq Spesifikasiya Promise vasitəsilə pulsuz və geri alınmaz patent lisenziyası kimi OST fayl formatına da tətbiq edilə bilər. O, aşağıdakı fərqləndirici elementlərdən ibarətdir:

* Başlıqdan qaçın

* Fayl başlığı məlumatları

* İndeks filial qovşağı

* İndeks yarpaq qovşağı

* (Fayl) ofset indeksi

* (Element) deskriptor indeksi

* Yerli deskriptorlar

* Maddə masa növü


### Başlıq Məlumatı

OST faylının HEADER strukturu faylın ən əvvəlində 0 ofsetdə yerləşir. O, yuxarıda təsvir edilən NDB Layer məlumat strukturlarına daxil olmaq üçün OST faylı və ROOT məlumatı haqqında metadata məlumatını ehtiva edir. HEADER strukturu OST Fayl Formatının Unicode və ANSI versiyaları üçün fərqlənir.

Başlıq baytlarla təmsil olunan 4 baytlıq sehrli söz **!BDN** ilə başlayır (0x21, 0x42, 0x44, 0x4E). Digər 2 baytlıq sehrli nömrə, **SM** (0x53, 0x4D), faylın başlanğıcından 8 ofsetində yerləşir. Versiya məlumatı (ANSI və ya Unicode) faylın başlanğıcından 10 ofsetdədir. Hex dəyəri (0x17) Unicode OST faylını təyin edir, 0x0E və ya 0x0F isə ANSI fayl formatını təmsil edir.

|Sahə|Təsvir
---|---|
|dwMagic (4 bayt)| { 0x21, 0x42, 0x44, 0x4E } (!BDN) OLMALIDIR
|dwCRCPartial (4 bayt)|wMagicClient-dən (0ffset 0x0008) başlayan 471 bayt məlumatın 32 bitlik CRC dəyəri
|wMagicClient (2 bayt)| { 0x53, 0x4D } olmalıdır.
|wVer (2 bayt)|Fayl formatı versiyası. Fayl ANSI PST faylıdırsa, bu dəyər 14 və ya 15, fayl Unicode PST faylıdırsa, 23 olmalıdır.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. Bu sənədə əsaslanan yeni PST faylının yaradıcıları bu dəyəri 19-a endirməlidirlər.
|bPlatformCreate (1 bayt)|Bu dəyər 0x01 olaraq təyin olunmalıdır.
|bPlatformAccess (1 bayt)|Bu dəyər 0x01 olaraq təyin olunmalıdır.
|dwReserved (8 bayt)|
|bidUnused (yalnız 8 bayt Unicode)|Unicode PST fayl formatı yaradılarkən istifadə olunmamış doldurma əlavə edildi.
|bidNextP (Unicode: 8 bayt; ANSI: 4 bayt)|Növbəti səhifə BID. Səhifələrdə bidIndex dəyərlərinin bölüşdürülməsi üçün xüsusi sayğac var. Səhifələr üçün BID-lər üçün bidIndex dəyəri bu sayğacdan ayrılır.
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Ətraflı məlumat üçün 2.2.2.2 bölməsinə baxın.
|dwUnique (4 bayt)|Bu, PST faylının HEADER strukturu dəyişdirildikdə hər dəfə dəyişdirilən monoton artan dəyərdir. Bu dəyərin funksiyası unikal dəyər təmin etmək və hər başlıq modifikasiyasından sonra HEADER CRC-lərin fərqli olmasını təmin etməkdir.
|rgnid[] (128 bayt)|Hər biri 32 mümkün NID_TYPE-dən birinə uyğun gələn 32 NID-dən ibarət sabit massiv (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE_MESSAGE_ASNID)
|qwUnused (8 bayt)|İstifadə olunmayan yer; Sıfıra təyin olunmalıdır. Yalnız Unicode PST fayl formatı.
|kök (Unicode: 72 bayt; ANSI: 40 bayt)|ROOT strukturu (bölmə 2.2.2.5).
|dwAlign (4 bayt)|İstifadə olunmamış düzləşdirmə baytları; Sıfıra təyin olunmalıdır. Yalnız Unicode PST fayl formatı.
|rgbFM (128 bayt)|FMap köhnəlmişdir. Bu artıq istifadə edilmir və 0xFF ilə doldurulmalıdır. Oxucular bu baytların dəyərinə məhəl qoymamalıdırlar.
|rgbFP (128 bayt)|Köhnəlmiş FPMap. Bu artıq istifadə edilmir və 0xFF ilə doldurulmalıdır. Oxucular bu baytların dəyərinə məhəl qoymamalıdırlar.
|bSentinel (1 bayt)| 0x80-ə təyin olunmalıdır.
|bCryptMethod (1 bayt)|PST faylı daxilində verilənlərin necə kodlandığını göstərir. Əvvəlcədən müəyyən edilmiş dəyərlərdən (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC) birinə təyin edilməlidir.
|rgbReserved (2 bayt)| Qorunur; Sıfıra təyin olunmalıdır.
|bidNextB (8 bayt)|Növbəti mövcud BID dəyərini göstərir. Yalnız Unicode PST fayl formatı.
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Ətraflı məlumat üçün 2.2.2.2 bölməsinə baxın.
|dwCRCFull (4 bayt)|wMagicClient-dən bidNextB-ə qədər daxil olmaqla, 516 bayt məlumatın 32-bit CRC dəyəri. Yalnız Unicode PST fayl formatı.
|ullReserved (8 bayt)|Zorunludur; Sıfıra təyin olunmalıdır. Yalnız ANSI PST fayl formatı.
|dwReserved (4 bayt)|Reserved; Sıfıra təyin olunmalıdır. Yalnız ANSI PST fayl formatı.
|rgbReserved2 (3 bayt)|
|bReserved (1 bayt) |
|rgbReserved3 (32 bayt) |

## İstinadlar

* [Outlook Personal Folders (.ost) Fayl Format](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Şəxsi Qovluq Fayl Formatının Xüsusiyyətləri](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)
