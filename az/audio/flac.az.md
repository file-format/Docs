---
date: 2019-12-13
keywords: flac, flac file format, .flac extension, flac file, flac vs mp3
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: LFLAC fayl formatı və FLAC faylını yarada və aça bilən API-lər haqqında qazanıns.
title: FLAC fayl formasıat
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## FLAC faylı nədir?

FLAC (Free Lossless Audio Codec) Xiph.Org Fondu tərəfindən hazırlanmış itkisiz sıxılma audio kodlaşdırma formatıdır. FLAC, .flac uzantısı ilə saxlanılan, royaltisiz açıq formatdır. FLAC alqoritmi ilə sıxılmış rəqəmsal audio adətən ölçüsü 50-70 faizə endirilir. FLAC faylları orijinal audio faylların eyni nüsxəsinə açıla bilər.

## FLAC fayl formatı

Bu, FLAC bit axınına ümumi baxışdır.

- **fLaC marker**: Bu marker axının əvvəlinə əlavə edilir. Ondan sonra bir və ya bir neçə metadata bloku gəlir.
- **Metaməlumat Blokları**: FLAC tərəfindən 128 növ metadata bloku dəstəklənir; hazırda aşağıdakılar müəyyən edilir.
  - "**STREAMINFO**: Bütün axın haqqında məlumatı ehtiva edir."
  - "**TƏTBİQ**: Bu, identifikasiya üçün üçüncü tərəf proqramları tərəfindən istifadə olunur."
  - "**PADDING**: Əgər metadata kodlaşdırıldıqdan sonra redaktə ediləcəksə, metadata üçün yer ayırmaq üçün istifadə olunur. Metaməlumat redaktə edildikdə, doldurma faktiki metadata ilə əvəz olunur."
  - "**SEEKTABLE**: Axtarış nöqtələrini saxlamaq üçün əlavə cədvəl."
  - "**VORBIS_COMMENT**: İnsan tərəfindən oxuna bilən açar/dəyər cütlərini saxlamaq üçün istifadə olunur."
  - "**CUESHEET**: İstiqamət vərəqi məlumatlarını saxlamaq üçün istifadə olunur."
  - "**ŞƏKİL**: Şəkilləri saxlamaq üçün istifadə olunur."
- **FRAME**: Audio data bir və ya bir neçə audio çərçivədən ibarətdir.
  - "**FRAME_HEADER**: Axın haqqında əsas məlumatları ehtiva edir."
  - "**ALT ÇƏRÇİVƏ**: Mürəkkəbliyi azaltmaq üçün fərdi alt çərçivələr çərçivə daxilində ayrıca kodlanır (hər kanala bir kadr)."
  - "**FRAME_FOOTER**: Tam çərçivənin CRC-ni ehtiva edir."

## FLAC Fayl Formatının Qısa Tarixi

Josh Coalson began the development of FLAC in 2000. FLAC-ın ilk versiyası 20 iyul 2001-ci ildə buraxıldı. FLAC 20 yanvar 2003-cü ildə Xiph.Org bayrağı altında birləşdi. FLAC-ın inkişafı 26 martda 1.3.0 versiyasının buraxılması ilə Xiph.Org git repozitoriyasına köçürüldü. 2013.

## FLAC Layihəsinin tərkibi

FLAC layihəsi aşağıdakılardan ibarətdir:

- Yayım formatları.
- Axın üçün sadə konteyner formatı (FLAC).
- libFLAC: İstinad kodlayıcıları, dekoderlər və metadata interfeysi kitabxanası.
- libFLAC++: libFLAC üçün obyekt yönümlü sarğı.
- flac: FLAC axınlarını kodlaşdırmaq və deşifrə etmək üçün əmr xətti proqramı.
- metaflac: FLAC üçün komanda xətti metadata redaktoru.
- Winamp, XMMX və s. kimi musiqi pleyerləri üçün giriş plaginləri.
- Ogg konteyner formatı (Ogg FLAC).

## FLAC Dizaynı

Musiqinin sıxlığından və amplitudasından asılı olaraq, sıxılmış faylın ölçüsü orijinal fayldan 80% az ola bilər.

### Mənbə Kodlayıcı ###

- O, yalnız tam nümunələri dəstəkləyir və üzən nöqtə deyil. O, hər nümunə üçün 4-dən 32 bitə qədər PCM bit həllini və 1Hz-dən 65,535 Hz-ə qədər seçmə sürətini idarə edə bilər. FLAC kodlaşdırması hər nümunə üçün 24 bitlə məhdudlaşır.
- Sıxılmanı artırmaq üçün kanallararası korrelyasiyadan faydalanmaq üçün kanallar qruplaşdırıla bilər.
- CRC yoxlama məbləğləri pozulmuş çərçivələri müəyyən etmək üçün istifadə olunur.
- Audio nümunələrinin çevrilməsi üçün FLAC xətti proqnozdan istifadə edir.

### Metadata ###

- FLAC ReplayGain-i dəstəkləyir (səsdə yüksəkliyi qəbul etmək və normallaşdırmaq üçün istifadə olunur).
- FLAC etiketləmə üçün Vorbis şərhlərində istifadə edilən eyni sistemdən istifadə edir.
- libFLAC əksər FLAC proqramları tərəfindən kodlaşdırma/deşifrə üçün istifadə olunur.
- libFLAC API əsas FLAC bit axınından abstraksiyanı artırmaq üçün axınlara, axtarılan axınlara və fayllara təşkil edilmişdir.

### Sıxılma ###

libFLAC 0-dan 8-ə qədər sıxılma səviyyələrindən istifadə edir, burada 0 ən sürətli, 8 isə ən yavaş sıxılma səviyyəsidir. Sıxılmış fayllar həmişə itkisizdir, baxmayaraq ki, sürət və ölçü arasında fərq var.

## FLAC vs MP3
MP3 itkili sıxılma formatıdır, o deməkdir ki, sıxılma tətbiq edildikdən sonra ölçüsünü azaltmaq üçün audionun bir hissəsini kəsə bilər. Halbuki, FLAC itkisiz bir fayl formatıdır, yəni səsi ən təmiz formada eşidə bilərsiniz. Əvvəllər itkisiz fayl formatları CDA və ya WAV idi ki, FLAC kimi çox yer səmərəli deyildi. Aşağıdakı cədvəl bəzi vacib şərtlər üçün bu iki format arasında müqayisəni göstərəcəkdir:

|Müddət|FLAC|MP3|
---|---|---|
|**Məlumat Keyfiyyəti**|Audio məlumat itkisi yoxdur| Audio verilənləri sıxarkən bəzi məlumatlar itirilə bilər|
|**Ölçü**|İtkili formatlarla müqayisədə daha böyük fayl ölçüsü. Beləliklə, daha böyük saxlama qabiliyyətinə ehtiyacınız var| Daha kiçik fayl ölçüsü, az yaddaş sahəsi olan kompakt audio cihazlarında oxutmaq üçün uyğun |
|**Avadanlıq tələbləri**| Yüksək keyfiyyətli audio qurğuya və böyük yaddaş tutumuna ehtiyacınız var |Böyük audio kitabxanaları daha kiçik yaddaşda saxlamaq olar. Audio pleyerlər və ya mobil telefonlar kimi əl cihazları üçün uyğundur|
|**İnternet üzərindən paylama**|Kütləvi fayl ölçüsünə görə internet üzərindən asanlıqla yayıla bilmir |Yığcam fayl ölçüsü internet üzərindən yayılmasını asanlaşdırır|
|**Uyğunluq**|Planetdəki hər bir cihaza demək olar ki, uyğun gələn ən populyar musiqi və audio dinləmə kodekYeni nəsil kompüterlər, telefonlar, AV qəbulediciləri, blu-ray pleyerləri, Roku və ya Fire TV kimi axın cihazları ilə uyğundur|

## İstinadlar ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

