{
  "date": "2019-12-13",
  "keywords": [
"pptx faylı",
"pptx fayl formatı",
"pptx faylı nədir",
"fayl",
"pptx nümunəsi",
"pptx fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "PPTX fayl formatı və PPTX fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "PPTX - PowerPoint təqdimat faylı formatı",
  "linktitle": "PPTX",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-ppt-azx"
}
},
  "lastmod": "2019-09-10"
}

## PPTX faylı nədir?

PPTX uzantılı fayllar məşhur Microsoft PowerPoint proqramı ilə yaradılmış təqdimat fayllarıdır. Təqdimat faylı formatının ikili olan əvvəlki PPT versiyasından fərqli olaraq, PPTX formatı Microsoft PowerPoint açıq XML təqdimat faylı formatına əsaslanır. Təqdimat faylı hər bir slaydın mətn, şəkillər, formatlaşdırma, animasiyalar və digər mediadan ibarət ola biləcəyi slaydlar toplusudur. Bu slaydlar xüsusi təqdimat parametrləri ilə slayd şouları şəklində tamaşaçılara təqdim olunur.

## Qısa tarix

PPTX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. PPTX-dən əvvəl istifadə edilən ümumi fayl formatı təmiz ikili fayl formatı olan PPT idi. Yeni fayl növü kiçik fayl ölçüləri, daha az korrupsiya dəyişiklikləri və yaxşı formatlaşdırılmış şəkillərin təqdim edilməsi kimi üstünlükləri əlavə etdi. 2000-ci ilin əvvəllərində Microsoft **Office Open XML** standartına uyğunlaşmaq üçün dəyişikliyə getməyə qərar verdi. 2007-ci ilə qədər bu yeni fayl formatı Office 2007-nin bir hissəsi oldu və Microsoft Office-in yeni versiyalarında da davam etdirilir.

## PPTX Fayl Formatının Xüsusiyyətləri

Office Open XML fayl formatı ilə yaradılan fayllar, bütün tərkib faylları arasında əlaqə təmin edən digər fayllarla birlikdə XML faylları toplusudur. Bu kolleksiya əslində məzmununa baxmaq üçün çıxarıla bilən sıxılmış arxivdir. Bunu etmək üçün sadəcə olaraq zip ilə PPTX fayl uzantısının adını dəyişdirin və məzmununu müşahidə etmək üçün onu çıxarın (Bax: Microsoft tərəfindən [PPTX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)).

Aşağıdakı bölmələr bunların hər birinə bir qədər işıq salır.

### [Məzmun_Növləri].xml

Bu, zip çıxarıldıqda baza səviyyəsində tapılan yeganə fayldır. Paketdəki hissələrin məzmun növlərini sadalayır. Paketə daxil olan XML fayllarına bütün istinadlar bu XML faylında istinad edilir. Aşağıda slayd hissəsi üçün məzmun növü verilmişdir:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Paketə yeni hissələrin əlavə edilməsi lazımdırsa, bu, yeni hissənin əlavə edilməsi və .rels faylları daxilində hər hansı əlaqənin yenilənməsi ilə edilə bilər. Nəzərə almaq lazımdır ki, belə bir dəyişiklik üçün Content_Types.xml də yenilənməlidir.

### \_rels (Qovluq) ###

Digər hissələr və paketdən kənar resurslar arasındakı əlaqələr əlaqələr hissəsi tərəfindən qorunur. Əlaqələr qovluğunda paket səviyyəli əlaqələri saxlayan tək XML faylı var. PPTX fayllarının əsas hissələrinə keçidlər bu faylda URI-lər kimi var. Bu URI-lər hər bir əsas hissənin paketlə əlaqə növünü müəyyən edir. Bura ppt/presentation.xml kimi yerləşən əsas ofis sənədi ilə əlaqə və əsas və genişləndirilmiş xüsusiyyətlər kimi docProps daxilindəki digər hissələr daxildir.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

Bir və ya bir neçə əlaqənin mənbəyi olan sənədin hər bir hissəsinin öz əlaqələr hissəsi olacaq, burada hər bir belə əlaqə hissəsi hissənin \_rels alt qovluğunda yerləşir və adın adına '.rels' əlavə edilməklə adlandırılır. hissəsi. Əsas məzmun hissəsinin (presentation.xml) öz əlaqələr hissəsi (presentation.xml.rels) var. O, slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml kimi məzmunun digər hissələri ilə əlaqələri, həmçinin xarici keçidlər üçün URI-ləri ehtiva edir.

#### Açıq Münasibət ####

Açıq əlaqə üçün a-nın Id atributundan istifadə edərək mənbəyə istinad edilir<Relationship> element. Yəni mənbədəki İd hədəfə açıq istinadla birbaşa əlaqə elementinin İd-si ilə xəritələnir.

Məsələn, slaydda bu kimi hiperlink ola bilər:

```
<a:hlinkClick r:id#"rId2">
```

r:id#rId2 slayd üçün əlaqələr hissəsində aşağıdakı əlaqəyə istinad edir (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Gizli Münasibət ####

Gizli əlaqə üçün `-ə belə birbaşa istinad yoxdur<Relationship> ID`. Bunun əvəzinə istinad başa düşülür.

### ppt Qovluğu ###

Bu, Təqdimatın məzmunu ilə bağlı bütün təfərrüatları ehtiva edən əsas qovluqdur. Varsayılan olaraq, aşağıdakı qovluqlara malikdir:

* \_rels

* mövzu

* slaydlar

* slideLayouts

* slideMasters


və aşağıdakı xml faylları:

* təqdimat.xml

* presProps.xml

* tableStyles.xml

* viewProps.xml


## İstinadlar ##

* [[MS-PPTX] - PPTX Fayl Formatı](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


