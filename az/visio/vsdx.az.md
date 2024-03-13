{
  "date" : "2019-10-11",
  "keywords" : [ "vsdx file", "vsdx file format", "what is a vsdx file", "file", "vsdx example", "vsdx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDX",
  "description":"VSDX faylları yarada və aça bilən VSDX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx-az",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## VSDX faylı nədir?

.vsdx uzantılı fayllar Microsoft Office 2013-dən etibarən təqdim edilmiş Microsoft Visio fayl formatını təmsil edir. O, Microsoft Visio-nun əvvəlki versiyaları tərəfindən dəstəklənən [.VSD](/visio/vsd/) ikili fayl formatını əvəz etmək üçün hazırlanmışdır. O, həmçinin Microsoft SharePoint Server 2013-də Visio Xidmətlərində dəstəklənir və SharePoint Serverdə dərc etmək üçün vasitəçi fayl formatını tələb etmir. Visio faylları vizual obyektləri, hərəkət sxemlərini, UML diaqramını, məlumat axını, təşkilati diaqramları, proqram diaqramlarını, şəbəkə düzenini, verilənlər bazası modellərini, obyektlərin xəritələşdirilməsini və digər oxşar məlumatları ehtiva edən çertyojlar yaratmaq üçün istifadə olunur. Visio istifadə edərək yaradılan fayllar [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) və başqaları kimi müxtəlif fayl formatlarına da ixrac edilə bilər.

## Fayl Format ##

VSDX faylları Açıq Qablaşdırma Konvensiyalarına və XML-ə əsaslanır və tərtibatçılar bu faylla proqramlı şəkildə işləməyi öyrənməklə bu formatdan faydalana bilərlər. Format, Visio XML Drawing fayl formatından (.vdx) onun hissələri kimi eyni XML strukturlarının çoxunu miras alır. Üçüncü tərəf proqram təminatı Visio fayllarını fayl formatı səviyyəsində manipulyasiya edə bildiyi üçün Visio faylları ilə qarşılıqlı fəaliyyət xeyli artır.

Visio 2013 fayl formatını təşkil edən bəzi digər fayl növlərinə aşağıdakılar daxildir:

* .vsdm (Visio makro ilə aktivləşdirilmiş rəsm)

* .vssx (Visio trafareti)

* .vssm (Visio makro-aktiv trafaret)

* .vstx (Visio şablonu)

* .vstm (Visio makro ilə aktivləşdirilmiş şablon)


Başlıq altında, Visio 2013 fayl formatı proqram məlumatlarını [ZIP](/compression/zip/) kimi arxivdə əlaqəli resurslarla birlikdə saxlamaq üçün strukturlaşdırılmış vasitələrdən istifadə edir. ZIP faylı digər növ faylları ehtiva etdiyi hər hansı bir standart çıxarma yardım proqramından istifadə etməklə çıxarıla bilər. VSDX faylının içindəki məzmunu görmək üçün sadəcə olaraq .vsdx fayl uzantısını .zip ilə əvəz edə bilərsiniz.

Hər bir Visio faylı digər faylları və ya hissələri saxlayan paket adlanır. Paket hissəsi XML faylı, şəkil və ya hətta VBA həlli ola bilər. Paket daxilindəki hissələr sənəd və əlaqə hissələrinə bölünə bilər.

### Sənəd ###

Sənəd hissələri Visio faylının faktiki məzmununu və metadatasını, məsələn, faylın adı, birinci səhifə və onun tərkibindəki bütün formaları, hətta formalar üçün məlumat bağlantılarını ehtiva edir. Paketdəki şəkillər və mətn faylları sənəd hissələri hesab olunur.

### Münasibətlər ###

Visio faylının əlaqə hissələri \_rels qovluğunda saxlanılır və paketdəki hissələrin hər biri ilə necə əlaqəli olduğunu təsvir edir. O, həmçinin faylın strukturunu təmin edir. Bağımsız bir XML sənədi obyektlərin bir-biri ilə əlaqəsini müəyyən etmək üçün elementlərin ana/uşaq münasibətindən istifadə edir. Etibarlı Visio 2013 fayl formatı düzgün hissələr dəstini və paket hissələr arasındakı əlaqələri ehtiva edir.

Əlaqə hissələri paket daxilində müxtəlif sənəd hissələri arasındakı əlaqələri təsvir edən XML sənədləridir. Onlar iki element arasında əlaqəni müəyyənləşdirirlər: müəyyən mənbə (əlaqə faylının adı və yeri ilə müəyyən edilir) və müəyyən edilmiş hədəf sənəd hissəsi. Məsələn, əlaqə hissələri hansı forma ustalarının faylla əlaqəli olduğunu, səhifələrin fayl və bir-biri ilə necə əlaqəli olduğunu və ya şəkillərin və obyektlərin müəyyən bir səhifə ilə necə əlaqəli olduğunu təsvir etmək üçün istifadə olunur.

## İstinadlar ##

* [Visio Fayl Formatına Giriş](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


