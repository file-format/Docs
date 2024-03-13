{
  "date": "2019-12-12",
  "keywords": [
"EPS",
"fayl",
"uzadılması",
"fayl formatı",
"Səhifə tərtibatı",
"Encapsulated PostScript"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "EPS fayl formatı və EPS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "EPS Fayl Format - Encapsulated PostScript Faylı",
  "linktitle": "EPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-ep-azs"
}
},
  "lastmod": "2019-09-10"
}

## EPS faylı nədir?

.eps faylı Encapsulated Postscript fayl formatında diskdə saxlanılan şəkil faylıdır. O, mətn, qrafika və şəkillərin istənilən kombinasiyasını ehtiva edə bilər. EPS faylları, həmçinin bu cür faylları aça bilən proqramlar tərəfindən göstərilmək üçün içəriyə daxil edilmiş bitmap önizləmə şəklini də daxil edə bilər.

## EPS Fayl Formatının Qısa Tarixi

Tarix nöqteyi-nəzərindən EPS fayl formatına sürətli nəzər salmaq aşağıdakı məlumatları ortaya qoyur:

* EPS-in ilk versiyası Adobe tərəfindən 1985-1988-ci illər arasında buraxılmışdır

* EPS spesifikasiyasının 2.0 versiyası 1989-cu ilin yanvarında nəşr edilmişdir

* EPS-nin 3.0 versiyası üçün spesifikasiya 1992-ci ildə ayrıca sənəd kimi nəşr edilmişdir; bu ən son nəşr olunmuş versiyadır.


EPS, Adobe-nin PostScript Dil Sənədinin Strukturlaşdırılması Konvensiyalarının Spesifikasiyasının 9-cu bəndində təsvir edilən Açıq Strukturlaşdırma Konvensiyalarının genişləndirilməsi mexanizmi ilə birlikdə Adobe Illustrator Artwork fayl formatının ilkin versiyalarının əsasını təşkil etmişdir.

## EPS fayl formatı

EPS mülkiyyətli, lakin açıq şəkildə sənədləşdirilmiş formatdır və EPS fayl formatının spesifikasiyaları tərtibatçının arayışı üçün açıq şəkildə mövcuddur. EPS fayl formatına uyğun olan [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Sənədin Strukturlaşdırılması Konvensiyası)dır və DSC tərəfindən müəyyən edilmiş bütün qaydalara riayət edir. DSC Adobe tərəfindən PostScript sənədləri üçün xüsusi fayl formatıdır. EPS fayllarını oxuya bildiyini iddia edən hər hansı proqram DSC-yə uyğun olmalıdır.

EPS faylı aşağıda izah edildiyi kimi iki əsas hissədən ibarətdir.

### Şəkilə bax ###

Tipik bir EPS faylı bir neçə sistem və ya tətbiqi əhatə edən iş prosesində rahat istifadə üçün nəzərdə tutulmuş formatda önizləmə şəklini ehtiva edir. İlkin baxışın məqsədi əksər qrafik proqramların göstərə biləcəyi formatda bir şəkilə sahib olmaqdır; önizləmə adətən piksel ölçülərində və/yaxud bit dərinliyində daha aşağı rezolyusiyaya malikdir. Önizləmə faylı bir sıra formatlardan birində ola bilər. EPS_3 üçün spesifikasiya üç cihaza məxsus önizləmə formatını sadalayır:

* Apple Macintosh üçün QuickDraw tətbiqi tərəfindən istifadə edilən PICT şəkli

* DOS kompüterləri üçün TIFF bitmapı

* Windows metafayl.


PICT və Windows Metafayl həm bitmap məlumatlarını, həm də vektor qrafiklərini özündə birləşdirə bilər. Bundan əlavə, spesifikasiya quraşdırılmış bitmaplı önizləmə şəkli üçün çox sadə cihazdan müstəqil təqdimatı müəyyən edir. Bu təqdimat Encapsulated PostScript Interchange Format (EPSI) kimi tanınır.

EPSI önizləməsi ASCII hexadecimal kimi təmsil olunan, eyniləşdirmə üçün bir neçə PostScript şərhi arasında bükülmüş və sadə və asanlıqla daşınmaq üçün nəzərdə tutulmuş bitmapdır. EPS fayllarını fərqli baxış formatları ilə fərqləndirmək üçün EPS spesifikasiyasında müxtəlif DOS fayl uzantıları və Macintosh fayl növləri tövsiyə edilmişdir.

### PostScript Kodu

Ən azı EPS fayl formatında aşağıdakılar olmalıdır:

* başlıq şərhi, %!PS-Adobe-3.0 EPSF-3.0

* və məhdudlaşdırıcı qutu şərhi, %%BoundingBox: llx lly urx ury, təsvirin hüdudlarını təsvir edir. Bu dörd arqument məhdudlaşdırıcı qutunun aşağı sol (llx, lly) və yuxarı sağ (urx, ury) künclərinə uyğundur.


EPS faylı aşağıdakı operatorlardan heç birini istifadə edə bilməz:

* bant cihazı,

* cleardictstack

* surəti

* silmə səhifəsi

* çıxış serveri

* çərçivə cihazı

* grestoreall

* initclip

* initqrafik

* initmatrix

* çıxın

* render lentləri

* qlobal

* quraşdırma cihazı

* setshared

* başlanğıc işi.


## EPS-nin digər fayl formatlarına çevrilməsi

EPS faylları Adobe Illustrator, Photoshop və PaintShop Pro kimi müxtəlif proqramlardan istifadə etməklə [JPG](/image/jpeg/), [PNG](/image/png/), [TIFF](/image/tiff/) və [PDF](/pdf/) kimi standart şəkil formatlarına çevrilə bilər.

EPS fayllarında [security vulnerability](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) olduğuna görə Office 2016, Office 2013, Office 2010 və Office 365 EPS fayllarını Office sənədlərinə daxil etmək imkanını söndürdü.

## İstinadlar

* [Encapsulated PostScript - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Encapsulated_PostScript)


