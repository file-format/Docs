{
  "date" : "2019-10-11",
  "keywords" : [ "vsdm file", "vsdm file format", "what is a vsdm file", "file", "vsdm example", "vsdm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDM - Microsoft Visio Rəsm Fayl Format",
  "description":"VSDM fayl formatı və VSDM faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm-az",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## VSDM faylı nədir?

.vsdm uzantılı fayllar makroları dəstəkləyən Microsoft Visio proqramı ilə yaradılmış rəsm fayllarıdır. VSDM faylları VSDX-ə bənzəyən OPC/XML çertyojlarıdır, eyni zamanda fayl açıldıqda makroları işə salmaq imkanı verir. Makrolar, Visual Basic for Applications (VBA) proqramında hazırlanmış və təkrarlanan tapşırıqları yerinə yetirmək üçün istifadə oluna bilən istifadəçi tərəfindən müəyyən edilmiş hərəkətlər/addımlardır. VSDM fayl formatı Microsoft Visio 2013-ün işə salınması ilə təqdim edildi. Visio faylları vizual obyektləri, axın diaqramlarını, UML diaqramını, məlumat axını, təşkilati diaqramları, proqram diaqramlarını, şəbəkə düzenini, verilənlər bazası modellərini, obyektlərin xəritələşdirilməsini və s. ehtiva edən çertyojlar yaratmaq üçün istifadə olunur. oxşar məlumatlar. Visio istifadə edərək yaradılan fayllar [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) və başqaları kimi müxtəlif fayl formatlarına da ixrac edilə bilər.

## VSDM fayl formatı

VSDM faylları Açıq Qablaşdırma Konvensiyalarına və XML-ə əsaslanır və tərtibatçılar bu faylla proqramlı şəkildə işləməyi öyrənməklə bu formatdan faydalana bilərlər. Format, Visio XML Drawing fayl formatından (.vdx) onun hissələri kimi eyni XML strukturlarının çoxunu miras alır. Üçüncü tərəf proqram təminatı Visio fayllarını fayl formatı səviyyəsində manipulyasiya edə bildiyi üçün Visio faylları ilə qarşılıqlı fəaliyyət xeyli artır.

Hər bir Visio faylı digər faylları və ya hissələri saxlayan paket adlanır. Paket hissəsi XML faylı, şəkil və ya hətta VBA həlli ola bilər. Paket daxilindəki hissələr sənəd və əlaqə hissələrinə bölünə bilər.

### Sənəd ###

Sənəd hissələri Visio faylının faktiki məzmununu və metadatasını, məsələn, faylın adı, birinci səhifə və onun tərkibindəki bütün formaları və hətta formalar üçün məlumat bağlantılarını ehtiva edir. Paketdəki şəkillər və mətn faylları sənəd hissələri hesab olunur.

### Münasibətlər ###

Visio faylının əlaqə hissələri \_rels qovluğunda saxlanılır və paketdəki hissələrin hər biri ilə necə əlaqəli olduğunu təsvir edir. O, həmçinin faylın strukturunu təmin edir. Müstəqil bir XML sənədi obyektlərin bir-biri ilə əlaqəsini müəyyən etmək üçün elementlərin ana/uşaq münasibətindən istifadə edir. Etibarlı Visio 2013 fayl formatı düzgün hissələr dəstini və paket hissələr arasındakı əlaqələri ehtiva edir.

Əlaqə hissələri paket daxilində müxtəlif sənəd hissələri arasındakı əlaqələri təsvir edən XML sənədləridir. Onlar iki element arasında əlaqəni müəyyənləşdirirlər: müəyyən mənbə (əlaqə faylının adı və yeri ilə müəyyən edilir) və müəyyən edilmiş hədəf sənəd hissəsi. Məsələn, əlaqə hissələri hansı forma ustalarının faylla əlaqəli olduğunu, səhifələrin fayl və bir-biri ilə necə əlaqəli olduğunu və ya şəkillərin və obyektlərin müəyyən bir səhifə ilə necə əlaqəli olduğunu təsvir etmək üçün istifadə olunur.

## İstinadlar ##

* [Visio Fayl Formatına Giriş](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


