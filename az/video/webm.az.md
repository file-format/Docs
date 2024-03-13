---
date: 2019-10-11
keywords: WEBM, What is a WEBM file, WEBM File Format
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: LWEBM faylı yarada və aça bilən WEBM fayl formatı və API-lər haqqında qazanıns.
title: WEBM - WebM Video Fayl Formasıat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## WEBM faylı nədir?

.webm uzantısı olan fayl açıq, royaltisiz WebM fayl formatına əsaslanan video fayldır. O, internetdə video paylaşmaq üçün nəzərdə tutulmuşdur və video və audio formatları daxil olmaqla fayl konteyner strukturunu müəyyən edir. WebM 100% pulsuzdur, HTML, HTTP və TCP/IP kimi açıq texnologiyalara əsaslanan yüksək keyfiyyətli həyata keçirir və həyata keçirmək üçün hər kəs üçün açıqdır. WebM xüsusi olaraq internetdə video təqdim etmək üçün nəzərdə tutulmuşdur ki, bu da onu aşağı hesablama izi ilə axın üçün optimallaşdırır. Bu, onu istənilən cihazda, xüsusən də aşağı güclü netbuklar, əl telefonları və planşetlərdə videoların oxunması üçün uyğun edir.

## WEBM fayl formatı

WebM fayl strukturu Matroska [MKV](/video/mkv/) konteyner fayl formatının alt çoxluğuna əsaslanır. WebM faylında mövcud olan video axınları sıxılmada yüksək effektiv olan VP8 və ya VP9 sıxılma texnologiyalarından istifadə etməklə sıxılır. Eynilə, WebM faylındakı audio axınlar [Xiph Foundation](https://www.xiph.org/) tərəfindən hazırlanmış Vorbis və ya Opus kodeklərindən istifadə etməklə sıxılır. Bütün bu videolar və audio kodeklər royaltisizdir və heç bir ödəniş etmədən istifadə edilə bilər.

Aşağıda WebM fayl formatı üçün ümumiləşdirilmiş spesifikasiyalar verilmişdir.

|Sahə|Təsvir|
---|---|
|MIME tipli |video/webm|
|Yalnız audio MIME tipli |audio/webm|
|Vahid Tip İdentifikatoru| org.webmproject.webm|
|Video Kodek Adı| VP8 və ya VP9|
|Audio Codec Adı| Vorbis və ya Opus|

### WebM Elementləri

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### EBML

|Adı |Təsviri|
---|---|
|EBML|İzlənəcək verilənlərin EBML xüsusiyyətlərini təyin edin. Hər bir EBML sənədi bununla başlamalıdır.|
|EBMLVersion |Faylı yaratmaq üçün istifadə edilən EBML analizatorunun versiyası.|
|EBMLReadVersion|Bu faylı oxumaq üçün təhlilçinin dəstəkləməli olduğu minimum EBML versiyası.|
|EBMLMaxIDLength |Bu faylda tapa biləcəyiniz ID-lərin maksimum uzunluğu (Matroskada 4 və ya daha az).|
|EBMLMaxSizeLength|Bu faylda tapa biləcəyiniz ölçülərin maksimum uzunluğu (Matroskada 8 və ya daha az). Bu, elementin əvvəlində göstərilən element ölçüsünü ləğv etmir. EBLMMaxSizeLength tərəfindən icazə veriləndən daha böyük ölçüyə malik olan elementlər etibarsız sayılacaq.|
|DocType|Bu EBML başlığından sonra gələn sənəd növünü təsvir edən sətir (bizim halda webm).|
|DocTypeVersion|Faylı yaratmaq üçün istifadə edilən DocType tərcüməçisinin versiyası.|
|DocTypeReadVersion|Tərcüməçinin bu faylı oxumaq üçün dəstəkləməli olduğu minimum DocType versiyası.|

#### Qlobal Elementlər

Hal-hazırda, zədələnmiş məlumatlardan istifadə zamanı gözlənilməz davranışların qarşısını almaq üçün zədələnmiş məlumatları ləğv etmək üçün istifadə edilən yalnız Void” elementi dəstəklənir. Məzmun atılır. Daha sonra istifadə üçün alt elementdə yer ayırmaq üçün də istifadə olunur.

#### Seqment
Bu element bütün digər yuxarı səviyyəli (1-ci səviyyə) elementləri ehtiva edir. Tipik olaraq Matroska faylı 1 seqmentdən ibarətdir.

#### Meta Axtarış Məlumatı

Aşağıdakı axtarış məlumatı dəstəklənir.

|Element Adı |Təsvir|
---|---|
|SeekHead |Digər səviyyə 1 elementinin mövqeyini ehtiva edir.|
|Axtar |EBML elementinə tək axtarış girişini ehtiva edir.|
|SeekID |Element adına uyğun gələn ikili ID.|
|SeekPosition |Elementin seqmentdəki mövqeyi (0 = birinci səviyyə 1 element).|

## İstinadlar

* [WebM](https://www.webmproject.org/)

* [WebM Code Repositories](https://www.webmproject.org/code/#webp-repositories)


