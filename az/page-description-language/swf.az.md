{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "keywords": [
"SWF",
"fayl",
"uzadılması",
"format",
"video formatı",
"SWF faylı nədir",
"swf fayl formatı",
"swf fayl pleyeri",
"swf faylını necə açmaq olar"
],
  "title": "SWF Fayl - Shockwave Flash Film Fayl Format",
  "description": "SWF faylının nə olduğu və SWF faylının necə açılacağını yarada və göstərə bilən API-lər haqqında öyrənin.",
  "linktitle": "SWF",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sw-azf"
}
},
  "lastmod": "2019-09-10"
}

## SWF faylı nədir?

SWF faylı Adobe Flash ilə yaradılmış animasiya faylıdır. Animasiya yaratmaq üçün mətn, vektor şəkilləri, rastr şəkilləri, fəaliyyət skriptləri, dairələr, xətlər, kvadratlar və düzbucaqlı kimi müxtəlif növ elementlərdən ibarət ola bilər. SWF faylları bu multimedia elementlərini saniyədə müxtəlif kadrlarda (fps) ifa edilə bilən kadrlarda təşkil edir. SWF Qısa Veb Fayl deməkdir, lakin Shockwave Formatına malik olduğu da bilinir.

*SWF fayllarını** aça bilən proqramlara Adobe Flash Player (hazırda dayandırılmışdır) və Eltima Elmedia Player daxildir.

## SWF Fayl Format - Ətraflı Məlumat

SWF faylları ikili fayllar kimi diskdə saxlanmaq üçün istifadə edilmişdir. SWF fayl formatı vebsaytlara daxil edilə bilən və müstəqil olaraq oynaya bilən animasiyalar və oyunlar hazırlamaq üçün istifadə edilmişdir. O, həmçinin tərtibatçılara interaktiv multimedia proqramları yaratmaq üçün çoxlu seçimlər verən video və səsləri dəstəkləyirdi. SWF faylları Adobe Shockwave quraşdırılmış veb brauzerlərdə oxuna bilər. Adobe Flash 2020-ci ilin dekabrında qısa müddətə gəlmələri və təhlükəsizlik problemlərinə görə dayandırıldı.

## SWF Fayl Formatının Qısa Tarixi

SWF fayl formatı əvvəlcə FutureWave Proqramı tərəfindən hazırlanmışdır, fayl ölçüsünü kiçik saxlamaqla, daha yavaş şəbəkə bağlantısı olan hər hansı bir sistemdə oyunçu proqramında işləmək niyyəti ilə animasiyalar göstərmək üçün. 1996-cı ilin dekabrında Macromedia FutureWave-ə sahib idi və Macromedia Flash 1.0-a çevrildi.

In 2005, Macromedia was acquired by Adobe, who announced the SWF as a part of its open source project in 2008. Elə həmin il Adobe dünyanın məşhur veb mühərriklərinə SWF fayllarının taranmasına və indeksləşdirilməsinə icazə vermək üçün kod buraxdı. Bununla belə, SWF faylları Flash məzmununu internetdə dərc etmək üçün standart formata çevrildiyinə görə, SWF Kiçik Veb Formatı mənasını vermək üçün yenidən işlənmişdir.

## SWF Fayl Strukturu

Yol sadə xətlərdən Bezier əyrilərinə qədər olan əsas elementlərin seqmentlərinin ardıcıllığı olan SWF-də əsas qrafik elementdir. Bu sadə elementlər həmçinin kublar, ellipslər və hətta mətnlər kimi digər əlavə primitivlər yaratmağa kömək edir. SWF-dəki qrafik primitivlər SVG və MPEG-4 BIFS kimi digər formatların qrafik elementləri ilə oxşarlığa malikdir.

Siyahıları göstərməyə və artıq müəyyən edilmiş elementlərin yenidən istifadəsinə/adının dəyişdirilməsinə də format tərəfindən icazə verilir. SWF-nin ikili axın formatını etiket, ölçü və yük baxımından oxşar olan QuickTime atomları ilə müqayisə etmək olar. İkili axın formatı köhnə oyunçulara dəstəklənməyən məzmunu atlamağa imkan verir. SWF-nin orijinal versiyaları vektor qrafikası və şəkilləri təklif etməklə məhdudlaşsa da, buna görə də yeni versiyalar audio və video məzmununa da imkan verir.

A new, low-level 3D API of the Flash Player named “Stage3D” was introduced in version 11. Bu API OpenGL və ya Direct3D-nin analoqu kimi nəzərdə tutulmuşdu. Stage3D rəngləri Adobe Graphics Assembly Language (AGAL) adlanan aşağı səviyyəli dildə müəyyən edir. Aşağıda SWF fayl formatının bir neçə əsas məlumat növü verilmişdir.

### Koordinatlar

SWF fayl formatında XY koordinatları tam ədədlər kimi saxlanılır və twip adlanan vahiddə ölçülür. Twip məntiqi pikselin 1/20 hissəsindən ibarətdir. Məntiqi piksel və ekran pikseli fayl miqyaslanmadan 100% oxunduqda eynidir.

### Tam ədəd növləri və bayt sırası

SWF fayl formatında 8, 16, 32 və 64 bitlik imzalanmış və işarəsiz tam ədəd növlərinə icazə verilir. Tam ədədlərin saxlanması üçün kiçik bayt sırası istifadə olunur. Bayt daxilində olsa da, bit sırası big-endian-da saxlanılır. Bütün tam dəyərlər bayta uyğunlaşdırılmalıdır. İşarələnmiş tam ədədlər ənənəvi 2-in tamamlayıcı bit nümunələrindən istifadə etməklə təmsil olunur.

### Sabit nöqtəli nömrələr

Sabit nöqtəli nömrələrin iki növü SWF fayl formatı tərəfindən dəstəklənir, yəni 32 və 16 bit.

### Üzən Nöqtəli Nömrələr

SWF 8 və sonrakı versiyalarda üzən nöqtə növlərinin IEEE Standard 754-ə uyğun olan üç növ üzən nöqtəli nömrələrdən (FLOAT, FLOAT 16, DOUBLE) istifadə olunur.

### Kodlanmış Tam ədədlər

Kodlanmış tam ədədin bir növü SWF 9 və daha sonra dəyişən bayt sayı ilə dəstəklənir.

## İstinadlar

* [SWF fayl formatı](https://en.wikipedia.org/wiki/Swf)


