{
  "date": "2019-12-09",
  "keywords": [
"3mf fayl",
"3mf fayl formatı",
"3mf fayl nədir",
"fayl",
"3mf nümunəsi",
"3mf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "3MF",
  "description": "3MF fayl formatı və 3MF fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "3MF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3m-azf"
}
},
  "lastmod": "2019-12-09"
}

## 3MF faylı nədir?

3MF, 3D İstehsalat Format, 3D obyekt modellərini müxtəlif digər proqramlara, platformalara, xidmətlərə və printerlərə göstərmək üçün proqramlar tərəfindən istifadə olunur. O, 3D printerlərin ən son versiyaları ilə işləmək üçün [STL](/cad/stl/) kimi digər 3D fayl formatlarında məhdudiyyətlərin və problemlərin qarşısını almaq üçün yaradılmışdır. 3MF, 3MF konsorsiumu tərəfindən hazırlanmış və nəşr edilmiş nisbətən yeni fayl formatıdır. O, modeli tam təsvir etmək üçün kifayət qədər zəngindir, daxili məlumatları, rəngi və 3D çapda yeni innovasiyaları dəstəkləmək üçün onu genişləndirilə bilən digər xüsusiyyətləri özündə saxlayır. Format genişləndirilə bilər, geniş şəkildə qəbul edilə bilər və digər geniş istifadə olunan fayl formatlarını əhatə edən problemlərdən azaddır.

## 3MF Fayl Formatının Qısa Tarixi

STL və digərləri kimi mövcud model təsviri fayl formatlarında mövcud məhdudiyyətlər aparıcı brendləri bir araya gətirməyə və 3D çap üçün daha genişlənən fayl formatını formalaşdırmağa vadar edir. Tətbiqlərin model məlumatlarını 3D printerlərə necə ötürməsi vacib bir məsələ idi. Beləliklə, 3MF konsorsiumu, 3D çap ehtiyaclarını ödəmək üçün kifayət qədər genişləndirilə bilən 3MF adlı yeni 3D fayl formatını dəstəkləmək üçün yarandı. Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP və başqaları da daxil olmaqla bir neçə şirkət bu konsorsiumun bir hissəsi idi. Microsoft, 3MF Konsorsiumunun birgə spesifikasiyanın gələcək inkişafı üçün başlanğıc nöqtəsi kimi davam etməkdə olan 3D fayl formatını hədiyyə etdi.

## 3MF Fayl Format - Ətraflı Məlumat

3MF XML əsaslı məlumat formatıdır - insan tərəfindən oxuna bilən sıxılmış XML - bu, 3D istehsalı ilə bağlı məlumatların təriflərini, o cümlədən fərdi məlumatlar üçün üçüncü tərəfin genişləndirilməsini ehtiva edir. 3MF fayl formatı digər 3D fayl formatlarının üzləşdiyi məhdudiyyətlər və problemləri nəzərə alaraq tərtib edilmişdir. Bu, 3MF fayl formatının formalaşmasına gətirib çıxarır, yəni:

* **Tam:** Bütün lazımi model, material və əmlak məlumatlarını bir arxivdə ehtiva edir

* **İnsan tərəfindən oxuna bilən:** İnkişafı asanlaşdırmaq üçün OPC, [ZIP](/compression/zip/) və XML kimi ümumi strukturlardan istifadə

* **Sadə:** İnkişafı asanlaşdıran və təsdiqi sürətli edən qısa, aydın spesifikasiya

* **Genişləndirilə bilən:** XML ad boşluqlarından istifadə uyğunluğu qoruyarkən həm ictimai, həm də şəxsi genişləndirmələrə imkan verir

* **Birmənalı deyil:** Aydın dil və uyğunluq testləri faylın həmişə rəqəmsaldan fiziki səviyyəyə uyğun olmasını təmin edir

* **Pulsuz:** 3MF spesifikasiyasına giriş və tətbiqi həmişə qonorar, patent və lisenziyasızdır və həmişə olacaq


The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## 3MF Fayl Formatının Xüsusiyyətləri

3MF fayl formatı fiziki modeli üçün ZIP arxivi şəklində Açıq Qablaşdırma spesifikasiyalarından istifadə edir. Bu, sənəddəki xüsusi məqsədi yerinə yetirən dəqiq müəyyən edilmiş hissələr və əlaqələr toplusunu ehtiva edir. Bu, həm də formatın rəqəmsal imzalar və miniatürlər daxil olmaqla paket funksiyasına uyğun olmasını təmin edir.

### 3MF Sənədi - İcmal

Tipik 3MF sənədi aşağıdakı kimi görünür:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**Ad**|**Təsvir**|**Əlaqə mənbəyi**|**Tələb olunur/İstəyə bağlı**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|Əsas Xüsusiyyətlər|Müxtəlif sənəd xüsusiyyətlərini ehtiva edən OPC hissəsi.|Paket|İSTEĞE BAĞLI
|Rəqəmsal İmza Mənşəyi|Paketdəki rəqəmsal imzaların kökü olan OPC hissəsi.|Paket|İstəyə Bağlı
|Rəqəmsal İmza|Hər biri rəqəmsal imza ehtiva edən OPC hissələri.|Rəqəmsal İmza Mənşəyi|İSTEĞE BAĞLI
|Rəqəmsal İmza Sertifikatı|Rəqəmsal imza sertifikatı olan OPC hissələri.|Rəqəmsal İmza|İstəyə Bağlıdır
|PrintTicket|3D Model hissəsində 3D obyekt(lər)i çıxararkən istifadə ediləcək parametrləri təmin edir.|3D Model|İstəyə bağlı
|Thumbnail|Paketdəki və ya bütövlükdə paketdəki 3D obyektləri təmsil edən kiçik JPEG və ya PNG şəklini ehtiva edir.|Paket|İstəyə bağlı
|3D Tekstura|3D Model hissəsində 3D obyektə rəng tətbiq etmək üçün istifadə edilən teksturadan ibarətdir (genişləndirmələr üçün mövcuddur)|3D Model|İsteğe bağlı
|Xüsusi Hissələr|Metadata ilə əlaqəli OPC hissələri|Paket|İSTEĞE BAĞLI

Spesifikasiyalar sənədinin [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) və [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) bölmələri 3MF sənədi haqqında ətraflı məlumat verir.

## İstinadlar ##

* [3MF Fayl Formatının Xüsusiyyətləri](https://github.com/3MFConsortium/spec_core)

* [3MF - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)


