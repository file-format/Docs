{
  "date": "2019-10-11",
  "keywords": [
"XSLFO",
"XSL Formatlaşdırma Obyektləri",
"Fayl",
"Uzatma",
"Fayl Format",
"Genişlənən Üslub Cədvəli Dili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLFO",
  "description": "XSLFO faylları yarada və aça bilən XSLFO fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "XSLFO",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xslf-azo"
}
},
  "lastmod": "2021-04-23"
}

## XSL-FO faylı nədir? ##

XSL-FO (XSL Formatting Objects) XML sənədlərini formatlaşdırmaq üçün güclü üslub cədvəli dilidir. Kağızın və çapın məhdud formasının semantikası ölçülər sabit olduqda XSL-FO ilə ifadə edilir. Dəyişən ölçüləri olan brauzer pəncərəsinin qeyri-məhdud formasının semantikasını təmsil edən HTML-dən fərqli olaraq. XSL-FO ilə formatlanmış XML sənədləri əsasən PDF faylları yaratmaq üçün istifadə olunur. XSL (Extensible Stylesheet Language) XML sənədlərinin və bu dilin XSL-FO hissəsinin formatlaşdırılması və mübadiləsi üçün dizayn üçün nəzərdə tutulmuş xüsusiyyətlərə malik tam W3C texnologiyaları toplusudur. XSLT və XPath də XSL-in digər hissələridir.

XML sənədlərinin əvvəlcə XSL-FO-ya çevrilməsi təklif olunur, PDF bu meyarlara nümunədir. PDF-də nəticələr əvvəlcə XSLT, sonra isə XSL-FO formatlayıcısı ilə verilir. Bu şəkildə XML sənədləri təsadüfi formatlaşdırıla bilər. Baxmayaraq ki, XSL-FO Cascading Style Sheet (CSS) xassələrindən istifadə etmək və onları real format üçün lazım olan yerdə genişləndirmək kimi üstünlüklərdən istifadə edir, o, XSL-FO terminologiyasında səhifə ustaları adlanan səhifə şablonlarını təmin edir. XSL-FO həmçinin kifayət qədər mürəkkəb sənədlər üçün formatlaşdırma təmin edir və indeks yaratmağı dəstəkləyir.

## Tarix və əsas anlayışlar ##

2012-ci ilin yanvarında XSL-FO-nun İşçi Layihəsi sonuncu dəfə yeniləndi və 2013-cü ilin noyabrında onun İşçi Qrupu bağlandı. XSL üslub cədvəli sinif nümunəsinin formatlaşdırma lüğətindən istifadə edən XML sənədinə necə çevrildiyini təsvir etməklə XML sənədləri sinfinin təqdimatını təyin edir. XSL-FO inteqrasiya olunmuş təqdimat dilidir və HTML-də istifadə olunan semantik işarələrə malik deyil. Bundan əlavə, bu dil xarici HTML və ya XML sənədinin standart parametrlərini dəyişdirən CSS-dən fərqli olaraq, sənədin bütün məlumatlarını özündə saxlayır.

XSL-FO-dan istifadənin ümumi meyarları istifadəçinin sənədi FO-da deyil, XML dilində yazmasıdır. Bundan sonra XSLT çevrilməsi baş verir. Bu XSLT çevrilməsi XML-in XSL-FO-ya çevrilməsindən məsuldur. XSL-FO sənədi yaradılan kimi, o, FO prosessoru adlanan proqrama təhvil verilir. FO prosessorları bu sənədi oxuna bilən və çap edilə bilən sənədə çevirmək üçün məsuliyyət daşıyırlar. PDF faylları və ya PS XSL-FO-nun ən ümumi çıxışına nümunədir. Lakin bu o demək deyil ki, FO prosessoru yalnız bu iki növ formatı çıxış kimi istehsal edə bilər. Bəzi FO prosessorları RTF fayllarında çıxış edə bilər və ya hətta istifadəçinin GUI-də pəncərə görünə bilər, bu pəncərə səhifənin ardıcıllığını və onların məzmununu göstərir.

XSL-FO sənədi o mənada PDF və ya PS-dən fərqlidir, nəticədə müxtəlif səhifələrdə mətn tərtibatını müəyyən etmir. Ola bilsin ki, o, səhifələrə üslub verir və məzmunun göstəriləcəyi yerləri müəyyənləşdirir. Bundan əlavə, FO prosessoru mətni FO sənədi ilə müəyyən edilmiş sərhədlər daxilində təşkil edir. Bu spesifikasiya hətta müxtəlif FO prosessorlarına nəticədə yaradılmış səhifələrə uyğun davranmağa icazə verir. Belə davranışa misal tiredir, bir neçə FO prosessoru sətir kəsildikdə yer saxlamaq üçün sözləri defis edə bilər, bəzi prosessorlar isə bu seçimi seçmir. Prosessorların tələblərinə uyğun müxtəlif defis alqoritmləri seçməkdən asılıdır. Bu defis alqoritmləri çox sadə və ya daha mürəkkəb ola bilər. Bəzi hallarda, XSL-FO spesifikasiyası FO prosessorlarını, tərtibat kontekstində müəyyən dərəcədə seçimlə açıq şəkildə sanksiyalara məruz qoyur.

FO prosessorları arasındakı bu dəyişkənlik prosessorların çox vaxt diqqətsiz qaldığı müxtəlif nəticələr yaradır. Çünki XSL-FO-nun ümumi diqqəti səhifələnmiş/çap edilmiş sənədlərin hazırlanmasıdır. XSL-FO sənədlərinin özləri adətən vasitəçi kimi çıxış edirlər, onların əsas funksiyası ya PDF faylları, ya da paylanacaq çıxış kimi çap oluna bilən sənəd yaratmaqdır. HTML/CSS və ya XSL-FO-da, formatlaşdırma dilini daxil etmək əvəzinə, son nəticə kimi PDF-i paylamaq, formatlaşdırma dilinin tərcüməçiləri arasında fərqlər səbəbindən yaranan çox yönlülükdən qəbuledicilərin təsirsiz qaldığını göstərir. Digər tərəfdən, aydındır ki, sənəd alıcıların müxtəlif ehtiyaclarını ödəyə bilər, məsələn, dəyişən səhifə ölçüsü və ya istənilən şrift ölçüsü və ya səhifə və ya çap üçün uyğunlaşdırma.

## XSLFO Fayl Format ##

SL-FO sənədləri əsasən XML sənədləridir, lakin onlar heç bir sxemə əməl etmirlər. Onun yerinə SL-FO sənədləri öz dillərinin spesifikasiyasında müəyyən edilmiş sintaksisə əməl edir. Hər bir XSL-FO sənədində iki bölmə tələb olunur:

1. Etiketli səhifə tərtibatlarının siyahısını təyin edən bölmə.
1. Sənəd məlumatlarının bütün təfərrüatlarını özündə əks etdirən, işarələmə ilə, müxtəlif səhifə tərtibatları vasitəsilə müxtəlif səhifələrdə məzmunun göstərilməsini müəyyən edən bölmə.

Səhifənin xüsusiyyətləri xüsusi dil üçün konvensiyalara uyğun olaraq mətn üçün təşkilatı təyin edə bilən səhifə tərtibatlarında qeyd olunur. Bundan əlavə, səhifənin ölçüsü, onların kənarları və səhifələrin ardıcıllığı (tək və cüt səhifələr üçün müxtəlif xassələri sanksiya edir) səhifə tərtibatı ilə də müəyyən edilir.

Sənədin məlumat hissəsi bir sıra axınlara bölünür, burada hər bir axın bir səhifə tərtibatı ilə əlaqələndirilir. Axınlar onlara blokların siyahısını əlavə edir. Blokların bu siyahısı daxili işarələmə xüsusiyyətlərini və ya mətn məlumatlarının siyahısını və ya hər ikisini eyni vaxtda ehtiva edə bilər. Sənədin kənarlarında səhifə nömrələri və ya fəsil başlıqları da göstərilə bilər. Həm blokların, həm də daxili elementlərin funksionallığı CSS-də olduğu kimi qalır, lakin bəzi doldurma və kənar qaydaları FO və CSS arasında fərqlidir.

The page orientation direction is entirely specified for the extension of blocks and inlines, thus making FO documents perform under the languages different from English. The language of the FO specification uses the words start and end rather than left and right for directions description. XSL-FO's basic content markup and cascading rules are taken from CSS. XSL-FO's language agrees to the following specifications.

## Çoxlu sütun ##

Səhifədə bir neçə sütun və blok ola bilər və standart olaraq bir sütundan digərinə uzana bilər. Birdən çox səhifənin müxtəlif eni və sütun sayına malik olmasına icazə verilir. Bütün FO xüsusiyyətləri çox sütunlu səhifənin sərhədlərini izləyir.

### Siyahılar ###

XSL-FO siyahısı yanaq-gövdə ilə düzülmüş iki blok dəsti ilə qurulur. Konseptual olaraq siyahıda soldakı blok nömrəni, gülləni və ya mətn sətirini göstərir, sağ tərəfdəki blok isə gözlənildiyi kimi işləyə bilər. XSL-FO siyahılarının nömrələnməsi adətən XSLT tərəfindən həyata keçirilir.

### Cədvəllər ###

FO cədvəli HTML/CSS cədvəlinə bənzəyir. İstifadəçi hər bir fərdi hüceyrə üçün məlumat sətirlərini, üslub məlumatlarını, fon rəngini seçə bilər. Fərqli üslub məlumatlarından istifadə edərək, istifadəçi birinci sıranı cədvəl başlığı sırası kimi seçmək imtiyazına malikdir. FO prosessoruna hər bir sütunun məkan spesifikasiyası və ya mətni cədvələ avtomatik uyğunlaşdırmaq üçün açıq şəkildə məlumat verilə bilər.

### İndeksləmə ###

XSL-FO 1.1 has features that help to generate an index through referencing properly marked-up elements.

### Faydaları ###

* Məzmuna əsaslanan nəşrlər üçün uyğundur

* İstifadə rahatlığı

* Aşağı qiymət


## İstinadlar ##

* [XSL-FO nədir?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)

* [XSL Formatlaşdırma Obyektləri](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)


