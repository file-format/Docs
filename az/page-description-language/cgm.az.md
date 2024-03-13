{
  "date": "2019-10-11",
  "keywords": [
"CGM",
"Computer Graphics Metafile",
"Fayl",
"Uzatma",
"Fayl Format",
"Vektor qrafikası",
"Metafayl təsviri"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CGM fayl formatı",
  "description": "CGM faylları yarada və aça bilən CGM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CGM",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-cg-azm"
}
},
  "lastmod": "2021-04-23"
}

## CGM faylı nədir? ##

Kompüter Qrafikası Metafayl (CGM) vektor qrafikasının (2D), rastr qrafikasının və mətnin saxlanması və mübadiləsi üçün pulsuz, platformadan müstəqil, beynəlxalq standart metafayl formatıdır. CGM təsvir istehsalı üçün obyekt yönümlü yanaşma və bir çox funksiya müddəalarından istifadə edir. CGM, təsviri göstərmək üçün qrafik elementləri yenidən formalaşdırmaq üçün bu obyekt yönümlü xüsusiyyətlərdən istifadə edir. Metafayl digər faylları müəyyən edən zəruri məlumatları ehtiva edir. CGM-də mətn əsaslı mənbə faylı bütün qrafik elementləri ehtiva edir və sonradan ikili fayla yığıla bilər. Əsasən, CGM hər hansı bir platformadan və ya cihazdan asılı olmayaraq 2D qrafik məlumat mübadiləsini asanlaşdırmaq üçün bir yoldur.

CGM formatı funksiyaları yerinə yetirmək üçün müxtəlif elementləri təmin edir və həndəsi primitivləri və qrafik məlumatları tənzimləmək üçün obyektləri işarələyir. Baxmayaraq ki, CGM veb səhifələrdə qrafik sənətini göstərmək üçün digər formatlarla əvəz olunsa da, veb səhifələr tərəfindən yaxşı dəstəklənmir, hələ də sənaye, aviasiya və digər texniki proqramlar arasında çox populyardır. Baxmayaraq ki, World Wide Web Konsorsiumu İnternetdə CGM-dən istifadə üçün alternativ bir yanaşma olan WebCGM-i inkişaf etdirmişdir. Əsas CGM tətbiqi Qrafik Nüvə Sisteminin (GKS) əsas əməliyyatlarının ardıcıllığının təsviri idi. Peşəkar dizaynlarda çox qəbul edilməmişdir, lakin əsasən DXF və SVG kimi digər formatlarla əvəz edilmişdir.

## Tarix ##

CGM 1987-ci ildə beynəlxalq standarta çevrildi (ISO 8632-1987) və həmçinin Böyük Britaniyada BSI və ABŞ-da ANSI tərəfindən milli standart kimi qəbul edildi. 1991-ci ildə edilən bir sıra düzəlişlərdən sonra 1992-ci ildə yenidən işlənmiş CGM standartı buraxıldı (ISO 8632:1992). 2001-ci ildə Ümumdünya Veb Konsorsiumu veb-səhifələrlə istifadə etmək üçün təkmilləşdirilmiş imkanlara malik WebCGM-i inkişaf etdirdi. 2007-ci ildə WebCGM-in ikinci versiyası, təkmilləşdirilmiş imkanlarla üçüncü versiyası isə 2010-cu ildə buraxıldı.

## CGM Fayl Format ##

Kompüter qrafikası metafaylları əsasən qrafik məlumat üçün verilənlər bazasıdır və qrafik məlumatların tutulması, saxlanması və ötürülməsi üçün vasitələri təmin edir. Nəticə etibarilə, metafayl formatında tətbiqin icrası ilə eyni vaxtda verilənlər bazası yaratmaq üçün qrafik sistem komponenti olmalıdır. Əksər hallarda bu komponent metafayl generatorudur. Bununla yanaşı, metafaylda qrafik məlumatları əldə edə, şərh edə və göstərə bilən başqa bir komponentə ehtiyac var. Bu ehtiyac metafayl tərcüməçisinin iştirakı ilə ödənilir. Aşağıdakı rəqəm qrafik metafayl iş mühitini təmsil edir.

CGM-nin tipik qrafik sisteminin digər komponentləri ilə əlaqəsi yuxarıdakı şəkildə göstərilmişdir. Şəkildən də aydın olur ki, metafaylın funksionallığı son cihazın çıxışından asılı deyil.

Generally, there are two categories of metafile: **section capture** and **picture capture**. The primary functionality of picture capture metafile is the capturing of device-independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two-level structure.

1. Metafayl təsviri
1. Məntiqi cəhətdən müstəqil şəkillər hovuzu

Hər bir şəkil şəkil deskriptorlarının toplusudur və şəkil tərifi də daxil olmaqla şəkil korpusudur. metafayl deskriptoru həmin metafaylın bütün şəkillərinə eyni dərəcədə aid olan təsviri məlumatı müəyyən edir. Bu məlumat tərcüməçiyə metafaylı düzgün təhlil etməyə və şəklin düzgün göstərilməsi üçün tələb olunan resursları tanımağa kömək edir. Şəkil deskriptoru təsviri məlumatı da əhatə etsə də, o, yalnız təsviredicinin yerləşdiyi şəkli tanıya bilər. Bu fayl formatında hər bir şəkil tərifi müstəqil və məntiqi olaraq suverendir. Onlar fayldakı bütün digər şəkil təriflərindən müstəqildirlər. Meta-deskriptorun şərhindən dərhal sonra şəkillərə təsadüfi şəkildə daxil olmaq və şərh etmək olar. Əvvəlki şəkillərin vəziyyətindəki dəyişiklik onların davamçılarına heç bir təsir göstərmir. Bu şəkil müstəqilliyi CGM.CGM-in başqa bir görkəmli xüsusiyyətidir. CGM virtual cihaz koordinatları adlanan 2D Kartezian koordinatları olan və diapazonu və qranularlığı təmsil edən say və ya dəqiqliklə təmsil oluna bilən koordinatlar məkanından ibarətdir. CGM həm rənglərin birbaşa seçimini, həm də indeks əsaslı seçimi müəyyən edir. Birincidə rəng təyinedicisi RGB üçlüyündən ibarətdir, daha sonra isə rəng təyinedicisi indeksi rəng cədvəlinə göstərir.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
