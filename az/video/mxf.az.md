{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MXF - Material mübadiləsi formatı",
  "keywords": [
"MXF",
"matroska video",
"mkv formatı",
"MXF fayllarını necə oynatmaq olar",
"SMPTE",
"multimedia",
"video"
],
  "description": "MXF fayl formatı və MXF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MXF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mx-azf"
}
},
  "lastmod": "2021-03-01"
}

## MXF faylı nədir?

.mxf uzantılı fayl, fayl haqqında metadata məlumatı ilə birlikdə rəqəmsal video və audio medianı ehtiva edən multimedia konteyner formatıdır. O, mühəndislik, texnologiya mütəxəssisləri və media və əyləncə sənayesində çalışan rəhbərlərin qlobal birliyi olan SMPTE (Society of Motion Picture and Television Engineers) standartına uyğundur. MXF faylları [AVI](/video/avi/) və ya [MOV](/video/mov/) kimi digər fayl formatlarına çevrilə bilər.

## MXF fayl formatı

MXF faylları əslində müəyyən formatda bayt ardıcıllığından ibarət olan ikili fayllardır. Deşifrə proqramları onu başa düşmək və ondan məlumat çıxarmaq üçün bu formata uyğun olmalıdır. Format aşağıda təsvir olunan KLV kodlaşdırmasından istifadə edərək geriyə uyğunluğu pozmadan yeni elementlər əlavə etməyə imkan verir.

 * Açar – elementin identifikatoru, SMPTE Universal Label (UL)
 * Uzunluq - bu element üçün tələb olunan yerin miqdarını azaltmaq üçün istifadə olunan dəyişən uzunluqlu kodlaşdırma olan məlumatın uzunluğu
 * Dəyər - elementin faktiki dəyəri.

### SMPTE Format Xüsusiyyətləri

MXF fayl formatı aşağıdakı SMPTE spesifikasiyası ilə müəyyən edilmişdir.

* SMPTE ST 377-1: 2011. Televiziya — Material Exchange Format (MXF) — File Format Specification

* SMPTE ST 377-2 (2012-ci ilin yanvar ayına olan işlər davam edir). MXF üçün KLV Kodlanmış Genişləndirmə Sintaksisi.

* SMPTE ST 378:2004 (Arxiv 2010). Televiziya — Material mübadiləsi formatı (MXF) — Əməliyyat nümunəsi 1a (Tək Maddə, Tək Paket)

* SMPTE ST 379-1: 2009. Material Exchange Format (MXF) — MXF Ümumi Konteyneri

* SMPTE ST 379-2: 2010. Material Exchange Format (MXF) -- MXF Məhdud Ümumi Konteyner

* SMPTE ST 380:2004. Televiziya — Material Exchange Format (MXF) — Təsviri Metadata Sxemi-1 (Standart, Dinamik)

* SMPTE ST 381-1: 2005. Televiziya — Material mübadiləsi formatı (MXF) — MPEG axınlarının MXF ümumi konteynerinə (Dinamik) uyğunlaşdırılması

* SMPTE ST 381-2: 2011. Material mübadiləsi formatı (MXF) — MPEG axınlarının MXF məhdudlaşdırılmış ümumi konteynerinə uyğunlaşdırılması

* SMPTE ST 382:2007. Material mübadiləsi formatı (MXF) — AES3 axınlarının və yayım dalğasının səsinin MXF ümumi konteynerinə uyğunlaşdırılması

* SMPTE ST 383:2008. Televiziya — Material Exchange Format (MXF) — DV-DIF Datanın MXF Ümumi Konteynerinə Xəritəçəkmə

* SMPTE ST 384:2005. Televiziya — Material mübadiləsi formatı (MXF) — Sıxılmamış şəkillərin MXF Ümumi Konteynerində Xəritəçəkmə

* SMPTE ST 385:2004. Televiziya — Material mübadiləsi formatı (MXF) — SDTI-CP mahiyyəti və metaməlumatların MXF ümumi konteynerinə uyğunlaşdırılması

* SMPTE ST 386:2004 (Arxiv 2010). Televiziya — Material Exchange Format (MXF) — MXF Ümumi Konteynerinə D-10 Essence Növü Məlumatının Xəritəçəkilməsi

* SMPTE ST 387:2004 (Arxiv 2010). Televiziya — Material Exchange Format (MXF) — MXF Ümumi Konteynerinə D-11 Essence Növü Məlumatının Xəritəçəkilməsi

* SMPTE ST 388:2004 (Arxiv 2010). Televiziya — Material mübadiləsi formatı (MXF) — A-law kodlu audionun MXF ümumi konteynerinə uyğunlaşdırılması

* SMPTE ST 389:2005. Televiziya — Material Exchange Format (MXF) — MXF Ümumi Konteyner Əks Oynatma Sistemi Elementi

* SMPTE ST 390:2011. Televiziya — Material mübadiləsi formatı (MXF) — İxtisaslaşdırılmış əməliyyat nümunəsi "Atom" (Tək elementin sadələşdirilmiş təsviri)

* SMPTE ST 391:2004 (Arxiv 2010). Televiziya — Material mübadiləsi formatı (MXF) — Əməliyyat nümunəsi 1b (Tək element, qruplaşdırılmış paketlər)

* SMPTE ST 392:2004. Televiziya — Material Exchange Format (MXF) — Operativ Pattern 2a (Play-List Elementləri, Tək Paket)

* SMPTE ST 393:2004. Televiziya — Material Exchange Format (MXF) — Operativ Pattern 2b (Play-List Elementləri, Ganged Paketlər)

* SMPTE ST 394:2006. Televiziya — Material Exchange Format (MXF) — MXF Ümumi Konteyneri üçün Sistem Sxem 1

* SMPTE ST 405:2006. Televiziya — Material Exchange Format (MXF) — MXF Ümumi Konteyner Sistemi Sxem 1 üçün Elementlər və Fərdi Məlumat Elementləri

* SMPTE ST 407:2006. Televiziya — MXF — Əməliyyat Nümunələri 3a və 3b

* SMPTE ST 408:2006. Televiziya — MXF — Əməliyyat Nümunələri 1c, 2c və 3c

* SMPTE ST 410: 2008. Material Exchange Format - Ümumi Axın Bölməsi.

* SMPTE ST 422:2006. Material mübadiləsi formatı — JPEG2000 Kod axınının MXF Ümumi Konteynerinə uyğunlaşdırılması

* SMPTE ST 429.4:2006. D-Cinema Packaging — MXF JPEG 2000 Tətbiqi

* SMPTE ST 429.5:2006. D-Cinema Packaging — Müddətli Mətn İz Faylı

* SMPTE ST 429.6:2006. D-Cinema Packaging — MXF Track File Essence Encryption

* SMPTE ST 434:2006. Material mübadiləsi formatı — Metadata və fayl strukturu məlumatı üçün XML kodlaşdırması

* SMPTE ST 436:2006. Televiziya — VBI xətləri və köməkçi məlumat paketləri üçün MXF Xəritəçəkmələri

* SMPTE ST 2019-4:2009. VC-3 Kodlaşdırma Vahidlərinin MXF Ümumi Konteynerinə Xəritəçəkmə

* SMPTE ST 2037:2009. VC-1-in MXF Ümumi Konteynerinə uyğunlaşdırılması

* SMPTE RP 2008:2008. Material mübadiləsi formatı — AVC axınlarının MXF Ümumi Konteynerinə çəkilməsi

* SMPTE RP 2057:2011. MXF-də mətn əsaslı metadata daşınması

* SMPTE EG 41:2004. Material Exchange Format (MXF) — Mühəndislik Təlimatları. Qeyd: 2012-ci ilin yanvarında məsləhətləşəndə bu sənəd artıq SMPTE veb-saytında göstərilməyib.

* SMPTE EG 42:2004. Material Exchange Format (MXF) — MXF Təsviri Metadata

* SMPTE RDD 3:2008. e-VTR MXF Qarşılıqlı Fəaliyyət Spesifikasiyası

* SMPTE RDD 9-2009. Sony MPEG Long GOP Məhsullarının MXF Qarşılıqlı Fəaliyyət Spesifikasiyası

* SMPTE metadata reyestrinin elektron cədvəl menyusu.


### MXF Struktur Metadata

Struktur metadata MXF faylında əsasdır, çünki o, faylın məzmunu haqqında faydalı məlumatları ehtiva edir. MXF metadata çərçivə sürəti, çərçivə ölçüsü, faylın yaradılması tarixi və fərdi dəyişiklik tarixi kimi məlumatları ehtiva edir. Struktur metadata MXF faylının strukturunu və imkanlarını təsvir edir ki, bura müxtəlif vacib komponentlərin texniki təsviri və çıxış qrafikinin necə tərtib edildiyini çatdırmaq daxildir.

## İstinadlar

 * [MXF - Vikipediya](https://en.wikipedia.org/wiki/Material_Exchange_Format)
 * [MXF - Progress Report](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
 * [MXF üçün OpenSource C++ Kitabxanası](http://www.freemxf.org/)

