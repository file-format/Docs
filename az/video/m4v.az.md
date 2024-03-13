{
  "date": "2019-10-11",
  "keywords": [
"M4V",
"fayl",
"uzadılması",
"format",
"MPEG-4",
"Rəqəmsal Hüquqların İdarə Edilməsi",
"DRM",
"alma",
"video"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4V",
  "description": "M4V fayl formatı və M4V faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "M4V",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-azv"
}
},
  "lastmod": "2019-09-14"
}

## M4V faylı nədir?

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection to protect privacy or copy. Videos and audio tracks are wrapped around by container files to indexing and organizing playback streams. In addition, containers also provide the feature of chapters similar to those on DVDs. Apple uses M4V to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used to purchase the video. However, if DRM-protection is removed from M4V files, these files can be played in other video players by changing the extension from .m4v to .mp4, which is why M4V files are associated with MPEG-4. M4V video üçün H.264, audio kodlaşdırma və deşifrə üçün **[AAC](/audio/aac/)** və Dolby Digital istifadə edir.

## M4V Fayl Strukturu ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V M4V_ olmalıdır alt tip ilə müəyyən edilir. Sonrakı parça növləri əvvəlcədən təyin edilmiş imzalardır: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, wide , load, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt, ssrc,  PICT. Naməlum növ aşkarlanana qədər parçaları təkrarlayan M4V faylını tərtib edirik.

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Ofset 32-də (onaltılıq: 20) ölçüsü 30,322 (hex: 00 00 76 72, böyük endian, aşağı bayt) və **moov** (hex: 6D 6F 6F) yazın ikinci hissə yerləşir. 76). Növbəti hissə 32+30,322#30,354 (onaltılıq: 00 00 76 92) ofsetində yerləşir və ölçüsü 8 (hex: 00 00 00 08) və **free** (onaltılıq: 66 72 65 65) növünə malikdir.
### M4V-də istifadə olunan kodeklər ###

#### Video Codec H.264 ####

H.264 video sıxılma standartı rəqəmsal videonu ötürmə və ya saxlama tələb olunduqda daha az yer tələb edən formata çevirir. M4V video sıxılma üçün H.264 istifadə edir. Onun tətbiqi DVD, TV, Videokonfrans və internet üzərindən video axınını əhatə edir. H.264 iki əsas hissədən ibarətdir: Kodlayıcı – Videonu sıxışdıran, Dekoder – Sıxılmış videonu geri açan. Aşağıdakı şəkildə kodlaşdırma və dekodlaşdırma prosesləri vurğulanır və digər proseslər H.264 standartında əhatə olunur.

##### H.264-də Video Kodlaşdırma və Deşifrə Prosesi #####

Sıxılmış H.264 bit axını üçün video kodlayıcı proqnozlaşdırma, transformasiya və kodlaşdırma prosesini həyata keçirir. Eyni zamanda, dekoder video faylı geri istehsal etmək üçün dekodlaşdırma, tərs çevrilmə və yenidən qurulmasının tərs prosesini həyata keçirir. H.264 MPEG ölçüsünün yarısını götürür.

#### Audio Codec ####

Qabaqcıl Audio Kodlaşdırma (AAC) itkili rəqəmsal audio sıxılma üçün audio kodekdir və M4V konteynerində istifadə olunur. AAC [MP3](/audio/mp3/) formatının varisidir və eyni bit sürəti ilə MP3-dən daha yaxşı keyfiyyət əldə edir. AAC formatı sıxılma prosesi zamanı daha az əhəmiyyət kəsb edən bəzi məlumatları atır. AAC dəyişən bit sürəti (VBR) blok-əsaslı kodekdir, burada hər blok 1024 zaman domen nümunəsini deşifrə edir.

### İstinadlar ###

* [Vikipediya - M4V](https://en.wikipedia.org/wiki/M4V)

* [Vikipediya - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)


